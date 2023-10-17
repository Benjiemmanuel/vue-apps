<template>
<div class="overall-container">
    <div class="container">
        <input type="text" placeholder="USA"> 
        <h1>Feels Like 22</h1>
        <div>
            <div class="weather-display"><h2>22</h2></div>
        </div>
        <h1>Broken Clouds</h1> 
          <div class="line"></div>
        <div class="weather-reading">
            <span>4.49</span>
            <span>%37</span>
            <span>%66</span>
        </div>
    </div>
    </div>
</template>
<style scoped>
*{
    padding: 0;
    margin: 0;
}
.overall-container{
    padding: 0;
    margin: 0;
    background: gray;
    width:1000px;
    height: 100vh;
    justify-content: center;
    align-items: center;
    display: flex;
}
    .container{
        background-color:whitesmoke;
        padding: 10px;
        width: 290px;
        height: 70vh;
        border: none;
        border-radius: 16px;
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
    }
    input{
        width: 90%;
        height: 40px;
        border: 2px light rgb(104, 103, 103);
        border-radius: 20px;
        background:transparent ;
        outline: none;
    }
    .line {
     width: 100%;
     height: 2px;
     background-color: rgb(235, 232, 232); 
       
    }

    h1{
        font-size: 15px;
        color:gray;
        font-family: sans-serif;
        text-align: center;
        padding: 40px;
    }
    .weather-display{
        width: 120px;
        background:transparent;
        height: 120px;
        border-radius: 50%;
         box-shadow: 0px 3px 35px gray;
    }
    .weather-reading{
        color: gray;
        display: flex;
        flex-direction: row;
        gap: 55px;
        box-sizing: border-box;
        padding-top: 20px;
    }
    h2{
        font-size: 70px;
        color:#000;
        text-align: center;
        padding-top: 1px;
        font-weight: bolder;
        font-family: 'Times New Roman', Times, serif;
    }
    ::placeholder{
        padding-left: 20px;
    }
</style>