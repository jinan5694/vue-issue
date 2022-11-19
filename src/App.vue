<script setup>
import { ref } from 'vue';
import TheTest from './components/TheTest.vue'
const value = ref('')
const filters = ref([])
</script>

<template>
  <div id="app">
    <p>输入些内容，会触发 TheTest 组件对 filters 属性的 watch</p>
    <p>input some thing, will emit TheTest component watch of props filter</p>

    <input type="text" v-model="value" placeholder="input here">
    <TheTest :filters="[{ foo: 'bar' }]"></TheTest>
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

@media (min-width: 1024px) {
  header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  }

  .logo {
    margin: 0 2rem 0 0;
  }

  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }
}
</style>
