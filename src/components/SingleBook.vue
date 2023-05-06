<template>
    

    <div  :class="product.In_stock ? 'black': 'white' ">

                        <h1>{{product.productname}}</h1>
                        <h2> Price : {{product.price}}</h2>
                        <h2> Exp_date : {{product.Exp_date}}</h2>
                        <h2> Quantity Available : {{product.stock_available}}</h2>
                        <h2> In Stock : {{product.In_stock}}</h2>

                       
                        
                        
    </div>
</template>

<script>

export default{
    name: 'SingleBook',
    props:{
        product: Array
    }
}
</script>

<style scoped>

.black{
    background-color: #77DD77;
}

h4{
    margin: 2px;
}

div{
    background-color: #FF6961;
    color: black;
    padding: 1em;
    text-align: center;
    width: 80%;
    margin: auto;
    border-color:black;

}

.white{
background-color: #FF6961;

}


</style>