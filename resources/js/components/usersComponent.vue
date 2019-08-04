<template>
  <div class="container">
    <div class="row py-4">
      <h2 class="text-center"> PARTNER AZIENDALI </h2>
      <div class="users_container d-flex justify-content-around flex-wrap p-2 border">
        <user class="mb-4"
        v-for="singolo_user in users"
        v-bind:key="singolo_user.id"
        v-bind:dati_user="singolo_user"></user>

      </div>
    </div>
  </div>
</template>

<script>
  export default {
    data:function(){
      return{
        users:[]
      }
    },
    mounted(){

      axios.get('https://jsonplaceholder.typicode.com/users').then(response=>{
        this.users=response.data;
      }).catch(error=>{
        console.log("error");
      });
    }
  }
</script>
