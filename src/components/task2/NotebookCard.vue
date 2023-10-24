<template>
   <div class="card">
      <a :href="notebookCardData.link" class="card__image">
         <img :src="notebookCardData.imgSrc" :alt="notebookCardData.title" />
      </a>
      <div>
         <a :href="notebookCardData.link" class="card__title">{{ notebookCardData.title }}</a>
         <div class="card__discount">
            Ваша економія: <span>{{ notebookCardData.discount }}</span>
         </div>
         <div class="card__old-price">{{ notebookCardData.oldPrice }}</div>
         <div class="card__info">
            <div class="card__price">{{ notebookCardData.price }}</div>
            <button type="button" class="button">Купити</button>
         </div>
      </div>
   </div>
</template>

<script>
export default {
   name: 'NotebookCard',

   props: {
      notebookCardData: {
         type: Object,
         default: () => ({}),
      },
   },
}
</script>

<style lang="css" scoped>
.card {
   display: flex;
   gap: 0 20px;
   padding: 0.625rem 1.25rem;
   border: 2px solid green;
}
.card__image {
   flex: 0 1 180px;
}
.card__image img {
   max-width: 100%;
}

.card__title {
   color: green;
   font-size: 1.25rem;
   font-weight: 500;
   line-height: 1.5;
   transition: color 0.3s ease 0s;
}
.card__title:hover {
   color: purple;
}
.card__title:not(:last-child) {
   margin-bottom: 16px;
}
.card__discount {
   font-size: 0.75rem;
}
.card__discount span {
   color: red;
}
.card__old-price {
   color: gray;
   line-height: 1.5;
   font-size: 1.125rem;
   text-decoration: line-through;
}
.card__info {
   display: flex;
   justify-content: space-between;
}
.card__price {
   color: red;
   font-size: 2rem;
}
.button {
   border: none;
   color: #fff;
   border-radius: 0.3125rem;
   background-color: green;
   padding: 0.3125rem 1.25rem;
   transition: background 0.3s ease 0s;
}
.button:hover {
   background-color: greenyellow;
}
</style>
