<template>
  <ion-page>
    <ion-header>
      <ion-toolbar>
        <ion-title>Tab 3</ion-title>
      </ion-toolbar>
    </ion-header>
    <ion-content :fullscreen="true">
      <ion-header collapse="condense">
        <ion-toolbar>
          <ion-title size="large">Tab 3</ion-title>
        </ion-toolbar>
      </ion-header>

      <ion-button @click="minhaFuncao()">Click aqui</ion-button>
      <ion-button @click="showHelloToast()">show Hello Toast</ion-button>

      <ion-item>
        <ion-label>Meu Input</ion-label>
        <ion-input v-model="outraVariavel"></ion-input>
      </ion-item>

      <div v-text="minhaVariavel"></div>
      <div v-html="minhaVariavel"></div>

      <div v-text="outraVariavel"></div>
      <div v-text="contador"></div>
      
      <ExploreContainer name="Tab 3 page" />
    </ion-content>
  </ion-page>
</template>

<script lang="ts">
import { defineComponent, ref } from 'vue';
import { IonButton, IonItem, IonLabel, IonInput, IonPage, IonHeader, IonToolbar, IonTitle, IonContent } from '@ionic/vue';
import ExploreContainer from '@/components/ExploreContainer.vue';
import { Toast } from '@capacitor/toast';

export default defineComponent({
  name: 'Tab3Page',
  components: { ExploreContainer, IonButton, IonItem, IonLabel, IonInput, IonHeader, IonToolbar, IonTitle, IonContent, IonPage },
  setup(){
      let minhaVariavel = ref("Pão de <b style='color:red'>queijo</b>");
      let outraVariavel = ref("");
      let contador = ref(0);
      const minhaFuncao = () => {
        contador.value += 1;
      }
      const showHelloToast = async () => {
        await Toast.show({
          text: 'Hello! ' + outraVariavel.value,
        });
      };
    return{
      minhaVariavel,
      outraVariavel,
      minhaFuncao,
      contador,
      showHelloToast
    }
  }
});
</script>
