<template>
  <div class="card">
    <img class="image__rectangle" v-if="showRedRectangle" src="../assets/images/red-rectangle.png" />
    <img v-if="showRedRectangle" class="card__rect" src="../assets/images/red-rect-top.svg" />
    <span v-if="showRedRectangle" class="card__booster">
      <img src="../assets/images/coin-mini.svg" /> x{{ item.x_crystals }}</span
    >
    <span class="card__image">
      <img :src="item.imageUrl" />
    </span>
    <div class="handful__coins">
      <span>x{{ item.handfulOfCoins }}</span>
      <p>Handful of Coins</p>
    </div>
    <span class="card__button">
      <button>
        Купить 
        <span v-if="isDollar" class="card__button-green">$</span> 
        <span v-if="isCrystal" class="card__button-green"><img src="../assets/images/crystal-mini.png" /></span> 
        {{ item.cost }}
      </button>
    </span>
  </div>
</template>

<script>
export default {
  name: "CoinsCard",
  props: ["item", 'showRedRectangle', 'isDollar', 'isCrystal'],
  data() {
    return {};
  },
};
</script>

<style lang="scss">
.coins__card {
  background-image: url("../assets/images/card.png");
  background-size: cover;
}
</style>
