<template>
  <div>
    <v-app-bar dark app>
      <v-toolbar-title class="headline text-uppercase">
        <router-link id="link" to="/">Vaquinha</router-link>
      </v-toolbar-title>
      <v-spacer></v-spacer>
      <v-btn text to="/signin" v-if="!getIsLogged" class="mx-2">Entrar</v-btn>
      <v-btn light to="/signup" v-if="!getIsLogged" class="mx-2">Criar Conta</v-btn>
      <v-btn light to="/perfil" v-if="getIsLogged" class="mx-2">Perfil</v-btn>
      <v-btn light v-if="getIsLogged" class="mx-2">Novo Projeto</v-btn>
      <v-btn light to="/signin" v-if="getIsLogged" @click="logoff" class="mx-2">Sair</v-btn>
      <v-btn text to="/" class="mx-2">Contato</v-btn>
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
import { mapGetters, mapMutations } from "vuex";

export default {
  computed: {
    ...mapGetters(["getIsLogged"]),
    ...mapMutations(["LOGOFF"])
  },

  methods: {
    logoff: function() {
      this.LOGOFF;
    }
  }
};
</script>
