<template>
    <div class="bookbox">
        <div v-for="book in books" :key="book.id" >
            <BookItem :book="book"/>
        </div>

    </div>
    


</template>'

<script>

    import BookItem from './BookItem.vue'


    export default{
        name: 'BookBox',
        components: {
            BookItem
        },
        props:{
            
            books: JSON
        }
    }

</script>

<style scoped>

.bookbox{
padding: 2.5em;
color: rgb(196, 66, 66);
}

</style>