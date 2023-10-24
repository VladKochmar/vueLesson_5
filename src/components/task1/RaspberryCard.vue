<template>
   <div class="card">
      <img class="card__image" :src="raspCardData.imgSrc" :alt="raspCardData.description" />
      <div class="card__info">
         <img :src="raspCardData.logo" :alt="raspCardData.companyTitle" class="card__icon" />
         <h2 class="card__company">{{ raspCardData.companyTitle }}</h2>
      </div>
      <p class="card__text">{{ raspCardData.description }}</p>
   </div>
</template>

<script>
export default {
   name: 'RaspberryCard',

   props: {
      raspCardData: {
         type: Object,
         default: () => ({}),
      },
   },
}
</script>

<style lang="css" scoped>
.card {
   max-width: 320px;
   width: 100%;
   padding: 10px;
   border: 2px solid green;
}
.card__image {
   border-radius: 20px;
   max-width: 100%;
}
.card__info {
   display: flex;
   align-items: center;
   gap: 0 5px;
}
.card__info:not(:last-child) {
   margin-bottom: 10px;
}
.card__company {
   font-size: 14px;
}
.card__text {
   font-weight: 700;
   font-size: 18px;
   color: #424242;
   line-height: 1.5;
}
</style>
