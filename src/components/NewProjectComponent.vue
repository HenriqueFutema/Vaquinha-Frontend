<template>
  <h1>Novo Projeto</h1>
</template>

<script>
import { mapGetters } from "vuex";

export default {
  computed: {
    ...mapGetters(["getIsLogged"])
  },

  created: function() {
    if (!this.getIsLogged) {
      return this.$router.push("/signin");
    }
  }
};
</script>

<style>
</style>