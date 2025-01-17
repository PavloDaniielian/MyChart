<template>
  <div id="app">
    <RadarChartComponent />
  </div>
</template>

<script>
import RadarChartComponent from './components/RadarChartComponent.vue';

export default {
  name: 'App',
  components: {
    RadarChartComponent,
  },
};
</script>

<style>
#app {
  font-family: Helvetica, Arial, sans-serif;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>