<template>
  <div id="app">
    <!-- <my-header></my-header>
    <left-menu></left-menu>
    <my-home></my-home> -->

    <router-view></router-view>





  </div>
</template>

<style>
#app {
  font-family: Helvetica, sans-serif;
  /*text-align: center;*/
  width: 100%;height: 100%;
}
*{margin: 0;padding: 0;}
body,html{margin: 0;padding: 0;width: 100%;height: 100%;}

</style>



<script>
import myHeader from './components/common/Header.vue';
import leftMenu from './components/common/LeftMenu.vue'
import myHome from './components/common/Home.vue'
export default {
  data () {
    return {
      msg: 'Want something new?',
      isCollapse: true
    }
  },
  components:{
    myHeader,
    leftMenu,
    myHome
  },

  methods: {
    startHacking () {
      this.$notify({
        title: 'Shhh',
        message: 'Just be patient...',
        duration: 6000
      })
    },
    handleOpen(key, keyPath) {
        console.log(key, keyPath);
      },
      handleClose(key, keyPath) {
        console.log(key, keyPath);
      }
  }
}
</script>
