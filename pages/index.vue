<template>
  <v-container>
    <v-row>
      <v-col
        cols="12"
        sm="6"
        lg="4"
        v-for="personaje in $store.state.personajes"
        :key="personaje.id"
      >
        <CharacterCard
          :personaje="personaje"
          @click="$router.push({ path: `/detalle/${$event.id}` })"
        />
      </v-col>
    </v-row>
  </v-container>
</template>
<script>
import CharacterCard from '../components/CharacterCard.vue'
export default {
  components: { CharacterCard },
}
</script>
