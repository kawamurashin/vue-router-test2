<template>
  <el-container>
  <el-aside id="aside">
    <AsideComponent></AsideComponent>

  </el-aside>
  <el-main>
    <nav>
      <router-link to="/">Home</router-link> |
      <router-link to="/about">About</router-link>
    </nav>
    <router-view/>
  </el-main>
  </el-container>
</template>

<!--
<script lang="ts" setup>
import AsideComponent from "@/components/aside/AsideComponent.vue";
import {watch} from "vue";
import {useRoute} from "vue-router";
const route = useRoute()
watch(
    () => route.name,
    (value) =>
    {
      console.log("value " + value!.toString())
    }
);


</script>
-->
<script>
import AsideComponent from "@/components/aside/AsideComponent.vue";
export default {
  components: {AsideComponent},
}
</script>

<style>
body
{
  margin: 0px;
}


#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;

}

nav {
  padding: 30px;
}

nav a {
  font-weight: bold;
  color: #2c3e50;
}

nav a.router-link-exact-active {
  color: #42b983;
}
#aside
{
  width: 150px;
  min-height: 100vh;
  background-color: lightblue;
}
</style>
