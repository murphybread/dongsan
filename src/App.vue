<template>


  <div class="menu">
    <a v-for="(menu,i) in menus" :key="i"> {{ menu}}</a>
  </div>
  
  <div class="room">
    
    <a v-for="(product, i) in products" :key="i" class="product-item">
      <img class="room-img" v-bind:src="images[i]" /> <br>
      <span class="product-name">{{ product }}    </span>   <span class="product-price">{{ prices[i] }}</span>만원
    <br><button @click="increase(i)"> 신고버튼</button> <span>{{ reports[i] }}</span>
    </a>
    </div>
  


    

</template>

<script>


export default {
  name: 'App',
  data(){
    return{
      reports: [0,0,0],
      menus: ['menu', 'shop' ,'about'],
      products : ['역삼동원룸', '천호동원룸', '마포구원룸'],
      prices: [70,60,50 ],
      images : [require("./assets/room0.jpg"), require("./assets/room1.jpg") , require("./assets/room2.jpg")]
    }
  },
  methods: {
    increase(num){
      this.reports[num] +=1 
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

.room a {
  display: block;
  margin-bottom: 10px; /* 각 a 태그 아래에 마진을 적용 */
  border: solid;
}

.room-img{

  margin-top: 40px;
}

.product-name {
  font-weight: bold;
  font-size: 20px;
}
.product-price {
  font-weight: bold;
  color: orangered;
}
</style>
