<template>
  <div>
    <v-container>
      <v-row>
        <v-col cols="2">
          <v-sheet rounded="lg">
            <v-list color="transparent">
              <v-list-item
                v-for="feature in featureList"
                :key="feature.name"
                :to="{name: feature.pathName}"
              >
                <v-list-item-content>
                  <v-list-item-title>
                    {{ feature.name }}
                  </v-list-item-title>
                </v-list-item-content>
              </v-list-item>
            </v-list>
          </v-sheet>
        </v-col>

        <v-col>
          <v-sheet
            min-height="70vh"
            rounded="lg"
          >
            <router-view />
          </v-sheet>
        </v-col>
      </v-row>
    </v-container>
  </div>
</template>

<script>
export default {
  data: () => ({
    featureList: [
      {
        name: 'Draggable',
        pathName: 'Draggable'
      }
    ]
  })
}
</script>
