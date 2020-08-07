<template>
  <div class="input-list">
      <input v-model="nom" class="input-list-add" type="text" placeholder="entrer le nom de la tâche">
         <button @click="send" class="btn">créer</button>
  </div>
</template>

<script>
export default {

 data() {
    return {
      nom: "",
      
    };
},
 methods: {
    send() {
      if (this.nom) {
        this.$emit("add-new-todo", {
          nom: this.nom,
         
        });
        this.nom = "";
      
      }
    },
  },
};



</script>

<style>
.input-list{
   background: skyblue;
  color: black;
  padding: 2rem;}

  .input-list-add{
    padding-top: 3px;
    width:200px;
    height: 15px;}

    .btn{height: 30px;
    width:57px;
    margin:auto;
      padding-top: 3px;
      text-align: center;
      font-size: 12px;
      }


    </style>
