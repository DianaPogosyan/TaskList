<template>
  <div class="app">
    <img alt="Vue logo" src="@/assets/logo.png">
    <HelloWorld msg="Welcome to Your Vue.js App"/>
  </div>
</template>

<script>
// @ is an alias to /src
import main from '@/views/main.vue'

export default {
  name: 'App',
  component: {
    main
  }
}

import Vue from 'vue';
import ElementUI from 'element-ui';
import 'element-ui/lib/theme-chalk/index.css';

Vue.use(ElementUI);

</script>

<style>
* {
  margin: 0;
  padding: 0;
  font-family: sans-serif; 
}
</style>