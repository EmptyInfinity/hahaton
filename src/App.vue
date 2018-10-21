<template>
<div id="app">
  <div class="container-fluid">
    <div class="row">
      <div class="col-2"></div>
      <div class="col-8">
        <div>
          <div class="arrow-back" v-show="isClickedReverse" @click="btnClickReverse"></div>
          <h1 class="h1" v-bind:style="{fontSize: h1FontSize + 'px' }">EWM</h1>
          <h3 class="h3" v-show="isClicked">Escape With Me</h3>
          <hr>
        <div class="check-list" v-show="isClickedReverse">
          <h4><span class="blue">Earthquake</span> - is a Lorem ipsum dolor, sit amet consectetur adipisicing elit. Accusantium harum deserunt beatae sequi dolorum officiis excepturi dicta consequatur autem tenetur.</h4>
          <div class="question">
            <p>Are you <span>inside</span> / <span>outside</span> ?</p>
          </div>
          <div class="d-flex justify-content-between flex-wrap">
            <div class="your-checklist w-50">
              <form>
                <p class="title">Yours checklist</p>
                <div class="list">
                  <div class="item">
                    <div class="icon"></div>
                    <p class="item-text">Battery operated radio</p>
                  </div>
                  <div class="item">
                    <div class="icon"></div>
                    <p class="item-text">Torch (with spare batteries)</p>
                  </div>
                  <div class="item">
                    <div class="icon"></div>
                    <p class="item-text">First aid kit</p>
                  </div>
                </div>
              </form>
            </div>
            <div class="recom-checklist w-50">
              <form>
                <p class="title">Recommended</p>
                <div class="list">
                  <div class="item">
                    <div class="icon"></div>
                    <p class="item-text">Battery operated radio</p>
                  </div>
                  <div class="item">
                    <div class="icon"></div>
                    <p class="item-text">Torch (with spare batteries)</p>
                  </div>
                  <div class="item">
                    <div class="icon"></div>
                    <p class="item-text">First aid kit</p>
                  </div>
                  <div class="item">
                    <div class="icon"></div>
                    <p class="item-text">Copy of home emergency plan</p>
                  </div>
                  <div class="item">
                    <div class="icon"></div>
                    <p class="item-text">Important documents</p>
                  </div>
                  <div class="item">
                    <div class="icon"></div>
                    <p class="item-text">Non-perishable food and drinking water for up to three days</p>
                  </div>
                  <div class="item">
                    <div class="icon"></div>
                    <p class="item-text">Mobile phone and charger</p>
                  </div>
                  <div class="item">
                    <div class="icon"></div>
                    <p class="item-text"> Prescriptions and medications</p>
                  </div>
                  <div class="item">
                    <div class="icon"></div>
                    <p class="item-text"> Clothing and strong shoes</p>
                  </div>
                  <div class="sos">

                  </div>
                </div>
              </form>
            </div>
          </div>
        </div>
        </div>
        <div class="btns-wrap" v-show="isClicked">
          <button @click="btnClick" class="up btn btn-1">
            <p><span class="yellow">T</span>ornado</p></button>
          <button class="up btn btn-2">
            <p><span class="yellow">V</span>olcano</p></button>
          <button class="up btn btn-3">
            <p><span class="yellow">D</span>rought</p></button>
          <button class="up btn btn-4">
            <p><span class="yellow">W</span>ildfire</p></button>
        </div>
        <div class="btns-desc w-50 m-auto" v-show="isClicked">
         Escape With Me (EWM) is created to help you to survive in any natural hazardous situation. To find some recommendations, just click on the button above. Your life is in your hands!
        </div>
        <div class="footer">
          <hr>
          &#9400; Copywrited 2018 <br>
          <p>NASA Space Apps Challenge 2018 - Don’t Forget the Can Opener! - Broken Machine - Project page - <a href="https://2018.spaceappschallenge.org/challenges/volcanoes-icebergs-and-asteroids-oh-my/dont-forget-can-opener/teams/broken-machine/project">EWM</a></p> 
        </div>
      </div>
      <div class="col-2"></div>
    </div>
  </div>
</div>
</template>

