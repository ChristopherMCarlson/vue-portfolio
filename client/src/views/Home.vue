<template>
  <v-container mt-5>
    <div class="display-4">About Me</div>
    <v-flex xs12>
      <v-card color="cyan darken-2" class="white--text">
        <v-layout align-center>
          <v-flex pa-2 xs5>
            <v-img src="https://i.imgur.com/lPJBNkG.jpg?1" contain></v-img>
          </v-flex>
          <v-flex xs7>
            <v-card-title primary-title>
              <div>
                <div class="headline">Chris Carlson</div>
                <div blockquote>A US Army veteran with experience in front and back-end software development
                  technologies.
                  Passionate about innovation, problem solving and building applications with an emphasis on client
                  functionality. Recently completed an immersive coding program, challenged and grew in programming and
                  scrum skills. A goal setter, natural born leader and possesses excellent collaboration and project
                  coordinating abilities. Seeking an opportunity with a leading tech company focused on connecting
                  users with creative breakthrough applications.</div>
              </div>
            </v-card-title>
          </v-flex>
        </v-layout>
      </v-card>
    </v-flex>
    <v-flex xs-12>
      <div class="display-4">Projects</div>
      <v-layout mt-3>
        <v-flex xs-3>
          <v-hover>
            <v-card slot-scope="{ hover }" class="mx-auto declare-width" color="grey lighten-4">
              <v-img :aspect-ratio="16/16" src="https://cdn.vuetifyjs.com/images/cards/kitchen.png">
                <v-expand-transition>
                  <div v-if="hover" class="d-flex transition-fast-in-fast-out orange darken-2 v-card--reveal display-1 white--text"
                    style="height: 100%;">
                    Inspire
                  </div>
                </v-expand-transition>
              </v-img>
            </v-card>
          </v-hover>
        </v-flex>

        <v-flex xs-3>
          <v-hover>
            <v-card slot-scope="{ hover }" class="mx-auto declare-width" color="grey lighten-4">
              <v-img :aspect-ratio="16/16" src="https://cdn.vuetifyjs.com/images/cards/kitchen.png">
                <v-expand-transition>
                  <div v-if="hover" class="d-flex transition-fast-in-fast-out orange darken-2 v-card--reveal display-1 white--text"
                    style="height: 100%;">
                    Lendr
                  </div>
                </v-expand-transition>
              </v-img>
            </v-card>
          </v-hover>
        </v-flex>

        <v-flex xs-3>
          <v-hover>
            <v-card slot-scope="{ hover }" class="mx-auto declare-width" color="grey lighten-4">
              <v-img :aspect-ratio="16/16" src="https://cdn.vuetifyjs.com/images/cards/kitchen.png">
                <v-expand-transition>
                  <div v-if="hover" class="d-flex transition-fast-in-fast-out orange darken-2 v-card--reveal display-1 white--text"
                    style="height: 100%;">
                    Keepr
                  </div>
                </v-expand-transition>
              </v-img>
            </v-card>
          </v-hover>
        </v-flex>
      </v-layout>
    </v-flex>
    <v-flex xs-12>
      <div class="display-4">Skills</div>
    </v-flex>
    <v-layout xs-12>
      <div class="text-xs-center">
        <v-progress-circular :rotate="-90" :size="200 " :width="25" :value="95" color="teal" justify-center>
          <v-hover>
            <i class="fab fa-js-square fa-7x" slot-scope="{ hover }">
              <v-expand-transition>
                <div v-if="hover" class="d-flex transition-fast-in-fast-out mySkills--reveal subheading black--text"
                  style="height: 100%;">
                  Javascript
                </div>
              </v-expand-transition>
            </i>
          </v-hover>
        </v-progress-circular>

        <v-progress-circular :rotate="-90" :size="200 " :width="25" :value="90" color="teal">
          <v-hover>
            <i class="fab fa-vuejs fa-7x" slot-scope="{ hover }">
              <v-expand-transition>
                <div v-if="hover" class="d-flex transition-fast-in-fast-out mySkills--reveal subheading black--text"
                  style="height: 100%;">
                  Vue JS
                </div>
              </v-expand-transition>
            </i>
          </v-hover>
        </v-progress-circular>

        <v-progress-circular :rotate="-90" :size="200 " :width="25" :value="95" color="teal">
          <v-hover>
            <i class="fab fa-html5 fa-7x" slot-scope="{ hover }">
              <v-expand-transition>
                <div v-if="hover" class="d-flex transition-fast-in-fast-out mySkills--reveal subheading black--text"
                  style="height: 100%;">
                  HTML 5
                </div>
              </v-expand-transition>
            </i>
          </v-hover>
        </v-progress-circular>

        <v-progress-circular :rotate="-90" :size="200 " :width="25" :value="95" color="teal">
          <v-hover>
            <i class="fab fa-css3 fa-7x" slot-scope="{ hover }">
              <v-expand-transition>
                <div v-if="hover" class="d-flex transition-fast-in-fast-out mySkills--reveal subheading black--text"
                  style="height: 100%;">
                  CSS 3
                </div>
              </v-expand-transition>
            </i>
          </v-hover>
        </v-progress-circular>
      </div>
    </v-layout>
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

<!-- Add "
    scoped" attribute to limit CSS to this component only -->
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

  .v-card--reveal {
    align-items: center;
    bottom: 0;
    justify-content: center;
    opacity: .7;
    position: absolute;
    width: 100%;
  }

  .mySkills--reveal {
    align-items: center;
    bottom: 0;
    justify-content: center;
    opacity: 1;
    position: absolute;
    width: 100%;
    background-color: rgb(250, 250, 250);
  }

  .declare-width {
    width: 23vw;

  }
</style>