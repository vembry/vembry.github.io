<template>
  <v-card outlined tile>
    <v-card-title>technical skills</v-card-title>
    <v-card-text>
      <ul>
        <li>
          Experienced in
          <template v-for="(techStack, index) in techStacks">
            <b :key="`techstack-${index}`">{{ techStack }}</b>
            <span :key="index" v-if="index != languages.length - 1">, </span>
          </template>
        </li>
        <li>
          Experienced on writing web application in
          <template v-for="(language, index) in languages">
            <b :key="`language-${index}`">{{ language }}</b>
            <span :key="index" v-if="index != languages.length - 1">, </span>
          </template>
        </li>
      </ul>
    </v-card-text>
  </v-card>
</template>
<script>
export default {
  data: () => ({
    techStacks: [
      "Spring Java",
      "NodeJs",
      "ExpressJs",
      "VueJs",
      "Django Python",
      "Echo Go",
      "Laravel",
      ".NET MVC",
      "Nginx",
      "Databases",
    ],
    languages: [
      "Java",
      "Javascript",
      "Python",
      "C#",
      "PHP",
      "Go",
      "HTML",
      "CSS",
    ],
  }),
};
</script>
