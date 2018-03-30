<template>
  <div class="container">


      <div v-for="item in lists" class="item">
        <image class="image" v-bind:src="item.imgUrl" resize="stretch"></image>
        <text class="text">{{ item.title }}</text>
      </div>

  </div>
</template>

<script>

export default {
  name: 'HomeTopFunctionCell',
  props: ['lists'],
  // data () {
  //   lists: {}
  // }
}
</script>


<style scoped>

.container {
  flex-direction: row;
  align-content: flex-start;
  width: 750px;
  flex-wrap: wrap;
}

.item {
  margin-top: 20px;
  margin-left: 20px;
  width: 162.5px;
  height: 205px;
  background-color: #ff0000;
  justify-content: space-between;
}
.image {
  align-self: center;
  width: 162.5px;
  height: 162.5px;
  background-color: #00ff00;
}
.text {
  text-align: center;
  width: 100%;

}
</style>
