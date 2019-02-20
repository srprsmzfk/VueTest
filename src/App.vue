<template>
  <div id="app">

    <!--<HelloWorld msg="Welcome to Your Vue.js App"/>-->
    <DComponent :money = "money" v-on:moneyChange="change($event)"></DComponent>
    <input v-model="factor" class="small">
    <EComponent :money= "money" :factor = "factor" v-on:moneyChange="change($event)"></EComponent>


  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import DComponent from "./components/DComponent";
import EComponent from "./components/EComponent";
import PComponent from "./components/PComponent";

export default {
  name: 'app',
  components: {
    PComponent,
    HelloWorld,
    DComponent,
    EComponent
  },
  data: function () {
    return {
      money: 123,
      factor: 2,
      factor2: 3
    }
  },
  methods: {
    change: function (amount) {
      this.money = amount;
    }
  }
}
//
// function fib(n) {
//   let prev = 0;
//   let curr = 1;
//
//   for (let i = 1; i < n; i++){
//     prev += curr;
//     curr += prev;
//   }
//   return curr;
// }
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
  input{
    width: 25%;
    height: 50px;
    font-size: 40px;
    padding: 7px;
    margin: 10px;
  }
  .small{
    width: 15%;
    height: 25px;
  }
</style>
