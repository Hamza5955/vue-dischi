<template>
  <div>
    <div class="card p-3">
      <div class="card-img align-center">
        <img :src="info.poster" :alt="info.title" />
      </div>

      <div class="text-center">
        <h5 class="">{{ info.title }}</h5>
        <p class="">{{ info.author }}</p>
        <p class="">{{ info.year }}</p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "MainCard",
  props: ["info"],
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import "../style/vars.scss";
.card {
  background-color: $blueblack;
  width: 230px;
  height: 380px;
  h5 {
    color: white;
    font-weight: 900;
  }
  .card-img {
    width: 200px;
    height: 200px;
    img {
      width: 200px;
      height: 200px;
    }
  }
  p {
    color: $greyc;
  }
}
</style>
