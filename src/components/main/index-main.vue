
<template>
    <section class="flex h-[calc(100vh-128px)] w-screen items-center flex-col">
      <h1 class="mb-2 text-[#EDEDED] 
      text-center
       text-lg w-[550px]
       pt-[60px]">{{ translate }}</h1>
       <Techs/>
    </section>
  </template>
  
  <script>
  import Techs from "../techs/index-techs.vue";
  
  
  export default {
    props: {
      
    },
    data() {
      return {
        translate: ""
      };
    },
    components: {
      Techs
    }
  };
  </script>