<template>
<div class="intro" v-bind:class="{ 'intro-active': textIsActive }">
  <div class="click-area" v-on:click="pClickHandler">
  <h1 class="title">Editable card test</h1>
  <Flipper :active="textIsActive" />
  </div>
  <p>{{introText}}</p>
  <textarea v-model="introText" class="edit-intro" v-if="textIsActive" />
</div>
</template>

<script>
import Flipper from './Flipper.vue'

export default {
  name: 'intro',
  methods: {
    pClickHandler: function () {
      this.textIsActive ? this.textIsActive = false : this.textIsActive = true
    }
  },
  components: {
    Flipper
  },
  data () {
    return {
      introText: 'Edit this text: Elit fugiat elit laborum consectetur nisi elit irure reprehenderit qui excepteur deserunt labore sint ad veniam irure ut dolore ut nulla reprehenderit eiusmod est mollit ut fugiat qui dolore sed dolore velit sed fugiat dolore in qui voluptate occaecat non qui tempor nostrud dolor duis cillum pariatur aliqua dolor minim eu et mollit nulla sunt excepteur id mollit in proident dolor magna do cupidatat dolor nulla tempor.',
      textIsActive: false
    }
  }
}
</script>

<style lang="css" scoped>
.intro {
  background-color: #fff;
  grid-column-start: 2;
  grid-column-end: span 6;
  width: 100%;
  position: relative;
  margin: 2em 0px;
  min-height: 200px;
  -webkit-box-shadow: 4px 3px 8px -2px rgba(0,0,0,0.66);
  -moz-box-shadow: 4px 3px 8px -2px rgba(0,0,0,0.66);
  box-shadow: 4px 3px 8px -2px rgba(0,0,0,0.66);
  padding: 10px 10px 10px 10px;
}

.intro-active {
  min-height: 350px;
}

.edit-intro {
  width: 80%;
  height: 150px;
  font-family: "Source Code Pro", "monospace";
  font-size: 16px;
  border: 0px solid;
  background: #ddd;
}

</style>