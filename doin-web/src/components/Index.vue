<template>
  <div>
    <Header></Header>
    <Summary></Summary>
  </div>
</template>

<script>

import Header from "./layout/Header"
import Summary from "./contents/Summary";

export default {
  name: 'Index',
  components: {Summary, Header},
  data () {
    return {
      message: 'Welcome to Your Vue.js App'
    }
  }
}
</script>

<style scoped>

</style>
