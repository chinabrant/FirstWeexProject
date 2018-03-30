<template>
  <image class='image' :src='hot.url'>

  </image>
</template>

<script>

export default {
  name: 'HomeHotAreaCell',
  props: ['hot']
}

</script>

<style scoped>
.image {
  margin-top: 16px;
  width: 750px;
  height: 770px;
}
</style>
