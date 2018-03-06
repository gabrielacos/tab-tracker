<template>
  <v-toolbar fixed class="cyan" dark>
    <v-toolbar-title class="mr-4">
      Tab Tracker  
    </v-toolbar-title>
    <v-toolbar-items>
      <v-btn router to="/" flat dark>
        Home 
      </v-btn>
    </v-toolbar-items>
    <v-spacer></v-spacer>
     <v-toolbar-items>
      <v-btn router to="login"  flat dark>
       Login
      </v-btn>
    </v-toolbar-items>
      <v-toolbar-items>
        <v-btn router to="register" flat dark>
          Sign Up
        </v-btn>
      </v-toolbar-items>
  </v-toolbar>
</template>

<script>
export default {

  data () {
    return {
     
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
