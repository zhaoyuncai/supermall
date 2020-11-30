<template>
  <div id="app">
    <router-view></router-view>
    <man-tab-bar></man-tab-bar>
  </div>
</template>

<script>
import ManTabBar from "components/content/ManTabBar";

export default {
  name: "App",
  components: {
    ManTabBar,
  },
};
</script>

<style>
@import "assets/css/base.css";
</style>
