<template>
   <div class="container">
      <notebook-card v-for="notebook in notebooksList" :key="notebook.id" :notebook-card-data="notebook" />
   </div>
</template>

<script>
import NotebookCard from './NotebookCard.vue'

export default {
   name: 'NotebooksPanel',

   components: {
      NotebookCard,
   },

   props: {
      notebooksList: {
         type: Array,
         default: () => [],
      },
   },
}
</script>

<style lang="css" scoped>
.container {
   display: grid;
   gap: 1.25rem 0;
}
</style>
