<template>
    <div class="restaurant-row">
        <h2>Nos restaurants</h2>
    <div class="wrapper-card">
        <restaurant-card v-for="(card,index) in 3" :key="index"/>
    </div>
        
    </div>
</template>

<script>
import RestaurantCard from './RestaurantCard.vue';

export default{
    name: "RestaurantRow",
    components: {
        RestaurantCard,
    },

}
</script>

<style scoped lang='scss'>
    .restaurant-row{
        padding-bottom: 100px;
        .wrapper-card{
            display: flex;
            align-items: center;
            justify-content: space-between;
        }
    }
</style>
