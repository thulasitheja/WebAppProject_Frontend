<template>
    <div>
        <h1 style="font-size: 50px;"> {{bookName}} </h1>
    </div>
</template>
    
    <script>
    
    export default{
        name: 'HeaderTop',
        props:{
            bookName: String,
        }
    }
    
    </script>
    
    <style scoped>
    
    div{
        text-align: center;
    }
    
    </style>