<template>
  <v-container fluid fill-height>
    <v-slide-y-transition mode="out-in">
      <v-layout align-center justify-center row>
        <v-flex xs6>
          <v-card class="elevation-2 pt-3">
            <v-layout row align-center class="px-3 pb-3">
              <v-flex xs5>
                <v-img src='https://lh3.googleusercontent.com/Xg_HeMQ-c5RmC0vQy3AdjgyxlybpN0-MoHXOnflPsbhdjspfiooCDuv3ocrxbvfNpcr6_lNl7PaBeZhhfkXmDkTJmiMqwRWb6AVImeTa3aQvprqdWwnBmNGKHBQjtKpoz6q0v1ej6kgWJ_zkFh7avji1l8NNb2vCqK3p3koktvtiNnKFQxrQKA9_aS7F1bOarvPRVN0GdfrtjFi1Ae-C-U2Pr35cSCppUglB3lseslO8DnZQJEhX_kxJjH5gpVQFXnxuFeKRXhdQC4QGvH9ZZsOWy81zITDMep8KV1XlV6sULRiGTuYDnsJLyqvwS-mhlsmDnyygFhnQAFIcua6n_4uAT3Uuufvyx-zKwSd6aoBuap45YszplSOizfB6driehSAiQmTtd2qinnUq4_LARj0cOfTDLjOG1NHxUedpWL6y76YkvMiMH8vcoeAlJel2-qGKY9MJdJQRk5OJDId6_KT0P_iq72uTgxYgvXvsGYohvjSh7r8nmOGCXrKWB0JEN5MksbP6rOKiTRHCnfp39pgpXJMlkKfcEaQKlR9HCjXEkYPsuPw1XguppzNLjikf4mCeeT6sSQvEq24wGjhMhoqx4SMA79EKjY9_bp4H-cLAw6ZPJGosc7_8MYA7d3k=s1012-no'></v-img>
              </v-flex>
              <v-flex xs5 offset-xs2>
                <v-layout class="display-1">
                  Christopher Carlson
                </v-layout>
                <v-layout class="body-2">
                  A US Army veteran with experience in front and back-end software development technologies. Passionate about innovation, problem
                  solving and building applications with an emphasis on client functionality. Recently completed an immersive
                  coding program, challenged and grew in programming and scrum skills. A goal setter, natural born leader
                  and possesses excellent collaboration and project coordinating abilities. Seeking an opportunity with a
                  leading tech company focused on connecting users with creative breakthrough applications.
                </v-layout>
              </v-flex>
            </v-layout>
            <v-layout row align-center class="blue-grey lighten-2 pa-1">
              <v-flex v-for="(link, i) in links" :key="i">
                <a :href=link.link target="_blank"><i :class=link.icon></i></a>
                <div>{{link.title}}</div>
              </v-flex>
            </v-layout>
          </v-card>
        </v-flex>
      </v-layout>
    </v-slide-y-transition>
  </v-container>
</template>


<script>

  export default {
    name: 'Home',
    data() {
      return {
        links: [
          {
            title: 'Github',
            icon: 'fab fa-github fa-3x',
            link: 'https://github.com/ChristopherMCarlson'
          }
        ]
      }
    }
  }
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  h1,
  h2 {
    font-weight: normal;
  }

  ul {
    list-style-type: none;
    padding: 0;
  }

  li {
    display: inline-block;
    margin: 0 10px;
  }

  a {
    color: #42b983;
  }
</style>