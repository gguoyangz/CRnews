<template>
  <div id="app">
    <router-view/>
    <div id="foot">
      <van-tabbar v-model="active">
        <van-tabbar-item icon="column" @click="goToNavigation('/')">新闻</van-tabbar-item>
        <van-tabbar-item icon="photo" @click="goToNavigation('/')">图片</van-tabbar-item>
        <van-tabbar-item icon="video" @click="goToNavigation('/')">视频</van-tabbar-item>
        <van-tabbar-item icon="manager" @click="goToNavigation('/')">我</van-tabbar-item>
      </van-tabbar>
    </div>
  </div>
</template>
<script>
export default {
  data () {
    return {
      active: 0
    }
  },
  methods: {
    goToNavigation (routerUrl) {
      this.$router.push({ path: routerUrl })
    }
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
}

#nav a {
  font-weight: bold;
  color: #2c3e50;
}

#nav a.router-link-exact-active {
  color: #42b983;
}
</style>
