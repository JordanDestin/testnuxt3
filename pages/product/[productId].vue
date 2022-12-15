<template>
      <div  class="p-5 flex flex-row-reverse gap-5">
      <div class="w-2/3">
        <!-- <img class="w-full" :src="'/assets/images/'+product.imageName" :alt="product.name"> -->
        image
      </div>
      <div class="w-1/3">
        
        <div class="text-sm breadcrumbs w-full break-words">
          <ul>
            <li>
              Catégorie
            </li> 
            <li>
              <!-- <NuxtLink :to="'/category/' + product.category">{{$getCategoryTitle(product.category) }}</NuxtLink> -->
            </li>
            <li>
              <span class="text-base-content/75">Ce produit</span>
            </li>
          </ul>
        </div>

        <h1 class="mt-8 text-xl font-bold">nom</h1>
       
        <p class="mt-4 text-sm font-bold">
          14 €
        </p>

        <form class="mt-8" @submit.prevent>
        
          <button class="w-full mt-4 btn" >Ajouter au panier</button> 
          <button class="w-full mt-4 btn btn-primary">Acheter maintenant</button> 
        </form>

      </div>
    </div>
</template>

<script setup>

</script>

<style lang="scss" scoped>

</style>