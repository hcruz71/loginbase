<template>
    <v-card width="400"  class=" mx-auto mt-10">
    <v-card-title>
        <h1 class="display-1">Acceso</h1>
    </v-card-title>
    <v-card-text>
        <v-form>
        <v-text-field 
            label="Username" 
            prepend-icon="mdi-account-circle"/>
        <v-text-field 
            :type="showPassword ? 'text' : 'password'"
            label="Password" 
            prepend-icon="mdi-lock"
            :append-icon="showPassword ? 'mdi-eye' : 'mdi-eye-off'"
            @click:append="showPassword = !showPassword"
            />
            
        </v-form>
    </v-card-text>
    <v-divider></v-divider>
    <v-card-action>
        <v-btn color="success" >Registrar</v-btn> 
        <v-btn color="info"  >Entrar</v-btn>
    </v-card-action>
    </v-card>
</template>

<script>
export default {
    name: 'loginPage',
    data: () => ({
        showPassword: false
  })
}
</script>

<style>
body {
  background: #ffffff;
  background-image: url("../assets/banner_login.jpg");
  background-attachment: fixed;
  background-position: center;
  background-repeat: no-repeat;
  background-size: cover;
  height: auto;
}
</style>