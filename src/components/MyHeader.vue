<template>
<div>
    <h1> {{Name}} </h1>
</div>
</template>

<script>

export default{ // Exporting Default Object
    name: 'MyHeader',
    props:{ 

        Name:String
        
    }
}

</script>

<style scoped>

div{
    text-align: center;
    height: 70px;
}

</style>