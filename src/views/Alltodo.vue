<template>
  <div>
 
    <p>ma liste venant de la bdd...</p>
   
    <hr />
   <TasksList />
  </div>
</template>

<script>
import TasksList from "@/components/TasksList";

export default {
  name: "Alltodo",
  components: {
    TasksList,
  }
};
</script>
