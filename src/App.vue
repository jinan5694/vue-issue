<script setup>
import { ref } from 'vue';
import TheTest from './components/TheTest.vue'

// the value is not relative any thing
const value = ref('')
</script>

<template>
  <div id="app">
    <h1>Case</h1>
    <p>input some thing, will emit TheTest component watch of props filter</p>
    <p>输入些内容，会触发 TheTest 组件对 filters 属性的 watch</p>
    <input type="text" v-model="value" placeholder="input here">
    <!-- the value of filters is a "normal data" -->
    <TheTest :filters="[{ foo: 'bar'}]"></TheTest>
  </div>
</template>

<style scoped>
header {
  line-height: 1.5;
}

.logo {
  display: block;
  margin: 0 auto 2rem;
}


</style>
