<template>
  <div class="home">
    <img class="logo" alt="Vue logo" src="../assets/logo.png" />
    <HelloWorld msg="My TodoList" />
    
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from "@/components/HelloWorld.vue";

export default {
  name: "Home",
  components: {
    HelloWorld
  }
};
</script>

<style >
.logo{width: 200px;
height: 200px;
padding-bottom: 100px;
}
</style>
