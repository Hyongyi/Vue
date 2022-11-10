<template>
  <img alt="Vue logo" src="./assets/logo.png">
  <HelloWorld msg="Welcome to Your Vue.js App"/>
  <div>
    {{logo}}
    <h4>XX 원룸</h4>   <!-- 데이터를 집어넣고 싶을시 {{변수명}} -->
    <p>{{price1}}만원</p>
  </div>
    <div>
    <h4>XX 원룸</h4>
    <p>{{price2}} 만원</p>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'

export default {
  name: 'App',
  data() {
    return {
      //데이터 보관 장소
      price1 : 60,
      price2 : 70,
      logo : '원룸샵'

    }
  },
  components: {
    HelloWorld
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
  margin-top: 60px;
}
</style>
