<template>
  <v-card outlined tile>
    <v-card-title>educations</v-card-title>
    <v-card-text>
      <v-list>
        <v-list-item
          v-for="(education, index) in educations"
          :key="`education-${index}`"
        >
          <a :href="education.link" target="_blank">
            <v-list-item-avatar tile max-width="40" style="align-self: unset;">
              <v-img
                contain
                :src="require(`@/assets/${education.image}`)"
              ></v-img>
            </v-list-item-avatar>
          </a>
          <v-list-item-content>
            <v-list-item-title>
              {{ education.name }}
            </v-list-item-title>
            <v-list-item-subtitle>
              {{ education.degree }}
            </v-list-item-subtitle>
            <v-list-item-subtitle>
              {{ education.description }}
            </v-list-item-subtitle>
          </v-list-item-content>
          <v-list-item-action style="align-self: unset;">
            {{ education.timeframe }}
          </v-list-item-action>
        </v-list-item>
      </v-list>
    </v-card-text>
  </v-card>
</template>
<script>
export default {
  data: () => ({
    educations: [
      {
        image: "binus-logo.png",
        link: "https://www.binus.ac.id/",
        name: "bina nusantara university",
        degree: "bachelor of computer science",
        description: "cumulative gpa: 3.47 / 4.00",
        timeframe: "09/2014 - 09/2018",
      },
    ],
  }),
};
</script>
