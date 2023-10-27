<template>
<div id="app">
    <Heading/>
    <Calculator/> 
</div>  
</template>
<script>
import Heading from './components/Heading.vue';
import Calculator from './components/Calculator.vue';
export default{
  name: 'apps',
  components:{
    Heading,
     Calculator,
   
  }
}
</script>

<style>
 *{
        margin: 0;
        padding:0;
        box-sizing: border-box;
        font-family: sans-serif;
    }
    body{
        width: 100%;
        height: 100vh;
        display: flex;
        justify-content: center;
        align-items: center;
        background: linear-gradient(45deg, #0a0a0a, #3a4452);
    }
    #app{
      display: grid;
      grid-template-columns: auto auto;
      justify-content: space-between;
      align-content: center;
    }
    .weather-btn
    {
      width: 100px;
      height: 50px;
      background: transparent;
      font-size: 20px;
      border-radius: 10px;
      margin: 30px;
      font-family: sans-serif;
      color: #6dee0a;
      box-shadow: -8px -8px 15px rgba(255, 255, 255, 0.1);
      
    } 
   
</style>