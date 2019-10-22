<template>
  <v-container>
    <v-row>
      <v-col cols="12">
          <v-container fluid>
            <v-row>
              <v-col
                v-for="n in 24"
                :key="n"
                class="d-flex child-flex"
                cols="2"
              >
                <v-card flat tile class="d-flex" @click="message(n)">
                  <v-img
                    :src="`https://picsum.photos/500/300?image=${n * 5 + 10}`"
                    aspect-ratio="1"
                    class="grey lighten-2 white--text align-end"
                    gradient="to bottom, rgba(0,0,0,.1), rgba(0,0,0,.5)"
                  >
                  <v-card-title v-text="`Animal ${n}`"></v-card-title>
                  </v-img>
                </v-card>
              </v-col>
            </v-row>
          </v-container>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {
  name: 'AnimalCards',
  methods: {
    message (val) {
      alert(`You clicked Animal ${val}`)
    }
  }
}
</script>
