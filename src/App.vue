
<template>
  <div class="container">
    <HeaderTop bookName="Authors and Books"/>

    <BookBox :books="books" />

</div>
</template>

<script>
import axios from "axios";
import HeaderTop from './components/HeaderTop.vue'
import BookBox from './components/BookBox.vue'

export default {
  name: 'App',
  components: {    
    HeaderTop,
    BookBox
  },

  data(){
    return {
      books: []
    }

  },

  methods: {

    // promises

      async fetchBooks(){
          //const res = await fetch('https://thulasi-backend.azurewebsites.net/api')
          //const data = await res.json()
          // console.log( data )
          // return data
          axios.get('/api').then((response) =>{
            this.books = response.data;
            console.log('response');
          })
          .catch((error)=>{
            console.log(error)
          })
      }


  },
  async created(){
    this.books = await this.fetchBooks()
    console.log(this.books);
  }
}

</script>

<style>

@import url('https://fonts.googleapis.com/css2?family=Montserrat:wght@300&display=swap');
* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}

body {
  font-family: 'Montserrat', sans-serif;
}
.container {
  background-image: url('/public/books.jpg');
  max-width: 700px;
  margin: 30px auto;
  overflow: auto;
  min-height: 300px;
  border: 0.3em solid black;
  padding: 30px;
  border-radius: 5px;
  font-size: 20px;
}

div{
  margin-bottom: 0.5em;
}

</style>
