<template>

<div class="container">
<div  class="row">
 <div class="col-md-6 col-md-offset-3">
        <h1 slot="heading"> Menü </h1>
    </div>
  </div>
    <ul>
      <li> <button @click="selectedComponent= 'appCold' " class="btn-sm btn btn-primary">Cold Drink</button></li>
      <li> <button @click="selectedComponent= 'appHotDrink' " class="btn-sm btn btn-primary">Hot Drink</button></li>
      <li> <button @click="selectedComponent= 'appFood' " class="btn-sm btn btn-primary"> Food</button></li>
  </ul> 
  <component id="component" :is="selectedComponent"></component>  
</div>

</template>

<script>
import ColdVue from './Cold.vue'
import FoodVue from './Food.vue'
import HotDrinkVue from './HotDrink.vue'


  export default{ 
    data: function(){
      return {
        selectedComponent : "ColdVue"
      }
    },
    components: {
      appCold : ColdVue,
      appFood : FoodVue,
      appHotDrink :HotDrinkVue

    }

  }
</script>

<style>

  #component{
    
    position: relative;
    top: 100px;
  
  }
  div.memory{
    border: 1px 2px #edf756;
    box-shadow: 1px 1px 2px #ccc;
    padding: 20px 20px;
    margin-top: 20px;
  }

  div.row{
    color: white;
    text-align: center;
    border: 1px 2px #edf756;
    box-shadow: 1px 1px 2px #000;
    padding: 10px;
    padding-right: 20px;
  
  }
  button:hover{
    text-decoration:underline;
    color: #000;
    background-color: #d0bdf4;
    
  }
  button{
    cursor: pointer;
    border: none;
    position:relative;
   color: #a28089;
    text-align: center;
    margin:5px;
    width:75%;
    transition: all 1s;
    height: 40px;
    font-size: 25px;
  }
  button.food{
    padding-right: 30px ;
    padding-left: 30px;
  }
  
  li{
      text-decoration: none;
      list-style-type: none;
      position: relative;
      
    }
</style>
