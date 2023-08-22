<script>
  import axios from 'axios';

  
  export default {
    data() {
      return {
        projects:[],
      }
    },
    methods: {
      functiontest() {
        axios.get('http://127.0.0.1:8000/api/api')
        // .then(function (response) {   
        //   const data = response.data.result;          
        //   this.projects = data;
        //   console.log(this.projects);
        // })
        .then(
          (response) => {
            const data = response.data.result;          
            this.projects = data;
            console.log(this.projects);
          }
        )
        .catch(function (error) {
          console.error(error);
        });

      }
    },
    mounted() {
      this.functiontest();
      
    }
  }
  
</script>

<template>

  <div
    v-for="project in projects"
  >
    {{ project.name_project }}
  </div>
hello
</template>

<style scoped>

</style>
