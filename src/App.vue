<template>
  <v-app>
    <v-container fill-height>
      <v-row justify="center" align="center">
        <v-col cols="12" class="text-center">
          <h1 class="display-4">Noe Ocanas's Portfolio</h1>
        </v-col>
        <v-col cols="12" class="text-center display-1">
          <p>ngocanas15@gmail.com</p>
        </v-col>
        <v-col cols="12">
          <v-container>
            <v-row justify="center">
              <v-col v-for="(project, index) in projects" :key="index">
                <v-card max-width="344" class="mx-auto">
                  <v-list-item>
                    <v-list-item-content>
                      <v-list-item-title class="headline">{{project.name}}</v-list-item-title>
                    </v-list-item-content>
                  </v-list-item>

                  <v-img :src="project.screenshot" contain height="194"></v-img>

                  <v-card-text>{{project.description}}</v-card-text>

                  <v-card-actions>
                    <v-btn
                      text
                      color="black accent-4"
                      :href="project.url"
                      target="_blank"
                    >Go to sites</v-btn>

                    <div class="flex-grow-1"></div>

                    <v-btn icon>
                      <v-icon>mdi-share-variant</v-icon>
                    </v-btn>
                  </v-card-actions>
                </v-card>
              </v-col>
            </v-row>
          </v-container>
        </v-col>
      </v-row>
    </v-container>
  </v-app>
</template>

<script>
export default {
  name: "App",
  data: () => ({
    projects: [
      {
        name: "Vue To do Application",
        description:
          "A simple to do application who handles completed and pending tasks, it also keeps records of total task per bucket",
        screenshot: "/images/vue-todo.PNG",
        url: "https://todo.noe-ocanas.site"
      },
      {
        name: "Marvel Finder",
        description:
          "Using Marvel Public API, we have a simple character finder application, with character descriptions and some comics where the character appears",
        screenshot: "/images/marvelfinder.PNG",
        url: "https://marvelfinder.noe-ocanas.site"
      },
      {
        name: "Super Awesome App",
        description:
          " The coolest and better social Network ever created (by me)",
        screenshot: "/images/super-awesome-app.PNG",
        url: "https://superawesomeapp.noe-ocanas.site"
      }
    ]
  })
};
</script>
