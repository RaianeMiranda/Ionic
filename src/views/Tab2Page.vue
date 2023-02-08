<template>
  <ion-page>
    <ion-header>
      <ion-toolbar>
        <ion-title>Mapa do app</ion-title>
      </ion-toolbar>
    </ion-header>
    <ion-content :fullscreen="true">
      <div class="conteudo">
        <h1>Vamos colocar um mapa aqui no futuro</h1>

      </div>
    </ion-content>
  </ion-page>
</template>

<script lang="ts">
import { defineComponent } from 'vue';
import { IonPage, IonHeader, IonToolbar, IonTitle, IonContent } from '@ionic/vue';

export default defineComponent({
  name: 'Tab2Page',
  components: { IonHeader, IonToolbar, IonTitle, IonContent, IonPage }
});
</script>

<style scoped="style">
  h1{
    color: rgb(175, 0, 99);
  }
  .conteudo{
    display: flex;
    align-items: center;
    justify-content: center;
  }
</style>