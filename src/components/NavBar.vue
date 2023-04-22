<template>
  <v-app-bar app color="black" dark flat class="px-12">
    <v-btn>
        <v-icon color="yellow" left class="mr-2">fas fa-file-signature</v-icon>Perfil Profissional
    </v-btn>
    <v-spacer></v-spacer>
    <v-btn text @click="scroll('home')" class="text-yellow">Home</v-btn>
    <v-btn text @click="scroll('sobre')" class="text-yellow">Sobre</v-btn>
    <v-btn text @click="scroll('portfolio')" class="text-yellow">Portfólio</v-btn>
    <v-btn text @click="scroll('contact')" class="text-yellow">Contatos</v-btn>    
  </v-app-bar>

</template>

<script>

export default {
    methods: {
        scroll(refName){
            const element = document.getElementById(refName);
            element.scrollIntoView({behavior: "smooth"});
        }
    }

}
</script>

<style>

</style>