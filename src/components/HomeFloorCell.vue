<template>
  <div class="container">
    <image class="image" src='http://images.jxsg.test/mobile_index/2018/03/bfad952061ab35291e94c8c674b76df1.png'></image>
    <scroller class="list" scroll-direction="horizontal">
      <template v-for="goods in floor.list" >

        <!-- <cell> -->
          <div class="goods">
            <image class="goodsImg" src="http://images.jxsg.test/thumb/goods/wap/201510/source_img/344_G_1445569351159.jpg"></image>
          </div>
        <!-- </cell> -->
      </template>

    </scroller>
  </div>
</template>

<script>

export default {
  name: 'HomeFloorCell',
  props: ['floor']
}

</script>


<style scoped>

.container {
  margin-top: 16px;
  width: 750px;
  height: 520px;
}
.image {
  width: 750px;
  height: 380px;
}
.list {
  width: 750px;
  position: absolute;
  top: 285px;
  height: 215px;
  flex-direction: row;
  flex-wrap: wrap;
}

.goods {
  margin-left: 20px;
}

.goodsImg {
  width: 130px;
  height: 130px;
}

</style>
