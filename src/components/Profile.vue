<template>
  <v-card tile outlined>
    <v-card-title>Jeo Vembry Pratama</v-card-title>
    <v-card-subtitle>Software Engineer</v-card-subtitle>
    <v-card-text>
      <!-- summary -->
      <v-row>
        <v-col>
          derp
        </v-col>
      </v-row>

      <!-- contacts -->
      <v-row>
        <v-col>
          <v-list subheader dense>
            <v-list-item
              v-for="(contact, index) in contacts"
              :key="`contact-${index}`"
            >
              <v-list-item-icon>
                <v-icon>{{ contact.icon }}</v-icon>
              </v-list-item-icon>
              <v-list-item-content>
                <v-list-item-subtitle>
                    <template v-for="(link, index1) in contact.links" >
                        <a
                            :key="`contact-${index}-link-${index1}`"
                            :href="`${contact.isMail ? 'mailto:' : 'https://'}${link.url}`"
                            target="_blank"
                        >{{ link.as }}</a>
                        <span :key="`separator-${index1}`" v-if="index1 != contact.links.length - 1">, </span>
                    </template>
                </v-list-item-subtitle>
              </v-list-item-content>
            </v-list-item>
          </v-list>
        </v-col>
      </v-row>
    </v-card-text>
  </v-card>
</template>
<script>
export default {
  data: () => ({
    contacts: [
      {
        name: "email",
        links: [
          {
            as: "airstrip99@gmail.com",
            url: "airstrip99@gmail.com",
          },
        ],
        icon: "mdi-email",
        isMail: true,
      },
      {
        name: "linkedin",
        links: [
          {
            as: "jeo vembry pratama",
            url: "linkedin.com/in/jeo-vembry/",
          },
        ],
        icon: "mdi-linkedin",
      },
      {
        name: "github",
        links: [
          {
            as: "@vembry",
            url: "github.com/vembry",
          },
          {
            as: "@jeopratama",
            url: "github.com/jeopratama",
          },
        ],
        icon: "mdi-github",
      },
      {
        name: "gitlab",
        links: [
          {
            as: "@vembry",
            url: "gitlab.com/vembry",
          },
        ],
        icon: "mdi-gitlab",
      },
    ],
  }),
};
</script>
