<template>
  <!--   <v-container>
    <v-row>
      <v-col
        v-for="personaje in personajes"
        :key="personaje.id"
        cols="12"
        md="6"
        lg="4"
      > -->
  <v-hover v-slot="{ hover }">
    <v-card
      v-ripple
      class="mx-auto card"
      max-width="344"
      :elevation="hover ? 12 : 2"
      @click="$emit('click', personaje)"
    >
      <v-img :src="personaje.imagen" height="200px"></v-img>

      <v-card-title> {{ personaje.nombre }}</v-card-title>
    </v-card>
  </v-hover>
  <!--       </v-col>
    </v-row>
  </v-container> -->
</template>

<script>
export default {
  props: {
    personaje: { type: Object, required: true },
  },
}
</script>

<style scoped>
.card {
  transition: all 0.2s linear;
  cursor: pointer;
}
</style>
