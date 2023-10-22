
<template>
  <div class="h-screen">
    <Header />
    <Main
      :translate="selected == '' ? this.flags[0].translations : selected"
      v-on:handler="handleClick"
    />
     

    <footer
      class="gap-[50px] flex h-16 w-screen items-center justify-center"
    >
      <Botao v-for="item in flags" :idioma="item" :key="item" @tradutor="handleClick" />
      <p>{{ item }}</p>
    </footer>
  </div>
</template>

<script>
//Imports
import Header from "./components/header/index-header.vue";
//import footer from "./components/footer/index-footer.vue";
import Main from "./components/main/index-main.vue";
import Botao from "./components/botao/index-botao.vue";





export default {
  data() {
    return {
      flags: [
        {
          
          idioma: "Português",
          flag: "https://raw.githubusercontent.com/daniellymomm/desafioweb/main/src/assets/brazil-flag.png",
          translations:
            "Olá, meu nome é Danielly Momm e eu sou Desenvolvedor Front-End, Tecnologias que tenho experiência:",
        },
        {
          
          idioma: "Francês",
          flag: "https://raw.githubusercontent.com/daniellymomm/desafioweb/main/src/assets/french-flag.png",
          translations:
            "Bonjour, je m'appelle Danielly Momm et je suis développeur Front-End, Technologies j'ai de l'expérience:",
        },
        {
          idioma: "Inglês",
          flag: "https://raw.githubusercontent.com/daniellymomm/desafioweb/main/src/assets/united-states-flag.png",
          translations:
            "Hi, my name`s Danielly Momm and I`m a Front-End Developer, Technologies that I have experience:",
        },
      ],
      selected: "",
    };
  },


     
  components: {
    Header,
    Main,
    Botao,
    
  },


  methods: {
    handleClick(language) {
      console.log(language);

      if (language == "Português") {
        this.selected = this.flags[0].translations;
      } else if (language == "Francês") {
        this.selected = this.flags[1].translations;
      } else {
        this.selected = this.flags[2].translations;
      }
    },
  },
};
</script>

<style></style>