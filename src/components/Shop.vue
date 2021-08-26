<template>
  <div class="shop">
    <Tabs>
      <Tab class="tabs__body" name="Монстр Боксы" selected="true">
        <h2 class="tabs__title">Кристаллы Незера</h2>
        <div class="tabs__block">
          <div class="coins__card" v-for="(item, index) in crystals" :key="index">
            <CoinsCard :isDollar="isDollar" :showRedRectangle="showRedRectangle" :item="item" />
          </div>
        </div>
        <h2 class="tabs__title">Монеты Незера</h2>
        <div class="tabs__block">
          <div class="coins__card" v-for="(item, index) in coins" :key="index">
            <CoinsCard :isCrystal="isCrystal" :item="item" />
          </div>
        </div>
      </Tab>
      <Tab class="tabs__body" name="Банк">
        <h2 class="tabs__title">Банк</h2>
        <div class="tabs__block">
          <div class="coins__card" v-for="(item, index) in coins" :key="index">
            <CoinsCard :item="item" />
          </div>
        </div>
      </Tab>
      <Tab class="tabs__body" name="Наборы">
        <h2 class="tabs__title">Наборы</h2>
        <div class="tabs__block">
          <div class="coins__card" v-for="(item, index) in coins" :key="index">
            <CoinsCard :item="item" />
          </div>
        </div>
      </Tab>
      <Tab class="tabs__body" name="Спец предложения">
        <h2 class="tabs__title">Спецпредложения</h2>
        <div class="tabs__block">
          <div class="coins__card" v-for="(item, index) in coins" :key="index">
            <CoinsCard :item="item" />
          </div>
        </div>
      </Tab>
      <Tab class="tabs__body" :name="checkedName()">
        <h2 class="tabs__title">Промокоды</h2>
        <div class="tabs__block">
          <div class="coins__card" v-for="(item, index) in coins" :key="index">
            <CoinsCard :item="item" />
          </div>
        </div>
      </Tab>
    </Tabs>
  </div>
</template>

<script>
import CoinsCard from "./CoinsCard";
import Tab from "../components/tabs/Tab";
import Tabs from "../components/tabs/Tabs";
export default {
  name: "Shop",
  components: {
    CoinsCard,
    Tab,
    Tabs,
  },
  data() {
    return {
      windowWidth: window.innerWidth,
      crystals: [
        {
          x_crystals: 500,
          handfulOfCoins: 100,
          cost: 10,
          imageUrl: require("../assets/images/crystals/one-crystal.png"),
        },
        {
          x_crystals: 500,
          handfulOfCoins: 500,
          cost: 10,
          imageUrl: require("../assets/images/crystals/two-crystals.png"),
        },
        {
          x_crystals: 750,
          handfulOfCoins: 1000,
          cost: 10,
          imageUrl: require("../assets/images/crystals/three-crystals.png"),
        },
        {
          x_crystals: 500,
          handfulOfCoins: 1500,
          cost: 10,
          imageUrl: require("../assets/images/crystals/four-crystals.png"),
        },
        {
          x_crystals: 500,
          handfulOfCoins: 100,
          cost: 10,
          imageUrl: require("../assets/images/crystals/five-crystals.png"),
        },
      ],
      coins: [
          {
          x_crystals: 500,
          handfulOfCoins: 100,
          cost: 10,
          imageUrl: require("../assets/images/crystals/one-crystal.png"),
        },
        {
          x_crystals: 500,
          handfulOfCoins: 500,
          cost: 10,
          imageUrl: require("../assets/images/crystals/two-crystals.png"),
        },
        {
          x_crystals: 750,
          handfulOfCoins: 1000,
          cost: 10,
          imageUrl: require("../assets/images/crystals/three-crystals.png"),
        },
        {
          x_crystals: 500,
          handfulOfCoins: 1500,
          cost: 10,
          imageUrl: require("../assets/images/crystals/four-crystals.png"),
        },
        {
          x_crystals: 500,
          handfulOfCoins: 100,
          cost: 10,
          imageUrl: require("../assets/images/crystals/five-crystals.png"),
        },
      ],
      showRedRectangle: true,
      isDollar: true,
      isCrystal: true
    };
  },
  methods: {
    checkedName() {
      let name;
      if (this.windowWidth < 768) {
        name = ' Промо код '
      } else {
        name = 'Промокоды'
      }
      return name;
    }
  }
};
</script>

<style lang="scss"></style>
