<template>
  <ion-page>    
    <ion-content :fullscreen="true">
      
      <div id="container">
        <strong>Ágora</strong>
        <div class="text-input-email">
          <ion-item class="text-input-content">
            <ion-input type="email" placeholder="Email" v-model="user.email"></ion-input>
          </ion-item>
        </div>
        <div class="text-input-password">
          <ion-item class="text-input-content">
            <ion-input type="password" placeholder="Senha" v-model="user.password"></ion-input>
          </ion-item>
        </div>
        <div class="routers-links">
          <ion-text>Primeiro acesso</ion-text>
          <ion-text style="margin-left: 30px;">Esqueci a senha</ion-text>
        </div>
        <div class="login-button">
          <ion-button expand="block" @click="login">Entrar</ion-button>
        </div>
      </div>
    </ion-content>
  </ion-page>
</template>

<script lang="ts">
import { IonContent, IonPage, IonInput, IonItem, IonButton, IonText } from '@ionic/vue';
import { defineComponent } from 'vue';

export default defineComponent({
  name: 'Login',
  components: {
    IonContent,
    IonPage,
    IonItem,
    IonInput,
    IonButton,
    IonText
  },
  data () {
    return {
      user: {
        email: null,
        password: null
      }
    }
  },
  methods: {
    login() {
      alert(`O e-mail do usuáio é ${this.user.email} e a senha é ${this.user.password}`)
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
.text-input-email {
  position: absolute;
  left: 25%;
  right: 25%;
  width: 50%;
}
.text-input-content {
  border-style: solid;
  border-radius: 20px;
  border-width: 1px;
}
.text-input-password {
  position: absolute;
  top: 90px;
  left: 25%;
  right: 25%;
  width: 50%;
}
.routers-links {
  position: absolute;
  top: 150px;
  left: 25%;
  right: 25%;
}
.login-button {
  position: absolute;
  top: 180px;
  left: 40%;
  right: 40%;
  width: 400px;
}
</style>