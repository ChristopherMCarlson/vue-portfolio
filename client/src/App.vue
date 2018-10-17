<template>
  <v-app>
    <v-toolbar absolute color="cyan darken-2" dark scroll-off-screen scroll-target="#scrolling-techniques">
      <v-toolbar-side-icon @click.stop="drawer = !drawer"></v-toolbar-side-icon>

      <v-toolbar-title>Chris Carlson</v-toolbar-title>
    </v-toolbar>
    <v-navigation-drawer v-model="drawer" absolute temporary>
      <v-list class="pa-1">
        <v-list-tile avatar>
          <v-list-tile-avatar>
            <img src="https://i.imgur.com/lPJBNkG.jpg?1">
          </v-list-tile-avatar>

          <v-list-tile-content>
            <v-list-tile-title>Chris Carlson</v-list-tile-title>
          </v-list-tile-content>
        </v-list-tile>
      </v-list>

      <v-list class="pt-0" dense>
        <v-divider></v-divider>

        <v-list-tile v-for="item in items" :key="item.title" @click="">
          <v-list-tile-action>
            <v-icon>{{ item.icon }}</v-icon>
          </v-list-tile-action>

          <v-list-tile-content>
            <v-list-tile-title>{{ item.title }}</v-list-tile-title>
          </v-list-tile-content>
        </v-list-tile>
      </v-list>
    </v-navigation-drawer>
    <div id="scrolling-techniques" class="scroll-y" style="max-height: 600px;"></div>
    <router-view />
  </v-app>
</template>

<script>

  export default {
    name: 'App',
    data() {
      return {
        drawer: null,
        items: [
          { title: 'Home', icon: 'dashboard' },
          { title: 'About', icon: 'question_answer' }
        ],
      }
    }
  }
</script>