<template>
  <div id="chart"></div>
</template>

<script lang="ts">
import { Component, Prop, Vue } from "vue-property-decorator";
import c3 from "c3";

@Component
export default class Chart extends Vue {
  @Prop()
  data!: { key: string; count: number }[];

  mounted() {
    c3.generate({
      bindto: "#chart",
      data: {
        columns: this.data.map(value => [value.key, value.count]),
        type: "donut"
      }
    });
  }
}
</script>

<style scoped>
@import "~c3/c3.min.css";
</style>
