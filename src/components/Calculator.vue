<template>
    <div class="calc">
        <div class="display"><h5>{{result || 0}}</h5>
        </div>

        <div>
            <button class="operator" @click="del" >DEL</button>
            <button class="operator" @click="clear">AC</button>
            <button class="operator" @click="percentage">%</button>
            <button class="operator" @click="appendToExpression('/')">/</button>
        </div>
         <div>
            <button @click="appendToExpression('7')">7</button>
            <button @click="appendToExpression('8')">8</button>
            <button @click="appendToExpression('9')">9</button>
            <button class="operator" @click="appendToExpression('*')">x</button>
        </div>
         <div>
            <button @click="appendToExpression('4')">4</button>
            <button @click="appendToExpression('5')">5</button>
            <button @click="appendToExpression('6')">6</button>
            <button class="operator" @click="appendToExpression('-')">-</button>
        </div>
         <div>
            <button @click="appendToExpression('1')">1</button>
            <button @click="appendToExpression('2')">2</button>
            <button @click="appendToExpression('3')">3</button>
            <button class="operator" @click="appendToExpression('+')">+</button>
        </div>
         <div>
            <button @click="appendToExpression('00')">00</button>
            <button @click="appendToExpression('0')">0</button>
            <button @click="dot">.</button>
            <button class="equal_btn" @click="calculateResult">=</button>
        </div>
    </div>
</template>
<script>
    export default{
        data(){
            return{
                result: "",
            }
        },
        methods:{
            appendToExpression(value){
                this.result += value
            },
            
            clear(){
                this.result = ""
            },
            dot(){
                if(this.result.indexOf('.') === -1){
                    this.appendToExpression('.')
                }
            },
            del(){
                this.result = this.result.slice(0, -1)
            },
            percentage(){
                this.result = parseFloat(this.result)/100
            },
        calculateResult() {
          try {
            this.result = eval(this.result);
          } catch (error) {
            this.result = 'Math Error';
          }
              
        },
        
    }
}
</script>

<style scoped>
    .calc{
        border: 1px solid #717377;
        padding: 20px;
        border-radius: 16px;
        background: transparent;
        box-shadow: 0px 3px 15px rgba(113, 115, 119, 0.5);
    }
    .display{
        color: #ffffff;
        width: 320px;
        border: none;
        padding: 24px;
        margin: 10px;
        background: transparent;
        box-shadow: 0px 3px 15px rgba(84, 84, 84, 2);
        text-align:right;
        cursor: pointer;
    }
    h5{
        overflow: hidden;
        font-size: 40px;
    }
    button{
        border: none;
        width: 60px;
        height: 60px;
        margin: 10px;
        border-radius: 50%;
        background: transparent;
        color: #ffffff;
        font-size: 20px;
        box-shadow: -8px -8px 15px rgba(255, 255, 255, 0.1);
        cursor: pointer;
    }
    button:active{
        background: #717377;
    }
    .equal_btn{
        background-color:#fb6c14;
    }
    .equal_btn:active{
        background: #191e24;
        color:#ffffff;
    }
    .operator{
        color: #6dee0a;
    }
   
</style>