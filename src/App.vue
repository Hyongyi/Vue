<template>
  <div class="menu">
    <a v-for="(a,i) in menu" :key="i">{{ a }}</a>
  </div>

  <div class="black-bg" v-if="modal == true">
    <div class="white-bg">
      <h4>상세페이지</h4>
      <p>내용</p>
      <button @click="modal = false">닫기</button>
    </div>
  </div>

  <!-- <img alt="Vue logo" src="./assets/logo.png"> -->
  <!-- <HelloWorld msg="Welcome to Your Vue.js App"/> -->


<div v-for="(a,i) in 6" :key="i">
    <img :src='oneroom[i].image' alt="사진1" class="room-img"> 
    <h4>{{oneroom[i].title}}</h4> 
    <p>{{oneroom[i].price}}원</p>
    <p>{{oneroom[i].content}}</p>
  </div>
</template>

<script>
// import HelloWorld from './components/HelloWorld.vue'
import data from './assets/oneroom.js'

export default {
  name: 'App',
  data() {
    return {
      //데이터 보관 장소
      oneroom :data,
      modal : false,
      img : ['room0','room1','room2'],
      price : [50,60,70],
      menu : ['Home', 'Shop', 'About'],
      products : ['역삼동 원룸', '천호동 원룸', '마포구 원룸'],
      

    }
  },
  methods : {
 
  },
  components: {
    // HelloWorld
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  /* margin-top: 60px; */
}

body {
  margin: 0;
}

div{
  box-sizing: border-box;
}

.black-bg {
  width: 100%;
  height: 100%;
  background: rgba(0, 0, 0, 0.5);
  position: fixed;
  padding: 20px;
}

.white-bg {
  width: 100%;
  background: white;
  border-radius: 8px;
  padding: 20px;
}

.room-img {width: 100%;
margin-top: 40px;}

.menu {
  background: darkslateblue;
  padding :15px;
  border-radius:  5px;
}

.menu a {
  color: white;
  padding: 10px;
}
</style>
