<template>
  <section>
    <form @submit.prevent="submitData">
      <input type="text" placeholder="name" v-model="userName" />
      <input type="text" placeholder="age" v-model="userAge" />
      <button>set data</button>
    </form>
  </section>
</template>
<script>
export default {
  emits: ['add-user'],
  data() {
    return {
      userName: "",
      userAge: "",
    };
  },
  methods: {
    submitData() {
      this.$emit('add-user', this.userName, this.userAge);
    },
  },
};
</script>