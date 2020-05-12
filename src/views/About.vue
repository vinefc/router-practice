<template>
  <div class="home">
    <h1>8 classic children's books</h1>
    <br/>
    <div id="allbooks">
    <router-link to="/" ><h2>{{book.title}}</h2> <p>{{book.author}}</p> <br/> <p>{{book.plot}}</p></router-link>
    </div>

  
  </div>
</template>

<script>
// @ is an alias to /src

import books from "../assets/books.json"

export default {
  name: 'Home',
  components: {
   
  },
  data(){
    return{
      book : books.books.find(b => b.id ===this.$route.params.id)
    }
  },

  created(){
    console.log('id');
    console.log( this.$route.params.id );
    
  }
}
</script>

<style scoped>

h1 {
  margin: 0px;
  padding: 0px;
  text-align:left;
}

.home {
  box-sizing: border-box;
  height: 100%;
  width: 70%;
  display: flex;
  flex-direction: column;
  justify-content: flex-start;
}

#allbooks{
  margin: 0;
  padding: 0;
  position: relative;
  box-sizing: border-box;
  height: 100%;
  width: 100%;
  display:flex;
  flex-direction: row;
  flex-wrap: wrap;
  justify-content: space-between;
}

#cover{
  display: flex;
  flex-direction: column;
  position: relative;
  box-sizing: border-box;
  height: 300px;
  width: 250px;
  border: solid 1px;
  margin-bottom: 10px;
  padding: 0;
  background-color: red;
}


</style>