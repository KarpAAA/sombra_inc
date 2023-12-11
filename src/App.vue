<template>

  <div class="main">
    <div class="charactersContainer">
      <div v-for="c in characters" class="character">
        <character_component :character="c"></character_component>
      </div>
    </div>
  </div>


</template>

<script>
import Character_component from "@/components/CharacterComponent.vue";
import ivan from "@/assets/ivan.jpg";
export default {
  name: "app",
  components: {Character_component},
  data(){
    return {
      characters: [
        {
          name: "Ivan",
          role: "Fullstack developer",
          image: ivan,
          salary: 10000
        }
      ]
    }
  },
}
</script>
<style scoped>
.character{
  width: 47%;
  margin: 15px
}
.charactersContainer {
  margin-top: 65px;
  width: 75%;
  display: flex;
  flex-wrap: wrap;
}
.main {
  display: flex;
  justify-content: center;
}
</style>
