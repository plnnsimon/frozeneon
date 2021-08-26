<template>
  <div id="app">
    <Header />
    <Shop />
  </div>
</template>

<script>
import Header from './components/Header.vue'
import Shop from './components/Shop.vue'
export default {
  name: 'App',
  components: {
    Header,
    Shop
  },
  
}
</script>

<style lang='scss'>
@font-face {
    font-family: 'LeksaSans';
    src: url('./assets/font/LeksaSans-Black.eot');
    src: local('☺'), url('./assets/font/LeksaSans-Black.woff') format('woff'), url('./assets/font/LeksaSans-Black.ttf') format('truetype'), url('./assets/font/LeksaSans-Black.svg') format('svg');
    font-weight: 900;
    font-style: normal;
}

@font-face {
    font-family: 'LeksaSans';
    src: url('./assets/font/LeksaSans-Bold.eot');
    src: local('☺'), url('./assets/font/LeksaSans-Bold.woff') format('woff'), url('./assets/font/LeksaSans-Bold.ttf') format('truetype'), url('./assets/font/LeksaSans-Bold.svg') format('svg');
    font-weight: 700;
    font-style: normal;
}

#app {
  background: url('./assets/images/backgroundImage.png') no-repeat;
  background-size: cover;
}
</style>
