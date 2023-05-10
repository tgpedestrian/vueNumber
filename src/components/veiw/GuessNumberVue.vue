<script>
export default{
    //自訂一 ID
    data() {
        return {
            firstNum:1,
            secondNum:100,
            answer:null,
            result: 80,
            isWin: false,
            isText:'',
            istrue:true,

        }
    },
    methods: {
        
        change(){
            if(this.answer>this.firstNum&& this.answer <this.secondNum && this.answer == this.result){
    
    
        this.isWin=true;
        this.isText="恭喜答對了";
        this.istrue=false;
        
        
    }
    else if(this.answer>this.firstNum && this.answer <this.result){
        
        this.firstNum=this.answer;
       
       
        this.isText="答錯了，再試一次";
        this.istrue=true;
    }
    else if(this.answer< this.secondNum && this.answer >this.result){
        
        this.secondNum=this.answer;
        this.isText="答錯了，再試一次";
        
        
    }
    else if(this.answer<1 || this.answer >100){
        
        this.isText="請好好打字";
        

    }else{
        console.log("=========");
    }
        }



    },
}

</script>

<template>
    <div class="containerGuess">
        <h1>𝔾𝕦𝕖𝕤𝕤 𝕋𝕙𝕖 ℕ𝕦𝕞𝕓𝕖𝕣</h1>
        <h2>猜一個數字</h2>
        <div class="numGroup">
            <p v-if="istrue"><span class="number" id="firstNum">{{firstNum}}</span> 一 <span class="number" id="secondNum">{{ secondNum }}</span></p>
            <p id="result" v-if="isWin">{{ result }}</p>
            <p>{{ isText }}</p>
        </div>
        <p v-if="istrue"><input type="number" v-model="answer"></p>
    
        <button id="btnGuess" type="button" v-on:click="change" v-if="istrue">回答</button>
    </div>

</template>

<style lang="scss" scoped>

.containerGuess{
    display: flex;
    justify-content: center;
    flex-direction: column;
    align-items: center;
    background-color: #E1B3AB;
    box-shadow: #f2d2e9 2px 2px 20px 10px;
    padding: 6px;
    border-radius: 20px;


    h1{
        font-size: 60px;
        color: #AD4EF0;
    }
    h2{
        letter-spacing: 6px;
        font-size: 30px;
        color: #FAE0C8;
        -webkit-filter: drop-shadow(12px 12px 7px rgba(200, 194, 194, 0.7));
    filter: drop-shadow(12px 12px 7px rgba(0, 0, 0, 0.7))

    }
    .numGroup{
        align-items: center;
        display: flex;
        flex-direction: column;
     
        
        .number{
            font-size: 20px;
            letter-spacing: 2px;
            margin-left: 20px;
            margin-right: 20px;
    }
        

}
}

</style>
