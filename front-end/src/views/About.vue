<template>
  <div class="about">
    <h1>AmericanJeremy Folklore Project</h1>
    <p>We are trying to gather as many stories as possible and share them with the world!</p>
    <p>Since 2021 we have been gathering and publishing personal stories and folklore.</p>
    <p>Send us your own stories:</p>
    <textarea v-model="message" placeholder="Type your story here..."></textarea>
  <br>
  <p>Be sure to include your name, a title, and tell us all about what happened!</p>
  <button>Submit</button>
  </div>
</template>

<script>
export default {
  name: 'About',
  components: {
  },
}
</script>


<style>
.about {
  margin-left: 10%;
  margin-right: 10%;
  margin-top: 1%;
  width: 80%;
  border: 3px black solid;
  background-color: lightsteelblue;
}



.storyBox img {
  width: 40%;
}

</style>