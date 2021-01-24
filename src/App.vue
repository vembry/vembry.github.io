<template>
  <v-app>
    <v-main>
      <v-container>
        <v-row>
          <v-col cols="4">
            <Profile />
          </v-col>
          <v-col cols="8">
            <div class="mb-6">
              <Skills />
            </div>
            <div class="mb-6">
              <Works />
            </div>
            <div class="mb-6">
              <Educations />
            </div>
          </v-col>
        </v-row>
      </v-container>
    </v-main>
  </v-app>
</template>

<script>
import Profile from "./components/Profile";
import Skills from "./components/Skills";
import Works from "./components/Works";
import Educations from "./components/Educations";

export default {
  name: "App",

  components: {
    Profile,
    Skills,
    Works,
    Educations,
  },

  data: () => ({
    //
  }),
};
</script>
