<template>
<div class="home">
  <div class="container px-0">
      <div class="head"></div>
      <div id="main" class="container">
          <h1 class="pt-4 text-center">Nordanå Gård</h1>
          <div  class="container">
            <p>{{home_text.p1.p1a}}<a href="https://sv.wikipedia.org/wiki/%C3%85hus">{{home_text.p1.p1c}}</a>{{home_text.p1.p1b}}</p>
            <p class="pb-4"  >{{home_text.p2.p2a}}<a href="https://en.wikipedia.org/wiki/Kristianstad">{{home_text.p2.p2kris}}</a>{{home_text.p2.p2c}}<a href="https://vattenriket.kristianstad.se/naturum/">{{home_text.p2.p2natur}}</a>{{home_text.p2.p2d}}<a href="http://www.regionmuseet.se/english/the-railway-museum-of-kristianstad.html">{{home_text.p2.p2muse}}</a>{{home_text.p2.p2b}}
              <a href="https://sv.wikipedia.org/wiki/Van%C3%A5s_slott">{{home_text.p2.p2vanas}}</a>{{home_text.p2.p2e}}<a href="https://sv.wikipedia.org/wiki/Vinsl%C3%B6v">{{home_text.p2.p2vins}}</a>{{home_text.p2.p2f}}<a href="https://sv.wikipedia.org/wiki/Pl%C3%B6tsligt_i_Vinsl%C3%B6v">{{home_text.p2.p2plot}}</a>
              {{home_text.p2.p2samt}}<a href="">{{home_text.p2.p2fleder}}</a>
            </p>
      </div>
      <div style="border-bottom: solid #2D4159 0.06rem;" class="embed-responsive embed-responsive-21by9 mb-2">
        <iframe class="embed-responsive-item" src="https://www.youtube.com/embed/FOikrW2D2o0" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
      </div>
        <div class="containe mt-2" >
          <div id="cont" class="row py-5">
              <div class="col-md-6 pb-5">
                <div class="row">
                  <div class="col d-flex justify-content-center">
                      <i class="py-2 fas fa-wifi"></i>
                  </div>
                </div>
                <div class="row">
                  <div class="col d-flex justify-content-center">
                    <h4 class="text-center py-1">{{getFacility.wifi}}</h4>
                  </div>
                </div>
              </div>
              <div class="col-md-6 pb-5">
                <div class="row">
                    <div class="col d-flex justify-content-center">
                      <i class="py-2 fas fa-language"></i>
                    </div>
                </div>
                <div class="row">
                    <div class="col">
                      <h4 class="text-center py-1">{{getFacility.language}}</h4>
                    </div>
                </div>
              </div>
              <div class="col-md-6 pb-5">
                <div class="row">
                  <div class="col d-flex justify-content-center">
                    <i class="py-2 fas fa-paw"></i>
                  </div>
                </div>
                <div class="row">
                  <div class="col">
                    <h4 class="text-center py-1">{{getFacility.pets}}</h4>
                  </div>
                </div>
              </div>
              <div class="col-md-6 pb-5">
                <div class="row">
                  <div class="col d-flex justify-content-center">
                    <i class="fas fa-handshake py-2"></i>
                  </div>
                </div>
                <div class="row">
                  <div class="col d-flex justify-content-center">
                    <h4 class="text-center py-1 ">{{getFacility.smoking}}</h4>
                  </div>
                </div>
              </div>
              <div class="col-md-6 pb-2">
                <div class="row">
                  <div class="col d-flex justify-content-center">
                      <i class="py-2 fas fa-parking"></i>
                  </div>
                </div>
                <div class="row">
                  <div class="col d-flex justify-content-center">
                    <h4 class="text-center py-1">{{getFacility.parking}}</h4>
                  </div>
                </div>
              </div>
              <div class="col-md-6 pb-2">
                <div class="row">
                  <div class="col d-flex justify-content-center">
                    <i class="py-2 fas fa-swimmer"></i>
                  </div>
                </div>
                <div class="row">
                  <div class="col d-flex justify-content-center">
                    <h4 class="text-center py-1">{{getFacility.pool}}</h4>
                  </div>
                </div>
              </div>
          </div>
        </div>
      </div>
  </div>
</div>
</template>

<script>
export default {
  computed:{
    home_text(){
      return this.$store.state.language.home_text
    },
    getFacility(){
      return this.$store.state.language.info
    } 
  }

}
</script>

<style scoped>

.home{
  min-height: 100vh;
}
h4{
  font-family: Arial, Helvetica, sans-serif;
  color: #2D4159;
}
.container .fas , .far {
  font-size: 2rem;
  color: #2D4159;
}

.home #main img{
  height: auto;
  max-width: 25%;
  border-radius: 1rem;
}

.home .container h1{
  font-size: 5rem;
  color:#2D4159;
  font-family: 'Parisienne', cursive;
}

.head {
    height: 20rem;
    min-height: 20rem;
    background-image:  linear-gradient(
        rgba(0, 0, 0, 0.3),
        rgba(0, 0, 0, 0.3)
      ), url('../assets/head.jpg');
    background-size: cover;
    background-position: center;
    background-repeat: no-repeat;
    border-radius: 0.150rem;
   
}

.home .container .container{
  background-color: #EDEAE5;
}



@media only screen and (max-width: 600px) {
  .home .container h1{
    font-size: 2.70rem;
  }
  .home #main img{
    max-width: 0%;
  }
}

@media only screen and (min-width: 600px) {
  .home .container h1{
    font-size: 4rem;
  }
   
}

@media only screen and (min-width: 768px) {
  .home .container h1{
    font-size: 5rem;
  }
  h4{
    font-size: 16px;
  }

}
@media only screen and (min-width: 830px) {
  h4{
    font-size: 16px;
  }
}
@media only screen and (min-width: 992px) {
  h4{
    font-size: 20px;
  }
}

</style>