<template>
    <div class="restaurant-card">
        <div class="restaurant-image"></div>
        <div class="restaurant-information">
            <div class="top">
                <p class="name">Subway</p>
                <p class="note">4/5</p>
            </div>
            <p class="time">20min</p>
        </div> 
        <button @click="count++">Commander: <br>{{ count }}</button> 
        <button @click="count--" class="annul">Annuler</button>
    </div>
</template>

<script>

export default{
    name: "RestaurantCard",

    
    }


</script>

<style scoped lang="scss">
.restaurant-card{
    width: 32%;
    height: 30vh;
    padding-bottom: 50px;
    .restaurant-image{
        background-color: wheat;
        //background-image: url('sandwich.jpg');
        height: 70%;
        background-size: cover;
        background-position: center;
    }
    .restaurant-information{
        .top{
            display: flex;
            align-items: center;
            justify-content: space-between;
            .note{
                background-color: #eeeeee;
                display: flex;
                justify-content: center;
                width: 30px;
                border-radius: 50%;
            }
        }
    }.annul{
        display: flex;
        justify-content: flex-end;
    }
}
</style>
