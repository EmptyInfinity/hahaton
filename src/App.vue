<template>
<div id="app">
  <div class="container-fluid">
    <div class="row">
      <div class="col-2"></div>
      <div class="col-8">
        <div>
          <h1 class="h1" v-bind:style="{fontSize: h1FontSize + 'px' }">EWM</h1>
          <h3 class="h3" v-show="isClicked">Escape With Me</h3>
          <hr>
        <div class="arrow-back" v-show="isClickedReverse" @click="btnClickReverse"></div>
        </div>
        <div class="btns-wrap" v-show="isClicked">
          <button @click="btnClick" class="up btn btn-primary">Earthquake</button>
          <button class="up btn btn-primary">Earthquake</button>
          <button class="up btn btn-primary">Earthquake</button>
          <button class="up btn btn-primary">Earthquake</button>
        </div>
        <div class="btns-desc" v-show="isClicked">
          Lorem ipsum dolor sit amet, consectetur adipisicing elit. Magni, voluptas temporibus, maiores ea asperiores illo accusamus facere, eum esse numquam ipsum architecto. Nostrum veniam in qui dolor est facilis veritatis.
        </div>
        <div class="footer">
          <hr>
          &#9400; Copywrited 2018 <br>
          Broken machine hahaton NACA
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
}
.up{
  text-transform: uppercase;
}
.col-8{
  position: relative;
}
.col-2{
  height: 100vh;
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
  cursor: pointer;
  border-radius: 50%;
  width: 70px;
  height: 70px;
  background: url('assets/back-icon3.png') no-repeat center;
}
.btns-wrap{
  padding-top: 30px;
  display: flex;
  flex-wrap: wrap;
  justify-content: space-between;
  max-width: 320px;
  margin: auto;
  height: 200px;
}
.btns-wrap .btn{
  height: 60px;
  width: 150px;
}
.btns-desc{
  text-align: center;
}
.footer{
  position: absolute;
  bottom: 0;
  left: 0;
  width: 100%;
  margin: auto;
  padding: 0 15px;
}
</style>
