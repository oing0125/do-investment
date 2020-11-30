<template>
  <div id="container">
    <div id="top-area">
      <input type="text"/>
      <button>검색</button>
    </div>
    <div id="contents-area">
      <line-chart :chart-data='datacollection' style="width: 300px; height: 200px;"></line-chart>
    </div>
  </div>
</template>

<script>
import LineChart from "../charts/LineChart";

export default {
  name: "Summary",
  components: {LineChart},
  data(){
    return{
      datacollection: null
    }
  },
  mounted () {
    this.fillData()
  },
  methods: {
    fillData () {
      this.datacollection = {
        labels: [this.getRandomInt(), this.getRandomInt()],
        datasets: [
          {
            label: 'Data One',
            backgroundColor: '#f87979',
            data: [this.getRandomInt(), this.getRandomInt()]
          }, {
            label: 'Data One',
            backgroundColor: '#f87979',
            data: [this.getRandomInt(), this.getRandomInt()]
          }
        ]
      }
    },
    getRandomInt () {
      return Math.floor(Math.random() * (50 - 5 + 1)) + 5
    }
  }
}
</script>

<style scoped>
#top-area{
  padding: 20px 10px 20px 10px;
}
</style>
