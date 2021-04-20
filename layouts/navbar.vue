<template>
  <v-app>
    <v-app-bar
      :clipped-left="clipped"
      fixed
      app
    >
      <v-app-bar-nav-icon @click.stop="drawer = !drawer"/>
      <v-btn
        icon
        @click.stop="miniVariant = !miniVariant"
      >
        <v-icon>mdi-{{ `chevron-${miniVariant ? 'right' : 'left'}` }}</v-icon>
      </v-btn>
      <v-btn
        icon
        @click.stop="clipped = !clipped"
      >
        <v-icon>mdi-application</v-icon>
      </v-btn>
      <v-btn
        icon
        @click.stop="fixed = !fixed"
      >
        <v-icon>mdi-minus</v-icon>
      </v-btn>
      <v-toolbar-title v-text="title"/>
      <v-spacer/>
      <v-spacer/>

      <div v-if="$auth.loggedIn">
        <v-btn color="primary">
          chào {{ $auth.user.name }}
        </v-btn>
        <v-btn
          color="red "
          @click.stop="$auth.logout()">
          <v-icon>
            mdi-login-variant
          </v-icon>
          Logout
        </v-btn>
      </div>
      <div v-else>
        <v-btn
          color="primary"
          to="/login">
          <v-icon>
            mdi-login-variant
          </v-icon>
          Login
        </v-btn>

        <v-btn
          color="orange"
          @click.stop="openRegisterForm=true">
          <v-icon>
            mdi-account-plus
          </v-icon>
          Register
        </v-btn>
        <RegisterComponent v-model="openRegisterForm"/>
      </div>
    </v-app-bar>
    <v-main>
      <v-container>
        <nuxt/>
      </v-container>
    </v-main>
  </v-app>


</template>

<script>
export default {
  name: "navbar",
  data() {
    return {
      clipped: false,
      fixed: false,
      openRegisterForm: false,
      miniVariant: false,
      title: 'Vuetify.js'
    }
  }
}
</script>

<style scoped>

</style>
