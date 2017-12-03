<template>
  <div class="switchbox" v-bind:class="{ 'swichbox-active': active }">
    <div class="flipper" v-bind:class="{ 'flipper-active': active }" ></div>
  </div>
</template>

<script>
export default {

  name: 'Flipper',
  props: ['active'],
  data () {
    return {
      isActive: true
    }
  }
}
</script>

<style lang="css" scoped>
.switchbox {
  position: absolute;
  top: 25px;
  right: 25px;
  background-color: #fff;
  height: 10px;
  width: 40px;
  border: 2px solid #ccc;
}

.swichbox-active {
  background-color: #0f0;
}

.flipper {
  background-color: #000;
  position: absolute;
  top: -5px;
  right: 0px;
  width: 20px;
  height: 20px;
}

.flipper-active {
  right: 20px;
}
</style>