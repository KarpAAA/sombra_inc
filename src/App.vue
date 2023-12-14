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
import vitalii from "@/assets/vitalii.jpg";
import olenaaa from "@/assets/olenaaa.jpg";
import volodymyr from "@/assets/volodymyr.jpg";
export default {
  name: "app",
  components: { Character_component },
  data() {
    return {
      characters: [
        {
          name: "Vitalii",
          role: "Project Manager",
          image: vitalii,
          salary: 15000,
        },
        {
          name: "Ivan",
          role: "Fullstack developer",
          image: ivan,
          salary: 100000,
        },
        {
          name: "Olena",
          role: "Back-end developer",
          image: olenaaa,
          salary: 1e4,
        },
        {
          name: "Volodymyr",
          role: "UI/UX Designer",
          image: volodymyr,
          salary: 12000,
        },
        {
          name: "Volodymyr",
          role: "UI/UX Designer",
          salary: 12000,
        },
      ],
    };
  },
};
</script>
<style scoped>
.character {
  width: 47%;
  margin: 15px;
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
