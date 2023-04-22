<template>
  <v-app id="home">
    <NavBar />
    <v-container fluid>
      <div class = "head">
            <v-row>
              <v-col cols="5">
                  <div style="position: relative"  class="mt-16">
                    <h1 class= "text-grey">Olá,</h1>
                    <h1 class= "text-white">Eu sou a Priscila Latance</h1>
                    <span class ="text-grey">Desenvolvedora BackEnd</span><br />
                    <v-btn tile dark class="text-yellow mt-8" variant="outlined">Entre em contato</v-btn>
                  </div>
              </v-col>
              <v-col cols="2">
                <div style="position: absolute; z-index: 9999; bottom:0;margin-left: auto;left: 0; right: 0; text-align: center;"></div>
                <v-icon>fas fa-agle-double-down</v-icon>
              </v-col>
                <v-col cols="5">
                <div style="position: relative; z-index: 9999;" class="mt-16">
                <v-img src="PriFormatado2.png" contain max-height="300"></v-img>
                </div>
              </v-col>
            </v-row>
      </div>
      <v-col cols="12" class="mt-16" id="sobre">
        <div>
          <v-row>
            <v-col cols="12" sm="6">
              <div class ="egg">
                  <v-img src="Programando.jpg" max-height="300"></v-img>
              </div>
            </v-col>
            <v-col cols="12" sm="6">
              <h5 class="mt-16">Sobre Mim</h5>
              <div style="width: 120px">
                <v-slider v-model="slider2" color="yellow">
                </v-slider>
              </div>
              <h4 class ="mt-n4">Eu sou uma Dev BackEnd focada na linguagem Java</h4>
              <p class="text-grey">Tendo experiência com Spring Boot, Spring Security, JWT, JPA, Hibernate, Microsserviços, C#, Observabilidade, Mensageria, SQL, HTML, CSS, JavaScript, Vue.js, TDD e Testes unitários.</p>
              <br />
              <v-btn tile dark color="yellow" class="mt-4">
                Download do Resumo
              </v-btn>
            </v-col>
          </v-row>
        </div>
      </v-col>
      <div class="text-center mt-4">
        <h2>Meus Projetos</h2>
        <div style="width:120px; margin: 0 auto">
          <v-slider v-model="slider2" color="yellow"></v-slider>
        </div>
      </div>
      <v-col cols="12" class="padd" id="portfolio">
        <div class="first" id="project">
            <v-col cols="12">
              <div class="child">
                <v-btn icon="fas fa-laptop" color="#FBDF7E" class= "text-white"></v-btn>
                <h3 class = "ml-3 mt-4">Java</h3>
                <p class= "text-grey ml-3 mt-4 text-caption">Todos meus projetos de estudos com java é possivel visualizar pelo meu canal no github priscilalatance<br />
                </p>                
              </div>              
            </v-col>
        </div>
      </v-col>
      <v-col cols="12" sm="12" class="px-16" id="contact">
        <v-row>
          <v-col cols="12" sm="4">
            <div class="child">
              <h1>Informações de Contato</h1>
              <v-btn icon="fas fa-map-marker-alt" class="mt-10" variant="outlined"></v-btn><br />
              <span class="text-caption">Rua imaginaria, 68</span><br />
              <v-btn icon="fas fa-phone-alt" class="mt-10" variant="outlined"></v-btn><br />
              <span class="text-caption">+55 99 99999-9999</span><br />
              <v-btn icon="fas fa-envelope" class="mt-10" variant="outlined"></v-btn><br />
              <span class="text-caption">priscila.latance@gmail.com</span><br />
            </div>
          </v-col>
          <v-col cols="12" sm="8">
            <h1 class= "mt-8">Escreva sua mensagem</h1>
            <v-divider></v-divider>
            <span class="text-caption"></span>
            <v-row class="mt-10">
              <v-col cols="12" sm="6">
                <v-text-field label="Name" persistent-hint variantt="outlined"></v-text-field>
              </v-col>
                <v-col cols="12" sm="6">
                <v-text-field label="Telefone" persistent-hint variantt="outlined"></v-text-field>
              </v-col>
            </v-row>
            <v-textarea label="Message" persistent-hint variantt="outlined"></v-textarea> 
            <v-btn color="#FBDF7E" class="mt-2">Enviar</v-btn>
          </v-col>
        </v-row>
      </v-col>
    </v-container>
    <FooterView />
  </v-app>
</template>

<script>
import { defineComponent } from 'vue';

// Components
import NavBar from '@/components/NavBar.vue';
import FooterView from '@/components/FooterView.vue';

export default defineComponent({
  name: 'HomeView',
  setup(){
    return{

    }
  },

  components: {
    NavBar,
    FooterView
  },
});
</script>

<style scoped>
.v-container{
  padding: 16px 0;
}
.head{
  position: relative;
  text-align: center;
  padding: 12px;
  margin-bottom: 6px;
  height: 400px;
  width: 100%;
  color: white; 
}
.head:before{
  content: " ";
  position: absolute;
  top: 0;
  left: 0;
  height: 100%;
  width: 50%;
  background: black;
  transform: skew(0deg, 6deg);
}
.head:after{
  content: " ";
  position: absolute;
  top: 0;
  right: 0;
  height: 100%;
  width: 50%;
  background: black;
  transform: skew(0deg, -6deg);  
}
.egg{
  display: block;
  margin-left: 100px;
  margin-top: 50px;
  width: 356px;
  height: 300px;
  background-color: white;
  border-radius: 50% 50% 50% 50% / 60% 60% 40% 0%;
}
.first{
  width: 100%;
  height: 280px;
  text-align: center;
  padding: 2rem 2rem;
}
.child{
  display: inline-block;
  padding: 2rem 1rem;
  vertical-align: middle;
  text-align: center;
  margin-right: 8px;

}
.pre{
  width: 100%;
  height: 380px;
  text-align: center;
  padding: 0 200px;
  background-color: #f5f5f5;
}
.hire{
  width:100%;
  height: 200px;
  padding: 0 200px;
  background-color: #e9e9e9;
  margin-top: -24px;
}
</style>
