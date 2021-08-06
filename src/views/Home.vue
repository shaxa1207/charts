<template>
  <div class="home d-flex">
    <ch-aside />
    <div class="main-part">
      <search-bar />
    </div>
  </div>
</template>

<script>
// @ is an alias to /src
import ChAside from "../components/ch-aside.vue";
import SearchBar from "../components/searchBar.vue";

export default {
  name: "Home",
  components: {
    ChAside,
    SearchBar,
  },
};
</script>
<style lang="scss">
@import url("https://fonts.googleapis.com/css2?family=Lato:ital,wght@0,100;0,300;0,400;0,700;0,900;1,100;1,300;1,400;1,700;1,900&display=swap");
.home {
  background: #f6f8fb;
  .main-part {
    width: 100%;
    padding: 24px 36px;
  }
}
</style>
