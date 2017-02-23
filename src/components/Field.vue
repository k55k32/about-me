<template lang="pug">
.field {{name}}
  .mark {{value}}
  slot
</template>

<script>
export default {
  props: ['name', 'value']
}
</script>

<style lang="css">
</style>
