<script lang="ts" setup>
import {ref,watch } from "vue";
import { useRoute } from 'vue-router'
const activeIndex = ref()
const route = useRoute()
watch(
    () => route.name,
    (value) =>
    {
      activeIndex.value = value;
    }
);


</script>

<template>
  aside
  hoge<br>
  hoge<br>
  hoge<br>hoge<br>
  hoge<br>hoge<br>
  hoge<br>hoge<br>hoge<br>hoge<br>hoge<br>
  <nav>
    <router-link to="/">Home</router-link> |
    <router-link to="/about">About</router-link>
  </nav>


  <el-menu  :default-active="activeIndex" router>
    <el-menu-item index="home" :route="{ name:'home' }">Home</el-menu-item>
    <el-menu-item index="about" :route="{ name:'about' }">About</el-menu-item>
  </el-menu>
</template>



<style scoped>

</style>