<script>
export default {
  props: {
    filters: {
      type: Array,
      default: () => []
    }
  },
  data() {
    return {
      logs: []
    }
  },
  watch: {
    filters: function () {
      console.log('watch filters');
      this.logs.push('watch filters emited.')
    }
  }
}

</script>

<template>
  <pre>{{ logs }}</pre>
</template>