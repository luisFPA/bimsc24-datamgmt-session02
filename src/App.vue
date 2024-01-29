<!-- the script is where the js code goes -->
<script setup>
    import { ref } from "vue"; // you need this to use ref()

    // Define variables and constants
    let count = ref(1)
    let pNumber = ref(1)

    let name = ref("Luis")
    //const message = ref('')

    /* Define functions
    function increment() {
    count.value++
    console.log(count.value)
    }
    */

    function fSequence() {
    count.value = count.value + pNumber.value
    console.log(count.value)

    pNumber.value = count.value
    }


    function fReset() {
    count.value = 1
    pNumber.value = 1
    console.log(count.value)
    }



</script>







<!-- the template is where the html code goes -->
<template>

    <div id="navbar" class="container">  
        <div id="title" class="smallNum"> Website by {{ name }}</div>
         <h2>Number Sequence</h2>
    </div>


    <div id="flex">
        <div id="sidebar" class="container"> 
            <div id="title" class="smallNum">Sidebar</div>
            <button @click="fSequence">Add to sequence</button>
            <button @click="fReset">Reset</button>
            
            <input v-model= message placeholder="Guess the next number" />
            <!--<button @click="sendText">Send text</button> -->
        </div>

        <div id="main" class="container"> 
            <div id="title" class="smallNum">Main</div>

            <p>Message is: {{ message }}</p> 
            <p> <strong>THE NUMBER IS:</strong></p>
            <p class="hugeNum">{{ count }}</p>   
        </div>
    </div>


</template>








<!-- style is where the css code goes -->
<style scoped>
    html{
        
        background-color: red; 
        color: black;
    }

    body{
        margin:0;
    }

    div{
        /* put the borders in the inside of container */
        box-sizing: border-box;
        color: rgb(0, 255, 0);
        font-family: Helvetica;
        font-size: 15px;
        background-color: black; 
    }

    #navbar{
        height: 100px;
        
    }

    #flex{
        display: flex;
        height: calc(100vh - 50px);
    }

    #sidebar{
        width:20%;
        
    }

    #main{
        width:80%;
        color: whitesmoke;
    }


    .container{
        border-style: dotted;
        border-color: white;
        border-width: 1px;
    }


    .hugeNum{
        font-size: 300px;
        position: relative;
        min-height: 100%;
        text-align:start;
    }

    .smallNum{
        font-size: 10px;
    }
</style>