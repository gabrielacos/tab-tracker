<template>
  <v-layout column>
    <v-flex xs6 offset-xs3>
      <div class="white elevation-2">
        <v-toolbar flat dense class="cyan" dark>
          <v-toolbar-title>Register</v-toolbar-title>
        </v-toolbar>
          <div class="pl-4 pr-4 pt-2 pb-2">
            <v-text-field
              label = "Email"
              v-model="email"
             ></v-text-field>
              <br>
               <v-text-field
              label="Password"
              type="password"
              name="password"
              v-model="password"
              ></v-text-field>
              <br>
              <div class="error" v-html="error"/>
              <br>
              <v-btn class="cyan" dark @click="register">Register
              </v-btn>
          </div>   
      </div>
    </v-flex>
  </v-layout>
</template>

<script>
import PageHeader from '@/components/Header.vue'
import AuthenticationService from "@/service/AuthenticationService";
export default {
  data() {
    return {
      email: "",
      password: "",
      error: null
    };
  },


  methods: {
    async register() {
      try {
        await AuthenticationService.register({
          email: this.email,
          password: this.password
        });
      } catch (error) {
        this.error = error.response.data.error;
      }
    }
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
