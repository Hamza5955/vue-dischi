<template>
  <header>
    <img
      src="https://www.wallpapertip.com/wmimgs/17-176153_download-logo-spotify-png.png"
      alt=""
    />
    <label
      >Seleziona un genere
      <select
        v-model="inputOption"
        @change="$emit('search', inputOption)"
        class="select"
      >
        <option>Seleziona un genere</option>
        <option>Rock</option>
        <option>Pop</option>
        <option>Jazz</option>
        <option>Metal</option>
      </select>
    </label>
  </header>
</template>

<script>
export default {
  name: "Header",
  data() {
    return {
      inputOption: "",
    };
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import "../style/general.scss";
@import "../style/vars.scss";
header {
  background-color: $blueblack;
  height: 70px;
  padding: 10px;
  img {
    height: 100%;
  }
}
</style>
