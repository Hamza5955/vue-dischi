<template>
  <div id="app">
    <Header @search="search" />
    <Main :genere="filter" />
  </div>
</template>

<script>
import Main from "./components/Main.vue";
import Header from "./components/Header.vue";
export default {
  name: "App",
  components: {
    Main,
    Header,
  },
  data() {
    return {
      filter: "all",
    };
  },
  methods: {
    search(pippo) {
      this.filter = pippo;
    },
  },
};
</script>

<style lang="scss">
@import "./style/general.scss";
@import "./style/vars.scss";
</style>
