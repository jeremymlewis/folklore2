<template>
  <div class="details">
      <div class="infoBox">
    <h1>AmericanJeremy Folklore Project</h1>
        <h3>{{this.name}}</h3>
        <img :src="require('../images/'+this.img)">
        <h4>by {{this.author}}</h4>
        <h4>Country of Origin: {{this.country}}</h4>
        </div>
        <div class="storyBox">
        <h5>My Story:</h5>
        <p>{{this.text}}</p>
        </div>
  </div>
</template>

<script>
export default {
  name: 'Details',
  data() {
    return {
        name: "",
        img: "default",
        text: "",
        author: "",
        country: "",
    }
   },
  beforeMount() {
      this.setName();
    },
  computed: {
  stories() {
    return this.$root.$data.stories;
  }
  },

  methods: {
      setName() {
        this.name = localStorage.getItem("name");
        this.$root.$data.stories.forEach(story=> {
           console.log(story.name)
           if (story.name == this.name) {
                this.img = story.image
                this.author = story.author
                this.text = story.text
                this.country = story.country
            } 
        });   
      }
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
.infoBox {
  margin-left: 10%;
  margin-right: 10%;
  margin-top: 1%;
  width: 80%;
  border: 3px black solid;
  background-color: lightyellow;
}

h2 {
  background-color: lightyellow;
}

.storyBox img {
  width: 40%;
}

</style>