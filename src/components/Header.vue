<template>
  <header class="header">
    <span class="mobile__btn">
      <img src="../assets/images/back-btn.svg" alt="" />
    </span>
    <div class="header__button header__button-left">
      <button><img src="../assets/images/back-btn.svg" alt="" /> BACK</button>
    </div>
    <div class="header__coins">
      <div class="coins__container">
        <img src="../assets/images/coins_top.png" />
        <div class="container__price">
          <p v-if="windowWidth < 768">{{cutNumber(coins)}}</p>
          <p v-else>{{coins}}</p>
          <p>Coins</p>
        </div>
        <span class="plus__button"><i class="fas fa-plus"></i></span>
      </div>
      <div class="coins__container">
        <img src="../assets/images/crystals_top.png" />
        <div class="container__price">
          <p v-if="windowWidth < 768">{{cutNumber(crystals)}}</p>
          <p v-else>{{crystals}}</p>
          <p>Crystals</p>
        </div>
        <span class="plus__button"><i class="fas fa-plus"></i></span>
      </div>
    </div>
    <span class="mobile__btn button__image"
      ><img class="button__image" src="../assets/images/home-btn.png" alt=""
    /></span>
    <div class="header__button header__button-right">
      <button>
        <span class="button__image"
          ><img
            class="button__image"
            src="../assets/images/home-btn.png"
            alt=""
        /></span>
        HOME
      </button>
    </div>
  </header>
</template>

<script>
export default {
  data() {
    return {
      crystals: 1253,
      coins: 100254,
      windowWidth: window.innerWidth
    }
  },
  mounted() {
    this.cutNumber()
    console.log(window.innerWidth);
  },
  methods: {
    cutNumber(number) {
      console.log(number);
      if (Number(number).toString().length > 4) {
        return (number / 1000).toFixed(1) + "K"
      } else {
        return number
      }
    }
  }
};
</script>

<style lang="scss">
</style>