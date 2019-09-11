<template>
  <v-container>
    <v-layout>
      <v-flex xs12 md12 class="mx-1">
        <v-card class="px-5 py-3">
          <v-card-title>
            <v-avatar size="150">
              <img src="https://vuetifyjs.com/apple-touch-icon-180x180.png" alt="avatar" />
            </v-avatar>
            <v-flex xs-12 md-8>
              <h1 class="font-weight-thin display-2 mb-5 ml-5 text-left">Henrique Futema</h1>
              <h1 class="font-weight-thin display-1 mb-5 ml-5 text-left">henrique.futema01@gmail.com</h1>
              <p class="font-weight-thin body-2 ml-5 text-left">
                <v-icon class="mr-1">mdi-star-outline</v-icon>5.0 / 5.0
              </p>
            </v-flex>
            <v-flex>
              <v-btn color="red darken-1">Alterar Perfil</v-btn>
            </v-flex>
          </v-card-title>
        </v-card>
      </v-flex>
    </v-layout>

    <v-layout row wrap>
      <v-flex xs12 md6 class="mt-5">
        <v-card class="mx-4 px-3 py-3">
          <v-card-title>
            <h1 class="font-weight-thin display-1 mb-5 text-left">
              <v-icon class="mr-2" color="red darken-1">mdi-cash-multiple</v-icon>Dados Bancários
            </h1>
          </v-card-title>
          <v-card-text>
            <v-form>
              <v-layout row wrap>
                <v-flex xs12 md5 class="mx-5">
                  <v-text-field label="Número do Cartão"></v-text-field>
                </v-flex>
                <v-flex xs12 md5>
                  <v-text-field label="Número do Cartão"></v-text-field>
                </v-flex>
                <v-flex xs12 md5 class="mx-5">
                  <v-text-field label="Número do Cartão"></v-text-field>
                </v-flex>
                <v-flex xs12 md5>
                  <v-text-field label="Número do Cartão"></v-text-field>
                </v-flex>

                <v-flex xs12 md5 class="mx-5">
                  <v-text-field label="Número do Cartão"></v-text-field>
                </v-flex>
                <v-flex xs12 md5>
                  <v-btn class="float-right mt-5" disabled color="red darken-1">Salvar</v-btn>
                </v-flex>
              </v-layout>
            </v-form>
          </v-card-text>
        </v-card>
      </v-flex>

      <v-flex xs12 md6 class="mt-5">
        <v-card class="mx-4 px-3 py-3">
          <v-card-title>
            <h1 class="font-weight-thin display-1 mb-5 text-left">
              <v-icon class="mr-2" color="red darken-1">mdi-home-city-outline</v-icon>Endereço
            </h1>
          </v-card-title>
          <v-card-text>
            <v-form>
              <v-layout row wrap>
                <v-flex xs12 md5 class="mx-5">
                  <v-text-field label="Bairro"></v-text-field>
                </v-flex>
                <v-flex xs12 md5>
                  <v-text-field label="Bairro"></v-text-field>
                </v-flex>
                <v-flex xs12 md5 class="mx-5">
                  <v-text-field label="Bairro"></v-text-field>
                </v-flex>
                <v-flex xs12 md5>
                  <v-text-field label="Bairro"></v-text-field>
                </v-flex>

                <v-flex xs12 md5 class="mx-5">
                  <v-text-field label="Bairro"></v-text-field>
                </v-flex>
                <v-flex xs12 md5>
                  <v-btn class="float-right mt-5" disabled color="red darken-1">Salvar</v-btn>
                </v-flex>
              </v-layout>
            </v-form>
          </v-card-text>
        </v-card>
      </v-flex>
    </v-layout>
  </v-container>
</template>

<script>
export default {};
</script>

<style>
</style>