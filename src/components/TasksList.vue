<template>
    <ul class="tasklists">
      <li class="tasklist" v-if="!tasklists.length">...loading</li>
    <li v-for="(tasklist, i) in tasklists" :key="i" class="tasklist">
      console.log('')
      <p>{{tasklist.nom }} </p>
      <p>
        <router-link class="link" :to="'/home' + tasklist._id"
          >see details...
        </router-link>
      </p>
    </li>
  </ul>
</template>

<script>
import axios from "axios";

export default {
  data() {
    return {
      tasklists: []
    };
  },
  methods: {
    async gettasklists() {
      const apiRes = await axios.get(
        process.env.VUE_APP_BACKEND_URL + "/tasks"
      );
      this.tasklists = apiRes.data;
      console.log(apiRes.data)// axios retourne TJS les results sous la clé data
    }
  },
  created() {
    try {
      this.gettasklists();
    } catch (err) {
      console.error(err);
    }
  }
};
</script>

<style scoped>
.tasklists {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
  grid-gap: 20px;
  grid-auto-rows: 100px;
}
.tasklist {
  
  border-radius: 0.3rem;
  list-style: none;
  padding: 20px;
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
}
</style>
