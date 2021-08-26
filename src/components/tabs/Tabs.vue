<template>
  <article class="shop__tabs">
    <ul class="tabs__items">
      <li
        :class="{ 'is-active': tab.isActive }"
        class="tabs__item"
        v-for="(tab, index) in tabs"
        :key="index"
        @click="selectTab(tab)"
      >
        {{ tab.name }}
      </li>
    </ul>
    <section class="tabs__body-shadow">
      <slot></slot>
    </section>
  </article>
</template>

<script>
export default {
  data() {
    return {
      tabs: [],
    };
  },
  methods: {
      selectTab(selectedTab) {
          this.tabs.forEach(tab => tab.isActive = tab.name === selectedTab.name)
      }
  },
  created() {
    this.tabs = this.$children;
  },
};
</script>
