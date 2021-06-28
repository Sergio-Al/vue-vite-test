<template>
  <nav class="mb-4 max-w-5xl m-auto">
    <ul class="flex">
      <li class="mr-6">
        <router-link class="text-blue-500 hover:text-blue-800" to="/home">Home</router-link>
      </li>
      <li class="mr-6">
        <router-link class="text-blue-500 animate-pulse" to="/about">About</router-link>
      </li>
    </ul>
  </nav>
  <router-view></router-view>
  <img class="m-auto" alt="Vue logo" src="./assets/logo.png" />
  <HelloWorld msg="Hello Vue 3 + Vite" />
  <div class="p-6 max-w-sm mx-auto bg-white rounded-xl shadow-md flex items-center space-x-4">
    <div class="flex-shrink-0">
      <img class="h-12 w-12" src="/img/logo.svg" alt="ChitChat Logo">
    </div>
    <div>
      <div class="text-xl font-medium text-black">ChitChat</div>
      <p class="text-gray-500">You have a new message!</p>
    </div>
  </div>

  <div class="p-6 max-w-2xl mx-auto mt-6 bg-white rounded-xl shadow-md flex items-start space-x-4">
    <div class="flex-shrink-0">
      <img src="" class="h-12 w-12" alt="">
    </div>
    <div class="flex items-start flex-col">
      <div class="text-xl font-medium text-black">
        MyCard
      </div>
      <p class="text-gray-500">This is my message, so how is this?</p>
    </div>
  </div>

  <div class="max-w-2xl flex flex-col bg-blue-600 shadow-xl font-medium content-center p-8 m-auto rounded-xl text-white mt-6">
    <h1>Hello!!!</h1>
    <p>This is my text</p>
    <p class="m-auto">{{inputData}}</p>
  </div>

  
  <form @submit.prevent="submitData" action="" class="max-w-xl shadow-xl p-9 m-auto rounded-2xl">
    <input type="text" v-model="inputData" class="w-64 m-auto border-solid border-gray-500 shadow-xl focus:outline-none focus:ring-2 focus:ring-green-500 focus:ring-opacity-50 rounded-2xl px-2" placeholder="Your Text!">
  </form>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'

export default {
  components: {
      HelloWorld,
  },
  data() {
    return {
      inputData: null,
      resultInputData: null,
    }
  },
  method: {
    submitData() {
      this.resultInputData = this.inputData;
    }
  }
}

// This starter template is using Vue 3 experimental <script setup> SFCs
// Check out https://github.com/vuejs/rfcs/blob/script-setup-2/active-rfcs/0000-script-setup.md
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
