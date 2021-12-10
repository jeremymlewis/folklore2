<template>
  <div class="home">
      <h2>Click on a story to see more information about it!</h2>
      <div v-for="story in stories" v-bind:key="story.id" class=storyBox>
        <h3>{{story.name}}</h3>
        <div v-on:click="setFocus(story.name)">
        <img :src="require('../images/'+story.image)" :alt="'../images/'+story.image">
        </div>
        <h4>by {{story.author}}</h4>
        </div>
  </div>
</template>

<script>

export default {
  name: 'Home',
  components: {
  },
  // data () {
  //   return
  // },
  computed: {
  stories() {
    return this.$root.$data.stories;
  }
  },
  methods: {
    setFocus(name) {
      console.log(name)
      localStorage.setItem("name", name);
      this.$router.push({ path: '/details' })
    },
  },
}
</script>
<style>
.storyBox {
  margin-left: 10%;
  margin-right: 10%;
  margin-top: 1%;
  width: 80%;
  border: 3px black solid;
  background-color: lightsteelblue;
}

h2 {
  background-color: lightyellow;
}

.storyBox img {
  width: 40%;
}

</style>
