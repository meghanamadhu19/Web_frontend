<template>
  <MyHeader Name="Convenience Store"/>

  <BookBox :store=store  />
</template>

<script>
import MyHeader from './components/MyHeader.vue'
import BookBox from  './components/BookBox.vue'

export default {
  name: 'App',
  components: {
    // Step 2 register the component 
    MyHeader,
    BookBox
  },

  data(){
    return {
      store: []
    }
  },
  methods: {
    // promises

      async fetchproducts(){
         const res= await fetch('https://zzzz-muiv.onrender.com/api')
         const data = await res.json();
         return data[0].store;

      }

  },

  async created(){
    this.store = await this.fetchproducts()
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
  max-width: 400px;
  margin: 30px auto;
  overflow: auto;
  min-height: 300px;
  border: 0.3em solid black;
  padding: 30px;
  border-radius: 5px;
}

div{
  margin-bottom: 0.5em;

}


</style>
