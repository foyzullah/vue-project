<template>
    <div class="container mx-auto">
      <h2 class="text-lg font-bold text-center py-5">Meal Categories</h2>
      <div class="flex flex-wrap mx-auto justify-center">
      <div v-for="meal in meals" class="border border-orange-300 rounded-sm p-4 mb-5 text-center h-full w-1/4 mr-2">
        <img :src="meal.strCategoryThumb" alt="">
        <h3 class="font-semibold mt-3">{{ meal.strCategory }}</h3>
      </div>
    </div>
    </div>
  </template>
  
  <script>
    export default{
  
      name: 'Home',
      data(){
        return {
         meals:[] 
        }
      },
      mounted(){
        fetch('https://www.themealdb.com/api/json/v1/1/categories.php')
        .then(response=> response.json())
        .then(json=>this.meals=json.categories)
      }
    }
  
  </script>