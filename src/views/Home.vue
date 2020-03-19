<template>
  <div class="home">
    <!-- <img alt="Vue logo" src="../assets/logo.png"> -->
    <!-- <HelloWorld msg="Welcome to Your Vue.js App"/> -->
    
    <b-container>
  <!-- Content here -->
  
    <div >
      <b-navbar toggleable="lg" type="dark" variant="primary" class="nav">
        <b-navbar-brand href="#">Ecommerce Side</b-navbar-brand>

        <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>

        

          <!-- Right aligned nav items -->
          <b-navbar-nav class="ml-auto">
            <b-nav-form>
              <b-form-input size="sm" class="mr-sm-2" placeholder="Search"></b-form-input>
              <b-button size="sm" class="my-2 my-sm-0" type="submit">Search Items</b-button>
          </b-nav-form>

          
        <!-- </b-collapse> -->
          </b-navbar-nav>
      </b-navbar>
    </div>

 <b-row >
    <b-col sm="2" variant="primary" title="categories" >
      
      <ShopMall v-for="categoryList in categories" :user="categoryList" :key="categoryList.id"/>
      
    </b-col>
    <b-col sm="10">
      
       <b-card  title="PRODUCTS">

         <CarouSlide />
        
         <ProductItemss v-for="product in items" :mada="product" :key="product.id"/>  
      </b-card>
        
       </b-col>
  </b-row>

  
    </b-container>
  </div>
</template>

<script>
// @ is an alias to /src
// import HelloWorld from '@/components/HelloWorld.vue' 
import ShopMall from '../components/ShopMall'
import ProductItemss from '../components/ProductItemss'
import CarouSlide from '../components/CarouSlide'
export default {
  name: 'Home',

  data() {
    return {
     categories: [
       {
         categoryId: 1,
         categoryName: 'Gadgets'
       },
        {
         categoryId: 2,
         categoryName: 'Food'
       },
        {
         categoryId: 3,
         categoryName: 'Fruits'
       },
        {
         categoryId: 4,
         categoryName: 'Shoes'
       },
        {
         categoryId: 5,
         categoryName: 'Fashion'
       }
      ],
      items: [
        {
          itemId: 1,
          imageLink: require('../../src/assets/img1.jpg'),
          itemName: "phones",
          itemPrice: "$500 " 
        },
        {
          itemId: 2,
          imageLink: require('../../src/assets/img2.jpg'),
          itemName: 'phones',
          itemPrice: "$500 " 
        },
        {
          itemId: 3,
          imageLink:  require('../../src/assets/img3.jpg'),
          itemName: 'phones',
          itemPrice: " $500" 
        },
        {
          itemId: 4,
          imageLink: require('../../src/assets/img4.jpg'),
          itemName: 'phones',
          itemPrice: "$500 " 
        },
        {
          itemId: 5,
          imageLink: require('../../src/assets/img5.jpg'),
          itemName: 'phones',
          itemPrice: " $500" 
        },
        {
          itemId: 6,
          imageLink: require('../../src/assets/img6.jpg'),
          itemName: 'phones',
          itemPrice: " $500" 
        },
        {
          itemId: 7,
          imageLink: require('../../src/assets/img7.jpeg'),
          itemName: 'phones',
          itemPrice: " $500" 
        },
        {
          itemId: 8,
          imageLink: require('../../src/assets/img8.jpg'),
          itemName: 'phones',
          itemPrice: " $500" 
        },
        {
          itemId: 9,
          imageLink: require('../../src/assets/img9.png'),
          itemName: 'phones',
          itemPrice: "$500 " 
        },
        {
          itemId: 10,
          imageLink: require('../../src/assets/img10.jpg'),
          itemName: 'phones',
          itemPrice: " $500" 
        },
        {
          itemId: 11,
          imageLink: require('../../src/assets/img11.jpg'),
          itemName: 'phones',
          itemPrice: " $500" 
        },
        {
          itemId: 12,
          imageLink: require('../../src/assets/img12.jpg'),
          itemName: 'phones',
          itemPrice: " $500" 
        }
      ]
    }
  },
  components: {
    
    ShopMall,
    ProductItemss,
    CarouSlide

  }
}
</script>

<style scoped>
.nav {
  height: 7em;
  margin-top: 0;
}
</style>