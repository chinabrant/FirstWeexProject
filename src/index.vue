<template>
  <!-- <div class='wrapper'> -->
    <list switch='type' class="wrapper">
      <template v-for='item in lists'>

        <cell class="cell" v-if="item.type === 'top-function'">
          <HomeTopFunctionCell v-bind:lists='item.data' :key="top"/>
        </cell>

        <cell class="cell" v-if="item.type === 'hot-area'">
          <HomeHotAreaCell v-bind:hot="item.data" :key="hot"/>
        </cell>

        <cell class="cell" v-if="item.type === 'floor'">
          <HomeFloorCell v-bind:floor="item.data"/>
        </cell>

    </template>
    </list>

  <!-- </div> -->
</template>

<script>

import HomeTopFunctionCell from './components/HomeTopFunctionCell.vue'
import HomeHotAreaCell from './components/HomeHotAreaCell.vue'
import HomeFloorCell from './components/HomeFloorCell.vue'

// 顶部入口
const topFunction = {
  type: 'top-function',
  data: [
    {
      'title': 'first',
      'imgUrl': 'http://images.jxsg.test/mobile_index/2018/03/8ae6d731c9fd5f4b1c96bd638d1302a2.png'
    },
    {
      'title': 'second',
      'imgUrl': 'http://images.jxsg.test/mobile_index/2018/03/8ae6d731c9fd5f4b1c96bd638d1302a2.png'
    },
    {
      'title': 'third',
      'imgUrl': 'http://images.jxsg.test/mobile_index/2018/03/8ae6d731c9fd5f4b1c96bd638d1302a2.png'
    },
    {
      'title': 'fourth',
      'imgUrl': 'http://images.jxsg.test/mobile_index/2018/03/8ae6d731c9fd5f4b1c96bd638d1302a2.png'
    },
    {
      'title': 'five',
      'imgUrl': 'http://images.jxsg.test/mobile_index/2018/03/8ae6d731c9fd5f4b1c96bd638d1302a2.png'
    },
    {
      'title': 'six',
      'imgUrl': 'http://images.jxsg.test/mobile_index/2018/03/8ae6d731c9fd5f4b1c96bd638d1302a2.png'
    },
    {
      'title': 'seven',
      'imgUrl': 'http://images.jxsg.test/mobile_index/2018/03/8ae6d731c9fd5f4b1c96bd638d1302a2.png'
    },
    {
      'title': 'eight',
      'imgUrl': 'http://images.jxsg.test/mobile_index/2018/03/8ae6d731c9fd5f4b1c96bd638d1302a2.png'
    }
  ]

}

const hotArea = {
  type: 'hot-area',
  data: {
    'url': 'http://images.jxsg.test/mobile_index/2018/03/0e1a973d6646ed7f269e36b8dce9b134.png'
  }
}

const floor = {
  type: 'floor',
  data: {
    list: [
      {},
      {},
      {},
      {},
      {},
      {},
      {},
      {},
      {},
      {},
      {},
      {},
    ]
  }
}

export default {
  name: 'App',
  data () {
    return {
      lists: [
        topFunction,
        hotArea,
        floor,
        floor,
        floor,
        floor,
        floor
      ]
    }
  },

  components: {
    HomeTopFunctionCell,
    HomeHotAreaCell,
    HomeFloorCell
  }

}
</script>

<style scoped>
  .wrapper {
    width: 750px;
/* height: 750px; */
    /* height: 100%; */
  }

  .cell {
    width: 750px;
  }

</style>
