<template>

    <div>
        <h2>{{book.author}}</h2>
        <h4>Title: {{book.title}}</h4>
        <h4>Language: {{book.language}}</h4>
        <h4>Country: {{book.country}}</h4>
        <h4>Pages: {{book.pages}}</h4>
        <h4>Year: {{book.year}}</h4>
        <h4>Link: {{book.link}}</h4>
    </div>

</template>

<script>


export default{
    name: 'BookItem',
    props:{
        book: JSON
    }
}


</script>

<style scoped>


h4{
    margin: 2px;
}

div{
    background-color: #a8d4a6;
    color: black;
    padding: 1em;
    border-radius: 1em;
}

.red{
background-color: orangered !important;

}
.green{
    color: white;
}


</style>