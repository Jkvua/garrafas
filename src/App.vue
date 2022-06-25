<template>
<v-app>
  <v-main class="main">
    <v-app-bar app color="#F5E1CE" elevation = "3">
      <v-spacer></v-spacer>
      <v-icon>mdi-cart</v-icon>
      <v-app-bar-nav-icon @click.stop="sidebar = !sidebar"></v-app-bar-nav-icon>
    </v-app-bar>
    
    <v-navigation-drawer app v-model="sidebar">
      <v-list dense color="#F5E1CE">
    <v-list-item>


    <v-icon class="bunda-bar"></v-icon>

<v-list-item>
          <v-list-item-avatar>
            <img src="https://randomuser.me/api/portraits/women/81.jpg">
          </v-list-item-avatar>
          <v-list-item-content>
            <v-list-item-title>Angèle Costa</v-list-item-title>
            <v-list-item-subtitle>Conta</v-list-item-subtitle>
          </v-list-item-content>
        </v-list-item>
        
  </v-list-item>
    
      </v-list>
      <v-divider></v-divider>
     <v-list-item>
       <v-list-item-avatar></v-list-item-avatar>
<v-list-item-content> Inicio</v-list-item-content>
<v-btn icon small><v-icon>mdi-chevron-left</v-icon></v-btn>
</v-list-item>
  <v-divider></v-divider>
  <v-list>
    <v-list-item>
      <v-list-item-icon>
        <v-icon>mdi-cart</v-icon>
      </v-list-item-icon>
      <v-list-item-content>Carrinho</v-list-item-content>
    </v-list-item>
    <v-divider></v-divider>
    <v-list-item>
       <v-list-item-avatar></v-list-item-avatar>
<v-list-item-content> Historico de compras</v-list-item-content>
<v-btn icon small><v-icon>mdi-chevron-left</v-icon></v-btn>
</v-list-item>
  </v-list>
    </v-navigation-drawer>
  </v-main>
   
  
 
 <img alt="Garrafas" src="./assets/garrafa55.png" class="imagem">
 <v-list dense color="#F5E1CE"> </v-list>
 <v-list class="amor">
 
    </v-list>
   
<v-list>
  <v-carousel hide-delimiters>
    <v-carousel-item
      v-for="(item,i) in items"
      :key="i"
      :src="item.src"
    ></v-carousel-item>
  </v-carousel>
  
 

<v-footer
    dark
    padless
  >
    <v-card
      flat
      tile
      class="light white--text text-center"
    >
      <v-card-text>
        <v-btn
          v-for="icon in icons"
          :key="icon"
          class="mx-7 white--text"
          icon
        >
          <v-icon size="30px">
            {{ icon }}
          </v-icon>
        </v-btn>
      </v-card-text>

      <v-card-text class="white--text pt-5">
       <h3>Quem somos?</h3><h4> "Esse é um site para você personalizar a sua garrafinha do jeito de você achar melhor -- Aqui vem a descrição da empresa."</h4> feugiat arcu sapien, et iaculis ipsum elementum sit amet. Mauris cursus commodo interdum. Praesent ut risus eget metus luctus accumsan id ultrices nunc. Sed at orci sed massa consectetur dignissim a sit amet dui. Duis commodo vitae velit et faucibus. Morbi vehicula lacinia malesuada. Nulla placerat augue vel ipsum ultrices, cursus iaculis dui sollicitudin. Vestibulum eu ipsum vel diam elementum tempor vel ut orci. Orci varius natoque penatibus et magnis dis parturient montes, nascetur ridiculus mus.
      </v-card-text>

      <v-divider></v-divider>

      <v-card-text class="white--text">
        {{ new Date().getFullYear() }} — <strong>Calamidade</strong>
      </v-card-text>
    </v-card>

    
  </v-footer>
 
</v-list>

</v-app>

</template>


<script>
export default {
  data(){
    return {
      sidebar: true,
      items: [
          {
            src: 'https://img.freepik.com/psd-gratuitas/maquete-de-garrafa-de-agua-doce_358694-287.jpg?w=2000',
          },
          {
            src: 'https://img.freepik.com/psd-gratuitas/maquete-de-garrafa-de-agua-doce_358694-282.jpg?w=2000',
          },
          {
            src: 'https://img.freepik.com/psd-gratuitas/maquete-de-garrafa-de-agua-doce_358694-291.jpg?w=2000',
          },
          {
            src: 'https://img.freepik.com/free-psd/1-0l-fresh-water-bottle-mockup_358694-292.jpg?w=2000',
          },
         {
            src: 'https://www.eymockup.com/wp-content/uploads/2021/01/Premium-Mineral-Water-Bottle-Psd-Mockup-4.jpg',
          },
        ],
        
      icons: [
        'mdi-facebook',
        'mdi-linkedin',
        'mdi-instagram',
      ],
   
  }
      }
    
  }
    
    
    




</script>


<style>
   .burger-bar {
        position: absolute;
        top: 10%;
        right: 6px;
        left: 70%;
        height: 3px;
        width: auto;
        margin-top: -1px;
        transition: transform .6s cubic-bezier(.165, .84, .44, 1), opacity .3s cubic-bezier(.165, .84, .44, 1), background-color .6s cubic-bezier(.165, .84, .44, 1);
   }
   .bunda-bar {
        position: absolute;
        top: 10%;
        right: 3px;
        left: 3%;
        height: 0px;
        width: auto;
        margin-top: -1px;
        transition: transform .6s cubic-bezier(.165, .84, .44, 1), opacity .3s cubic-bezier(.165, .84, .44, 1), background-color .6s cubic-bezier(.165, .84, .44, 1);
   }
  .imagem {
        display: block;
  }

  .amor {
    text-align: center;
    font-family: 'Times New Roman', Times, serif;
  }
  
   



</style>