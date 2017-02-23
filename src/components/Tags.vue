<template lang="pug">
.tags
  i(v-for="t in tags") {{t}}
</template>

<script>
export default {
  props: ['tags']
}
</script>

<style lang="css">
</style>
