<template>
  <v-row justify="center" align="center">
    <v-col>
      <v-carousel
        cycle
        height="95vh"
        hide-delimiter-background
        hide-delimiters
        show-arrows-on-hover
        progress
      >
        <v-carousel-item
          v-for="(slide, i) in slides"
          :key="i"
        >
          <v-sheet
            :color="colors[1]"
            width="100%"
            height="100%"
          >
            <v-row
              class="fill-height"
              align="center"
              justify="center"
            >
              <div class="text-h2">
                {{ slide }} Slide
              </div>
            </v-row>
          </v-sheet>
        </v-carousel-item>
      </v-carousel>
    </v-col>
  </v-row>
</template>

<script>

export default ({
  data () {
    return {
      colors: [
        'indigo',
        'warning',
        'pink darken-2',
        'red lighten-1',
        'deep-purple accent-4',
      ],
      slides: [],
    }
  },
  mounted () {
    const maxSize = 100
    for (let i=0; i<=maxSize; i++) {
      this.slides.push(`${i}`)
    }
  },
})
</script>
