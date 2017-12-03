<template>
<div class="plus-circle">+</div>
</template>

<script>
export default {

  name: 'plus-circle',

  data () {
    return {

    }
  }
}
</script>

<style lang="css" scoped>
.plus-circle {
  width: 80px;
  height: 80px;
  background-color: #fff;
  border-radius: 100%;
  -webkit-box-shadow: 4px 3px 8px -2px rgba(0,0,0,0.66);
  -moz-box-shadow: 4px 3px 8px -2px rgba(0,0,0,0.66);
  box-shadow: 4px 3px 8px -2px rgba(0,0,0,0.66);
  position: fixed;
  bottom: 10px;
  right: 10px;
  text-align: center;
  vertical-align: middle;
  line-height: 80px;
  font-size: 80px;
  color: #000;
  z-index: 999;
}
</style>