<template>
  <div>
    <sample-component :title="indexTitle">
      <div class="come">
        slot example
      </div>
    </sample-component>
    <nuxt-link to="/about">ABOUT</nuxt-link>
  </div>
</template>

<script>
import SampleComponent from '~/components/SampleComponent.vue'

export default {
  components: {
    SampleComponent
  },
  data() {
    return {
      indexTitle: 'Nuxt.js data'
    }
  }
}
</script>
