<template>


  <div class="menu">
    <a v-for="(menu,i) in menus" :key="i"> {{ menu}}</a>
  </div>
  
  <div class="room">
    <a v-for="(product,i) in products" :key="i">
      {{ product }} <br>{{ prices[i] }}만원<br></a>
  </div>
  



</template>

<script>


export default {
  name: 'App',
  data(){
    return{
      menus: ['menu', 'shop' ,'about'],
      products : ['역삼동원룸', '천호동원룸', '마포구원룸'],
      prices: [70,60,50 ]
    }
  },
  components: {
   
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;

}

.menu{

  background: darkslateblue;
  padding: 15;
  border-radius: 5px;

}

.menu a {
  color: white;
  padding: 10px;
}

.room{
  background: yellowgreen;
  margin: 15px;

}
</style>
