<template>
  <div class="character1">
    <div>
      <div :style='{backgroundImage:`url(${this.character.image})`, width: "200px", height: "200px", borderRadius: "15px" }'>
      </div>
    </div>

    <div class="info">
      <div>Position: {{ this.character.role }}</div>
      <div>Name: {{ this.character.name }}</div>
      <div>Salary: {{ this.character.salary }} $</div>
    </div>



  </div>
</template>

<script>
export default {
  name: "character_component",
  data() {
    return {
      some: String
    }
  },
  props: {
    character: {
      name: String,
      role: String,
      image: String,
      salary: Number,
      required: true
    }
  }
}
</script>

<style scoped>
.info{
  padding-left: 30px;
  margin-top: 14%;
  font-size: 18px;
}
.character1 {
  display: flex;
  flex-wrap: wrap;
  padding: 30px;
  border-radius: 15px;
  border: 1px solid grey;
  color: black;
  font-size: 20px;
  background-color: white;
}
</style>