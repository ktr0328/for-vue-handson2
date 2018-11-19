<template>
  <v-app>
    <v-toolbar app>
      <v-toolbar-side-icon @click='toolbar = !toolbar' />
      <v-toolbar-title class="headline">
        for-vue-handson
      </v-toolbar-title>
      <v-spacer></v-spacer>
    </v-toolbar>
    <v-navigation-drawer
      app
      v-model='toolbar'
    >
      <v-list>
        <v-list-tile to='/'>
          <v-list-tile-avatar>
            <v-icon color="teal">fas fa-home</v-icon>
          </v-list-tile-avatar>
          <v-list-tile-content>
            <v-list-tile-title>home</v-list-tile-title>
          </v-list-tile-content>
        </v-list-tile>
        <v-list-tile to='/about'>
          <v-list-tile-avatar>
            <v-icon color="teal">fas fa-shapes</v-icon>
          </v-list-tile-avatar>
          <v-list-tile-content>
            <v-list-tile-title>about</v-list-tile-title>
          </v-list-tile-content>
        </v-list-tile>
      </v-list>
    </v-navigation-drawer>
    <v-content>
      <router-view/>
    </v-content>
  </v-app>
</template>

<script>
export default {
  name: 'App',
  data () {
    return {
      toolbar: true
    }
  }
}
</script>
