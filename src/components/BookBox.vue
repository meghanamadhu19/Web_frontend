<template>
   
    
    <div v-for="product in store" :key="product.id" >
       <SingleBook :product=product />

    </div>

</template>
<script>
import SingleBook from './SingleBook.vue'

export default {
    name: 'BookBox',
    props:{
        store: Array
    },
    components:{
        SingleBook
    }
    
}
</script>
<style scoped>

</style>
