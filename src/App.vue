<template>
  <div id="app">
    <img src="./assets/logo.png">
    <input v-model="name"/>
    <router-view/>
  </div>
</template>

<script lang="ts">
import Vue from 'vue'
import Component from 'vue-class-component'

@Component({})
export default class App extends Vue {
   name:string = 'Simon Zhang';
   age:number =15;
  get MyName():string {
    return `My name is ${this.name}`
  }

  // methods
  sayHello():void {
    alert(`Hello ${this.name},${this.age}`)
  }

  getAge():void {
    alert(`Hello ${this.age}`)
  }

  mounted() {

    this.sayHello();
    this.getAge()
  }
}
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

</style>
