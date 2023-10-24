<template>
   <h2>Завдання №1</h2>
   <raspberry-panel :raspberry-list="raspberryList" />
   <h2>Завдання №2</h2>
   <notebooks-panel :notebooks-list="notebooksList" />
</template>

<script>
import RaspberryPanel from '@/components/task1/RaspberryPanel.vue'
import NotebooksPanel from '@/components/task2/NotebooksPanel.vue'

import { raspberryList } from './constants/2_data_raspberry'
import { notebooksList } from './constants/3_data_notebooks'

export default {
   name: 'App',

   components: {
      RaspberryPanel,
      NotebooksPanel,
   },

   data() {
      return {
         raspberryList,
         notebooksList,
      }
   },
}
</script>

<style></style>
