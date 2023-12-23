<template>
<input v-model="msg" type="text"><br><br>
<input v-model="msg1" type="text"><br><br>
<button @click="change">поменять местами</button><br><br>
<hr>
<input v-model="user" type="text">
<p>{{ surname }}</p>
<p>{{ name }}</p>
<p>{{ ochestvo }}</p>
<button @click="vivod">вывести</button>
</template>
    
<script>
    export default {
      data(){
        return{
          msg: '',
          msg1: '',
          res: '',
          res1: '',
          user: '',
          surname: '',
          name: '',
          ochestvo: '',
        }
      },
      methods: {
        change(){
          this.res = this.msg
          this.res1 = this.msg1
          this.msg = this.res1
          this.msg1 = this.res
        },
        vivod(){
          const users = this.user.split(" ")
          this.surname = users[0];
          this.name = users[1];
          this.ochestvo = users[2];
        }
      }
    }
</script>

<style>

</style>
    
