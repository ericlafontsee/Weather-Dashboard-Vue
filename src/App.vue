<template>
  <the-header></the-header>
  <div class="container">
    <div class="row">
      <div class="col-8 col-md-4">
        <search-box></search-box>
      </div>
      <div class="col-12 col-md-8">
        <current-weather></current-weather>
      </div>
    </div>
    <div class="row">
      <div class="col-12">
        <the-forecast></the-forecast>
      </div>
    </div>
  </div>
</template>

<script>
import TheHeader from "./components/layout/TheHeader.vue";
import CurrentWeather from "./components/layout/CurrentWeather.vue";
import TheForecast from "./components/layout/TheForecast.vue";
import SearchBox from "./components/UI/SearchBox.vue";

export default {
  name: "App",
  components: {
    TheHeader,
    CurrentWeather,
    TheForecast,
    SearchBox
  }
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
