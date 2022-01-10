<template>
  <div class="home">
    <RandomFloat />
  </div>
</template>

<script>
import RandomFloat from "./components/RandomFloat.vue";

export default {
  name: "App",
  components: {
    RandomFloat,
  },
};
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Open+Sans:wght@300;400;500;600;700;800&display=swap');
body{
  background-color: #70dbc4;
  font-family: 'Open Sans', sans-serif;
}


</style>
