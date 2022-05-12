<template>
    <body>
    <div class="home">
        <restaurant-row/>
        <restaurant-row/>
        <restaurant-row/>
        
        <br>
        <button @click="open = true">Open Modal</button>
    </div>

    <Teleport to="div">
        <div v-if="open" class="modal">
        <p>Hello from the modal!</p>
        <button @click="open = false">Close</button>
        </div>
    </Teleport>

    </body>

</template>

<script>
import RestaurantRow from '../components/RestaurantRow.vue';
import { ref } from 'vue'


export default {
    name: "home",
    components: {
        RestaurantRow, 
    },

    setup(){
        const count = ref(0)
        return{
            count
        }
    },



    /*setup() {
        class Restaurant {
            constructor (name, note, drive_time){
                this.name= name,
                this.note = note,
                this.drive_time = drive_time
            }
        };

        let data_restaurant= [];

        const make_data_restaurant = () => {
            let three_restaurant = [];
    
            for (const restaurant of restaurants ){
                const new_restaurant = new Restaurant (restaurant.name, restaurant.note, restaurant.drive_time)
                if (three_restaurant.lenght === 2){
                    three_restaurant.push(new_restaurant);
                    data_restaurant.push(three_restaurant);
                    three_restaurant = [];
                } else {
                    three_restaurant.push(new_restaurant);
                }
            }
            console.log(data_restaurant);  
        } 
        make_data_restaurant();

    }*/
}
</script>
