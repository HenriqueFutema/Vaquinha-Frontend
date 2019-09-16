<template>
  <form @submit.prevent="handleSubmit">
    <v-container>
      <v-layout>
        <v-flex xs12 md12 class="mx-1">
          <v-card class="px-5 py-3">
            <h1>Novo Projeto</h1>
            <v-card-title>
              <v-row>
                <v-col cols="12">
                  <v-text-field
                    label="Nome do Projeto"
                    outlined
                    required
                    color="#F3B61F"
                    rounded
                    autofocus
                    v-model="nameProject"
                  ></v-text-field>
                </v-col>

                <v-col cols="12">
                  <v-textarea
                    v-model="descriptionProject"
                    outlined
                    name="input-7-4"
                    label="Descrição"
                    value
                    color="#F3B61F"
                  ></v-textarea>
                </v-col>

                <v-col cols="12">
                  <v-text-field
                    v-model="hashtags"
                    label="HashTags"
                    outlined
                    required
                    color="#F3B61F"
                    rounded
                  ></v-text-field>
                </v-col>
                <v-col cols="12">
                  <v-file-input
                    v-model="image"
                    show-size
                    counter
                    multiple
                    label="Foto do Projeto"
                    outlined
                  ></v-file-input>
                </v-col>

                <v-col cols="12">
                  <v-btn elevation="10" color="success" type="submit">Criar</v-btn>
                </v-col>
              </v-row>
            </v-card-title>
          </v-card>
        </v-flex>
      </v-layout>
    </v-container>
  </form>
</template>

<script>
import { mapGetters } from "vuex";
import api from "@/services/api";

export default {
  computed: {
    ...mapGetters(["getIsLogged", "getTokenUser"])
  },

  data: () => ({
    nameProject: "",
    descriptionProject: "",
    hashtags: "",
    image: null
  }),

  created: function() {
    if (!this.getIsLogged) {
      return this.$router.push("/signin");
    }
  },

  methods: {
    handleSubmit: async function() {
      const { nameProject, descriptionProject, hashtags, image } = this;

      const data = new FormData();

      data.append("nameProject", nameProject);
      data.append("description", descriptionProject);
      data.append("hashtags", hashtags);
      data.append("image", image[0]);

      const project = await api.post("projects/create", data, {
        headers: { Authorization: "Bearer " + this.getTokenUser }
      });

      this.nameProject = "";
      this.descriptionProject = "";
      this.hashtags = "";
      this.image = null;
    }
  }
};
</script>

<style scoped>
/* .cont {
  height: 100%;
  width: 100%;
} */
</style>