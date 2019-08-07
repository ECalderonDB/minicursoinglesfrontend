<template>
  <v-container>
    <v-layout
      text-center
      wrap
    >
      <v-flex xs12>
        <v-img
          :src="require('../assets/logo.svg')"
          class="my-3"
          contain
          height="200"
        ></v-img>
      </v-flex>

      <v-flex mb-4>
        <h1 class="display-2 font-weight-bold mb-3">
          BIENVENIDO AL MINICURSO DE INGLES
        </h1>
        <p class="subheading font-weight-regular">
          Un curso que te hara a fortalecer tus capacidades como Bilingue A1,
          <br>Let's go
          <a href="https://community.vuetifyjs.com" target="_blank">Entrar aqui</a>
        </p>
      </v-flex>

      <v-flex
        mb-5
        xs12
      >
        <h2 class="headline font-weight-bold mb-3">USUARIOS</h2>

        <v-layout justify-center>
          <a
            v-for="(next, i) in whatsNext"
            :key="i"
            :href="next.href"
            class="subheading mx-3"
            target="_blank"
          >
            {{ next.text }}
          </a>
        </v-layout>
      </v-flex>

      <v-flex
        xs12
        mb-5
      >
        <h2 class="headline font-weight-bold mb-3">TEMAS</h2>

        <v-layout justify-center>
          <a
            v-for="(link, i) in importantLinks"
            :key="i"
            :href="link.href"
            class="subheading mx-3"
            target="_blank"
          >
            {{ link.text }}
          </a>
        </v-layout>
      </v-flex>


      <v-flex
        xs12
        mb-5
      >
        <h2 class="headline font-weight-bold mb-3">ACTIVIDADES</h2>

        <v-layout justify-center>
          <a
            v-for="(eco, i) in ecosystem"
            :key="i"
            :href="eco.href"
            class="subheading mx-3"
            target="_blank"
          >
            {{ eco.text }}
          </a>
        </v-layout>
      </v-flex>
    </v-layout>
  </v-container>
</template>

<script>
export default {
  data: () => ({
    ecosystem: [
      {
        text: 'NOMBRE_ACTIVIDAD',
        href: 'https://github.com/vuetifyjs/vuetify-loader',
      },
      {
        text: 'TIPO DE ACTIVIDAD',
        href: 'https://github.com/vuetifyjs/vuetify',
      },

    ],
    importantLinks: [
      {
        text: 'NOMBRE DEL TEMA',
        href: 'https://vuetifyjs.com',
      },
      {
        text: 'OBJETIVO DEL TEMA',
        href: 'https://community.vuetifyjs.com',
      },

    ],
    whatsNext: [
      {
        text: ' NOMBRES',
        href: 'https://vuetifyjs.com/components/api-explorer',
      },
      {
        text: 'APRELLIDOS ',
        href: 'https://vuetifyjs.com/layout/pre-defined',
      },
      {
        text: 'ALIAS_USUARIO',
        href: 'https://vuetifyjs.com/getting-started/frequently-asked-questions',
      },
    ],
  }),
};
</script>
