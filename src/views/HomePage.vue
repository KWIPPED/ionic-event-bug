<template>
  <ion-page>
    <ion-header :translucent="true">
      <ion-toolbar>
        <ion-title>Blank</ion-title>
      </ion-toolbar>
    </ion-header>
    
    <ion-content :fullscreen="true">
      <ion-header collapse="condense">
        <ion-toolbar>
          <ion-title size="large">Blank</ion-title>
        </ion-toolbar>
      </ion-header>
    
      <div id="container">
        <strong>Ready to create an app?</strong>
        <p>Start with Ionic <a target="_blank" rel="noopener noreferrer" href="https://ionicframework.com/docs/components">UI Components</a></p>
        <BR/>
         Open the inspector and click on the input below. You will see the following order of events:<BR/>
        <BR/>
         <table style="width:100%">
           <thead>
            <tr>
              <th class="ion-text-end">Action</th>
              <th>Events fired</th>
            </tr>
          </thead>
          <tbody>
           <tr>
            <td class="ion-text-end">On focus</td>
            <td>focus / blur /focus</td>
          </tr>
          <tr>
            <td class="ion-text-end">On blur</td>
            <td>blur</td>
          </tr>
          </tbody>
        </table>
         <ion-input @ionFocus="focus()"  @ionBlur="blur()" placeholder="click in here"></ion-input>
      </div>
    </ion-content>
  </ion-page>
</template>

<script lang="ts">
import { IonContent, IonHeader, IonPage, IonTitle, IonToolbar,IonInput } from '@ionic/vue';
import { defineComponent } from 'vue';

export default defineComponent({
  name: 'HomePage',
  components: {
    IonContent,
    IonHeader,
    IonPage,
    IonTitle,
    IonToolbar,
    IonInput
  },
  methods:{
    focus:function(){
      console.log("Focus Fired")
    },
    blur:function(){
      console.log("Blur Fired")
    }
  }
});
</script>

<style scoped>
#container {
  text-align: center;
  
  position: absolute;
  left: 0;
  right: 0;
  top: 50%;
  transform: translateY(-50%);
}

#container strong {
  font-size: 20px;
  line-height: 26px;
}

#container p {
  font-size: 16px;
  line-height: 22px;
  
  color: #8c8c8c;
  
  margin: 0;
}

#container a {
  text-decoration: none;
}
</style>
