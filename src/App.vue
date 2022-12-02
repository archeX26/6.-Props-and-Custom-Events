<template>
  <section>
    <active-user :username='user.name' :userage='user.age'> </active-user>
    <user-data @add-user="addUserData"></user-data>
  </section>
</template>

<script>
export default {
    data(){
        return{
            user:{
                name:'giorgi',
                age: 20,
            }
            
        }
    },
    methods:{
        addUserData(name,age) {
      this.user={
        name: name,
        age: age
      }
      
    },

    }
};
</script>
<style>
html {
  font-family: sans-serif;
}

section {
  margin: 2rem auto;
  max-width: 40rem;
  border-radius: 12px;
  border: 1px solid #ccc;
  padding: 1rem;
}

</style>