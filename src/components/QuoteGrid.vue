<template>
  <div class="row">
    <quote v-for="(quote, index) in quotesss" @click.native="deleteQuote(index)" :key="quote">{{ quote }}</quote>
  </div>
</template>

<script>
import Quote from './Quote'

export default {
  props: ['quotesss'],
  components: {
    Quote
  },
  methods: {
    deleteQuote(index) {
      this.$emit('quoteDel', index)
    }
  }
}
</script>

<style scoped>

</style>
