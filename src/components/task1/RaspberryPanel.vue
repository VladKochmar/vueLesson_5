<template>
   <div class="rasp-container">
      <raspberry-card v-for="card in raspberryList" :key="card.id" :rasp-card-data="card" />
   </div>
</template>

<script>
import RaspberryCard from './RaspberryCard.vue'

export default {
   name: 'RaspberryPanel',

   components: {
      RaspberryCard,
   },

   props: {
      raspberryList: {
         type: Array,
         default: () => [],
      },
   },
}
</script>

<style lang="css" scoped>
.rasp-container {
   display: flex;
   flex-wrap: wrap;
   gap: 0 20px;
}
</style>
