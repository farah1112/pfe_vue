<template>
  <navbar-view />
  <div class="Nutrition">
    <v-row> </v-row>
  </div>
  <br />
  <div>
    <v-container align="center" style="background-color: #f1f8e9">
      <h5>Découvrez le projet CatchIT</h5>
      <p style="color: #1a237e; font-size: 20px" class="align:center">
        Soutenez le développement de Vue.js en postant une offre d'emploi ou un
        stage chez nous !
      </p>
      <h5>Découvrez qui se cache derrière CatchIT</h5>
      <p>
        CatchIT a été développé par des passionnés de Vue.js et Laravel dont le
        but est de contribuer à la communauté grandissante en aidant les
        entreprises à trouver stages et emplois en Tunisie.<br />Lorsque vous
        vous inscrivez à CatchIT, les entreprises pourront répertorier les
        emplois, les stages et les développeurs auront la possibilité de
        postuler à ces emplois et stages.
      </p>
      <v-row>
        <v-col cols="12" md="6">
          <v-card class="mx-auto" max-width="344">
            <v-img
              src="https://media-exp1.licdn.com/dms/image/C4E03AQEK9l8Tm3ZS8A/profile-displayphoto-shrink_800_800/0/1616934438146?e=1656547200&v=beta&t=6dGvVKqot-dNjGVjzwjFtnsOxcRwm3Lq4MnfR7QhZvE"
              height="280px"
              cover
            ></v-img>

            <v-card-title> WESLATI FARAH </v-card-title>

            <v-card-subtitle> VueJs developeur </v-card-subtitle>
            <p>Si vous aimez notre travail, évaluez-nous s'il vous plaît!</p>
            <v-card-actions>
              <v-rating
                v-model="rating"
                empty-icon="mdi-circle-outline"
                full-icon="mdi-circle"
                half-icon="mdi-circle-half"
                half-increments
                hover
              ></v-rating>

              <v-spacer></v-spacer>

              <v-btn
                :icon="show ? 'mdi-chevron-up' : 'mdi-chevron-down'"
                @click="show = !show"
              ></v-btn>
            </v-card-actions>

            <v-expand-transition>
              <div v-show="show">
                <v-divider></v-divider>

                <v-card-text>
                  Je suis développeur frontend/backend et UI designer. j'ai un
                  intérêt profond pour la conception parfaite au pixel près et
                  centrée sur l'utilisateur avec un focus particulier sur
                  l'expérience utilisateur.Je suis étudiant en 3ème année aussi
                </v-card-text>
              </div>
            </v-expand-transition>
          </v-card>
        </v-col>
        <v-col cols="12" md="6">
          <v-card class="mx-auto" max-width="344">
            <v-img
              src="https://avatars.githubusercontent.com/u/58521599?v=4"
              height="280px"
              cover
            ></v-img>

            <v-card-title> MEJRI MED ALI </v-card-title>

            <v-card-subtitle> Laravel developer </v-card-subtitle>
            <p>If you like our work ,Rate us please!</p>
            <v-card-actions>
              <v-rating
                v-model="rating1"
                empty-icon="mdi-circle-outline"
                full-icon="mdi-circle"
                half-icon="mdi-circle-half"
                half-increments
                hover
              ></v-rating>
              <v-spacer></v-spacer>

              <v-btn
                :icon="show1 ? 'mdi-chevron-up' : 'mdi-chevron-down'"
                @click="show1 = !show1"
              ></v-btn>
            </v-card-actions>

            <v-expand-transition>
              <div v-show="show1">
                <v-divider></v-divider>

                <v-card-text>
                  Je suis développeur web. J'aime jouer avec la pointe les
                  technologies. Aimer Laravel et travailler avec lui dans ce
                  projet et je viens de découvrir Vue.js avec mon partenaire
                  Farah. Je suis un étudiant de 3ème aussi.
                </v-card-text>
              </div>
            </v-expand-transition>
          </v-card>
        </v-col>
      </v-row>
    </v-container>
  </div>
  <br />
  <div>
    <h2>Avantages de poster avec nous</h2>
    <br />
    <v-timeline>
      <v-timeline-item color="purple-lighten-2" fill-dot right>
        <v-card>
          <v-card-title class="purple-lighten-2">
            <v-icon dark size="42" class="mr-4">
              mdi-account-supervisor
            </v-icon>
            <h5 class="display-6 white--text font-weight-light">
              Ici pour les étudiants
            </h5>
          </v-card-title>
          <v-card-text>
            Nous vous aidons à obtenir les meilleures opportunités (stages) dans
            différents domaines .
          </v-card-text>
        </v-card>
      </v-timeline-item>

      <v-timeline-item color="amber-lighten-1" fill-dot size="small">
        <v-card>
          <v-card-title class="amber-lighten-1 justify-end">
            <h5 class="display-6 mr-4 white--text font-weight-light">
              Ici pour les chômeurs
            </h5>
            <v-icon dark size="42"> mdi-account-tie </v-icon>
          </v-card-title>
          nous vous fournissons les opportunités d'emploi dans toute la Tunisie.
          <v-card-text> </v-card-text>
        </v-card>
      </v-timeline-item>

      <v-timeline-item color="cyan-lighten-1" fill-dot>
        <v-card>
          <v-card-title class="cyan-lighten-1">
            <v-icon class="mr-4" dark size="42">
              mdi-alarm-light-outline
            </v-icon>
            <h5 class="display-6 white--text font-weight-light">
              Vous proposer le travail/stage que vous souhaitez
            </h5>
          </v-card-title>
          <v-card-text>
            nous ferons de notre mieux pour votre aide. Soyez des nôtres!
          </v-card-text>
        </v-card>
      </v-timeline-item>
    </v-timeline>
  </div>
  <br /><br />
  <v-divider></v-divider>
  <footer-view />
</template>
<script>
import NavbarView from "@/components/NavbarView.vue";
import FooterView from "@/components/FooterView.vue";
export default {
  components: { NavbarView, FooterView },
  data: () => ({
    show: false,
    show1: false,
    rating: 3.5,
    rating1: 3.5,
  }),
};
</script>

<style>
.Nutrition {
  min-height: 80vh;
  min-width: 57vh;
  background-size: cover !important;
  background-position: center !important;
  padding: 2rem 9%;
  display: flex;
  align-items: center;
  background-image: url("https://cdn.dribbble.com/users/846207/screenshots/4670120/laptop_icon_animation.gif");
}
</style>
