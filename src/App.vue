<template>
  <div id="app">
    <Chart :data="data"></Chart>
  </div>
</template>

<script lang="ts">
import { Component, Vue } from "vue-property-decorator";
import Chart from "./components/Chart.vue";

@Component({
  components: {
    Chart
  }
})
export default class App extends Vue {
  data = [
    { key: "data1", count: 500 },
    { key: "data2", count: 250 },
    { key: "data3", count: 150 },
    { key: "data4", count: 100 }
  ];
}
</script>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
