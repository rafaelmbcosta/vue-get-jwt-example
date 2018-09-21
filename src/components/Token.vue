<template lang="html">
  <div>
    <h2> Testando Token </h2>
    <p v-if="token"> {{ token }} </p>
    <button @click="setToken"> Setar Token</button>
  </div>
</template>

<script>
import axios from 'axios';

export default {
  data: function(){
    return{
      token: null
    }
  },
  methods: {
    setToken(){
      axios.post('http://localhost:3000/user_token', {
        auth: {
          email: 'nome@email.com',
          password: '123456'
        }
      })
      .then(response => {
        this.token = response.data.jwt
      })
      .catch(error => {
        this.token = 'Erro ao recuperar token'
      })
    }
  }
}
</script>

<style lang="css">
</style>
