<template>
  <section class="container">
    <div class="clicker" v-on:click="activeCards += 1">
      <PlusCircle />
    </div>
    <Intro v-for="v in activeCards"/>
  </section>
</template>

<script>
import Intro from '~/components/Intro.vue'
import PlusCircle from '~/components/PlusCircle.vue'

export default {
  components: {
    Intro,
    PlusCircle
  },
  data () {
    return {
      activeCards: 1
    }
  }
}
</script>

<style>
@import url('https://fonts.googleapis.com/css?family=Open+Sans:400,600,800');

h1 {
  font-family: "Open Sans", "sans-serif";
  font-weight: 600;
}

.container {
  min-height: 100vh;
  display: grid;
  grid-template-columns: repeat(8, 12.5%);
  align-content: center;
}

.clicker {
  height: 0px;
  width: 0px;
}
@media (max-width: 12450px) {

} 
</style>
