<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
 
       
  </div>
</template>

<script>
export default {
  name: "HelloWorld",
  props: {
    msg: String
  }
};
</script>


}
<style>
.hello{background: whitesmoke;
box-shadow: 30px 30px 25px black;
border: 1px solid black;
width: 100vh;
height: 800px;
margin: auto;}
</style>
