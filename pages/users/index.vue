<template>
  <div>
    <h2>hello user</h2>
    <input type="text" v-model="id">
    <button @click="loadUser">ユーザーをロードする</button>
  </div>
</template>


<script>
  export default {
    data(){
      return {
        id: ''
      }
    },
    methods: {
      loadUser(){
        this.$router.push(`/users/${this.id}`)
      }
    }
  }
</script>
