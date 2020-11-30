<template>
  <div>
    <nav-bar class="nav-bar">
      <div slot="center">购物街</div>
    </nav-bar>
    <home-swiper :banners="banners"></home-swiper>
  </div>
</template>

<script>
import NavBar from "components/common/navbar/NavBar.vue";
import HomeSwiper from "./childComps/HomeSwiper.vue";
import { getHomeMultiData } from "network/home";

export default {
  name: "Home",
  components: {
    NavBar,
    HomeSwiper,
  },
  data() {
    return {
      banners: [],
    };
  },
  created() {
    getHomeMultiData().then((res) => {
      this.banners = res.data.banner.list;
    });
  },
};
</script>

<style>
.nav-bar {
  background: var(--color-tint);
  color: #fff;
}
</style>