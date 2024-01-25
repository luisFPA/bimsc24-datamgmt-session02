<!-- the script is where the js code goes -->
<script>
import { ref } from "vue" // you need this to use ref()


</script>








<!-- the template is where the html code goes -->
<template>
<div id="navbar" class="container">  
        <div id="title">Vue website</div>
        



        <div id="top-bar">
    <div id="title-container">
      <img class="logo-image" alt="Iaac logo" src="./assets/iaac-white.png" />
      <h2>Digital Tools for Cloud-based Data Management</h2>
    </div>
  </div>

  <div id="content">
    <!-- First example - button -->
    <!-- Here we define what function will be called when button is clicked. -->
    <button @click="increment">Add one more</button>

    <!-- Now we print the value. The syntax to print variable is {{ variable_name }}. -->
    <p style="margin-left: 8px">Count is: {{ count }}</p>

  </div>

  


        <!--
        <div id="logo">
            <img src="cow.jpg" alt="macad cow">

        </div>
        -->


    </div>

    <div id="flex">

        <div id="sidebar" class="container"> Sidebar </div>

        <div id="main" class="container"> Text input </div>
    </div>
</template>








<!-- style is where the css code goes -->
<style scoped>
html{
    background-color: rgb(59, 59, 59); 
    color: white;
}

body{
    margin:0;
}

div{
    /* put the borders in the inside of container */
    box-sizing: border-box;
}

img{
    height: 100%;
    width: auto;
}

#navbar{
    height: 50px;
    border-color: red;
}

#flex{
    display: flex;
    height: calc(100vh - 50px);
}

#sidebar{
    width:30%;
    border-color: blue;
}

#main{
    width:70%;
    border-color: green;
}

#title{
    width: 70%;
    float:left;
}

#logo{
    width: 30%;
    height: 100%;
    float:right;
    text-align: right;
}

.container{
    border-style: dotted;
    border-width: 1px;
}

</style>