<template>
  <home/>
</template>

<script>
import Home from './components/home.vue'

export default {
  name: 'App',
  components: {
    Home
  }
}
</script>

<style>
html{
   height: 100%;
}
body{
  margin: 0;
  padding: 0;
  width: 100%;
  height: 100%;
}
#app {
  width: 100%;
  height: 100%;
}
a {
  text-decoration: none;
  outline: 0;
}
.fl{
  float: left;
}
.fr{
  float: right;
}
.clearfix:after {
  content: "";
  display: block;
  height: 0;
  clear: both;
}

.clearfix:after {
  content: "";
  display: block;
  height: 0;
  clear: both;
}
</style>
