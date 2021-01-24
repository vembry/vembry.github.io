<template>
  <v-card outlined tile>
    <v-card-title>work experience</v-card-title>
    <v-card-text>
      <v-list>
        <v-list-item
          v-for="(work, index) in works"
          :key="`work-${index}`"
          style="align-items: unset;"
        >
          <a :href="work.link" target="_blank">
            <v-list-item-avatar tile max-width="40" style="align-self: unset;">
              <v-img contain :src="require(`@/assets/${work.image}`)"></v-img>
            </v-list-item-avatar>
          </a>
          <v-list-item-content>
            <v-list-item-title>
              {{ work.name }}
            </v-list-item-title>
            <v-list-item-subtitle>
              {{ work.description }}
            </v-list-item-subtitle>
            <v-list>
              <v-list-item
                v-for="(position, index1) in work.positions"
                :key="`work-${index}-pos${index1}`"
              >
                <v-list-item-content>
                  <v-list-item-title>
                    {{ position.name }}
                  </v-list-item-title>
                </v-list-item-content>
              </v-list-item>
            </v-list>
          </v-list-item-content>
          <v-list-item-action style="align-self: unset;">
            {{ work.timeframe }}
          </v-list-item-action>
        </v-list-item>
      </v-list>
    </v-card-text>
  </v-card>
</template>
<script>
export default {
  data: () => ({
    works: [
      {
        image: "tiket-com-200.jpg",
        link: "https://www.tiket.com/",
        name: "tiket.com",
        description: "description",
        positions: [
          {
            name: "software engineer",
          },
        ],
        position: "software engineer",
        timeframe: "05/2019 - present",
      },
      {
        image: "logo.png",
        link: "https://vembry.github.io/",
        name: "freelance",
        description: "description",
        position: "fullstack engineer",
        positions: [
          {
            name: "fullstack engineer",
          },
        ],
        timeframe: "02/2019 - present",
      },
      {
        image: "binus-logo.png",
        link: "https://www.binus.edu/",
        name: "bina nusantara group",
        description: "description",
        position: "junior programmer",
        positions: [
          {
            name: "junior programmer",
          },
          {
            name: "associate system analyst",
          },
        ],
        timeframe: "03/2017 - 02/2019",
      },
    ],
  }),
};
</script>
