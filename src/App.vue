<script>
  import axios from 'axios';

  axios.get('http://127.0.0.1:8000/api/api')
  .then(function (response) {                  
    console.log(response.data);
  })
  .catch(function (error) {
    console.error(error);
  });
  
</script>

<template>

</template>

<style scoped>

</style>
