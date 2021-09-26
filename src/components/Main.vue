<template>
  <div>
    <div class="container mt-5 mb-5">
      <div class="row gx-5">
        <div
          v-for="(disco, index) in Albums"
          :key="index"
          class="col-6 col-md-4 col-lg-2 m-3"
        >
          <Disck :info="disco" />
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import axios from "axios";
import Disck from "./Disck.vue";
export default {
  name: "Main",
  components: {
    Disck,
  },
  data() {
    return {
      Albums: [],
      APIUrl: "https://flynn.boolean.careers/exercises/api/array/music",
    };
  },
  created() {
    this.getAlbum();
  },
  methods: {
    getAlbum() {
      axios.get(this.APIUrl).then((result) => {
        console.log(result.data);
        this.Albums = result.data.response;
      });
    },
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss"></style>
