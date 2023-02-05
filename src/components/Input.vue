<template>
   <div id="input-main">
    <input type="text" id="input" name="input" v-model="dados" placeholder="Tape the Activity" >
    <button type="submit">Enter</button>
   </div>

   <div>
        
   </div>
</template>

<script>
    export default{
        name:"Input",
        data(){
            return{
                dados: null
                 
            }
        },
        methods:{
           async getData(){

           } 
        }
        
    }
      

</script>

<style scoped>

    #input-main{
        margin-top: 40px;
        width: 100%;
        height: 30px;
        align-items: center;
        display: flex;
        justify-content: center;
    }

    #input{
        font-size: 20px;
        font-family: Georgia, 'Times New Roman', Times, serif;
        border-radius: 5px;
        height: 80%;
        width: 400px;
    }

    button{
        margin-left: 30px;
        height: 100%;
        width: 80px;
        cursor:grab;
    }
</style>