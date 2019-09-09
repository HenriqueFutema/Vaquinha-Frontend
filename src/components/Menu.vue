<template>
  <div>
    <v-app-bar dark app>
      <v-toolbar-title class="headline text-uppercase">
        <router-link id="link" to="/">Vaquinha</router-link>
      </v-toolbar-title>
      <v-spacer></v-spacer>
      <v-btn text to="/signin" v-if="!getIsLogged">Entrar</v-btn>
      <v-btn light to="/signup" v-if="!getIsLogged">Criar Conta</v-btn>
      <v-btn light to="/signup" v-if="getIsLogged">Sair</v-btn>
      <v-btn text to="/">Contato</v-btn>
    </v-app-bar>
  </div>
</template>

<style scoped>
#link {
  text-decoration: none;
  color: white;
}
</style>

<script>
import { mapGetters } from "vuex";

export default {
  computed: {
    ...mapGetters(["getIsLogged"])
  }
};
</script>