<script>
export default {
  name: 'app',
  data () {
    return {
      h1FontSize: 50,
      isClicked: true,
      isClickedReverse: false
    }
  },
  methods: {
    btnClick(){
      this.h1FontSize = 30;
      this.isClicked = false;
      this.isClickedReverse = true;
    },
    btnClickReverse(){
      this.h1FontSize = 50;
      this.isClicked = true;
      this.isClickedReverse = false;
    }
  }
}
</script>

<style>
@import url('https://fonts.googleapis.com/css?family=Audiowide|Roboto:400,500,700|VT323');
body{
  background: #35495e;
  min-height: 100vh;
}
.up{
  text-transform: uppercase;
}
.col-8{
  position: relative;
}
.col-2{
  min-height: 100vh;
  background: #1a2530;
}
.h1{
  font-size: 50px;
  margin-top: 10px;
  text-align: center;
  font-family: 'Audiowide', cursive;
}
.h3{
  text-align: center;
  text-transform: uppercase;
  font: 300 17px sans-serif;
}
.arrow-back{
  position: absolute;
  top: 0;
  cursor: pointer;
  border-radius: 50%;
  width: 55px;
  height: 55px;
  background: url('assets/back-icon3.png') no-repeat center;
}
.btns-wrap{
  padding-top: 30px;
  display: flex;
  flex-wrap: wrap;
  justify-content: space-between;
  margin: auto;
  max-width: 620px;
  height: 670px;
}
.btns-wrap .btn{
  height: 300px;
  width: 300px;
  background-size: contain;
  transition: .3s;
}
.btns-wrap .btn p{
  color: #fff;
  font: 900 22px 'Audiowide', cursive;
  letter-spacing: 4px;
  background: rgba(0, 0, 0, 0.8);
  padding: 2px 10px;
  width: fit-content;
  margin: auto;
}
.yellow{
  color: #fed000 !important;
}
.blue{
  color: #00afaf !important;
}
.btn-1{
  background: url('assets/tornado_blur.jpg') no-repeat center;
  border-radius: 50px 0 50px 0;
}
.btn-2{
  background: url('assets/volcano_blur.jpg') no-repeat center;
  border-radius:  0 50px 0 50px;
}
.btn-3{
  background: url('assets/drought_blur.jpg') no-repeat center;
  border-radius:  0 50px 0 50px;
}
.btn-4{
  background: url('assets/wildfire_blur.jpg') no-repeat center;
  border-radius: 50px 0 50px 0;
}
.btn-1:hover{
  background: url('assets/tornado2.jpg') no-repeat center;
  background-size: contain;
  border-radius: 50px 0 50px 0;
}
.btn-2:hover{
  background: url('assets/volcano2.jpg') no-repeat center;
  background-size: contain;
  border-radius:  0 50px 0 50px;
}
.btn-3:hover{
  background: url('assets/drought2.jpg') no-repeat center;
  background-size: contain;
  border-radius:  0 50px 0 50px;
}
.btn-4:hover{
  background: url('assets/wildfire2.jpg') no-repeat center;
  background-size: contain;
  border-radius: 50px 0 50px 0;
}
.btns-desc{
  text-align: center;
  margin-bottom: 90px;
}
.check-list h4{
  font-weight: 300;
  padding: 0 20px;
}
.question{
  margin: 20px;
  color: #fff;
  background: #1a2530;
  border-radius: 32px 2px;
  font-size: 25px;
  padding: 10px 15px 1px 15px;
}
.question span{
  text-decoration: underline;
  color: #00afaf;
  cursor: pointer;
  font-weight: bold;
}
.footer{
  position: absolute;
  bottom: 0;
  left: 0;
  width: 100%;
  margin: auto;
  padding: 0 15px;
}
.footer p{
  text-align: center;
}
.footer a{
  color:#1a2530;
}
.check-list form{
  margin: 10px 20px;
  background:#1a2530;
  color: #fff;
}
.title{
  font: 500 22px 'Roboto', cursive;
  text-align: center;
  padding: 5px;
  margin-bottom: 0;
  border-bottom: 1px solid #fff;
}
.item{
  display: flex;
  align-items: center;
  padding: 8px;
}
.item p{
  margin-bottom: 0;
  font: 400 15px 'Roboto', cursive;
}
.icon{
  background: url('assets/checkbox_active.png') no-repeat center;
  background-size: contain;
  min-width: 30px;
  height: 30px;
  margin-right: 8px;
  cursor: pointer;
}
</style>