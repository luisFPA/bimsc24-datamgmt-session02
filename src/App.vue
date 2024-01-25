<!-- the script is where the js code goes -->
<script setup>
import { ref } from "vue"; // you need this to use ref()

// Define variables and constants
let count = ref(0)
let name = ("luis")
let bcolor = (255,0,0)

// Define functions
function increment() {
  count.value++
  console.log(count.value)
}

</script>







<!-- the template is where the html code goes -->
<template>

    <div id="navbar" class="container">  
        <div id="title"> Website</div>
        <!-- <h2>Digital Tools for Cloud-based Data Management {{ name }}</h2> -->
    </div>

    
  


    <div id="flex">
        <div id="sidebar" class="container"> 
            <div id="title">Sidebar</div>
            <button @click="increment">Add one more</button>
        </div>

        <div id="main" class="container"> Main 
            <p style="margin-left: 8px"> Count is: {{ count }} </p>    
        </div>
    </div>


</template>








<!-- style is where the css code goes -->
<style scoped>
html{
    
    background-color: black; 
    color: white;
}

body{
    margin:0;
}

div{
    /* put the borders in the inside of container */
    box-sizing: border-box;
}

#navbar{
    height: 50px;
    background-color: grey;
}

#flex{
    display: flex;
    height: calc(100vh - 50px);
}

#sidebar{
    width:30%;
}

#main{
    width:70%;
    background-color: gray;
}


.container{
    border-style: dotted;
    border-color: white;
    border-width: 1px;
}
</style>