<template>
  <div class="hello">
    <div class="contenaire">
<Input />
  <UserInput @add-new-todo="pushNewTodo" />
    </div>
    <!-- <h1>{{ msg }}</h1> -->
 
       
  </div>
</template>


<script>
import Input from "@/components/Input";

  
export default {
  components: { Input },
  name: "HelloWorld",
  props: {
    msg: String
  },
 data() {
    return {
      noms: [ {nom: "faire mon api"},],
    };
  },
  
   methods: {
    pushNewTodo(i) {
      console.log("i");
      this.noms.push(i);
    },
   
  },
};


</script>


}
<style>
.hello{
margin: auto;
display: flex;}

.contenaire{
  background: whitesmoke;
box-shadow: 30px 30px 25px black;
border: 1px solid black;
width: 100vh;
height: 800px;
margin:auto
}
</style>
