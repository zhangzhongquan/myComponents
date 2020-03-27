<template>
  <div ref="home" class="home">
    <div class="top_box">

    </div>
    <div ref="content" class="content">
      <div ref="box" class="box">
        <div ref="add" v-for="item in list" :key="item.id" class="item">{{item.value }}</div>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  name: 'home',
  components: {},
  data () {
    return {
      list: [
        {
          id: 1,
          value: 11,
          show: false,
          children: [
            { id: 11, value: 111 },
            { id: 12, value: 112 },
            { id: 13, value: 113 },
            { id: 14, value: 114 },
            { id: 15, value: 115 },
            { id: 16, value: 116 }
          ]
        },
        {
          id: 2,
          value: 22,
          show: false,
          children: [
            { id: 21, value: 221 },
            { id: 22, value: 222 },
            { id: 23, value: 223 },
            { id: 24, value: 224 },
            { id: 25, value: 225 },
            { id: 26, value: 226 }
          ]
        },
        {
          id: 3,
          value: 33,
          show: false,
          children: [
            { id: 31, value: 331 },
            { id: 32, value: 332 },
            { id: 33, value: 333 },
            { id: 34, value: 334 },
            { id: 35, value: 335 },
            { id: 36, value: 336 }
          ]
        },
        {
          id: 4,
          value: 44,
          show: false,
          children: [
            { id: 41, value: 441 },
            { id: 42, value: 442 },
            { id: 43, value: 443 },
            { id: 44, value: 444 },
            { id: 45, value: 445 },
            { id: 46, value: 446 }
          ]
        },
        {
          id: 5,
          value: 55,
          show: false,
          children: [
            { id: 55, value: 551 },
            { id: 52, value: 552 },
            { id: 53, value: 553 },
            { id: 54, value: 554 },
            { id: 55, value: 555 },
            { id: 56, value: 556 }
          ]
        },
        {
          id: 6,
          value: 66,
          show: false,
          children: [
            { id: 61, value: 661 },
            { id: 62, value: 662 },
            { id: 63, value: 663 },
            { id: 64, value: 664 },
            { id: 65, value: 665 },
            { id: 66, value: 666 }
          ]
        },
        {
          id: 7,
          value: 77,
          show: false,
          children: [
            { id: 71, value: 771 },
            { id: 72, value: 772 },
            { id: 73, value: 773 },
            { id: 74, value: 774 },
            { id: 75, value: 775 },
            { id: 76, value: 776 }
          ]
        },
        {
          id: 8,
          value: 88,
          show: false,
          children: [
            { id: 81, value: 881 },
            { id: 82, value: 882 },
            { id: 83, value: 883 },
            { id: 84, value: 884 },
            { id: 85, value: 885 },
            { id: 86, value: 886 }
          ]
        },
        {
          id: 9,
          value: 99,
          show: false,
          children: [
            { id: 91, value: 991 },
            { id: 92, value: 992 },
            { id: 93, value: 993 },
            { id: 94, value: 994 },
            { id: 95, value: 995 },
            { id: 96, value: 996 }
          ]
        },
        {
          id: 10,
          value: 1010,
          show: false,
          children: [
            { id: 101, value: 10101 },
            { id: 102, value: 10102 },
            { id: 103, value: 10103 },
            { id: 104, value: 10104 },
            { id: 105, value: 10105 },
            { id: 106, value: 10106 }
          ]
        },
        {
          id: 11,
          value: 1111,
          show: false,
          children: [
            { id: 111, value: 11111 },
            { id: 112, value: 11112 },
            { id: 113, value: 11113 },
            { id: 114, value: 11114 },
            { id: 115, value: 11115 },
            { id: 116, value: 11116 }
          ]
        },
        {
          id: 12,
          value: 1212,
          show: false,
          children: [
            { id: 121, value: 12121 },
            { id: 122, value: 12122 },
            { id: 123, value: 12123 },
            { id: 124, value: 12124 },
            { id: 125, value: 12125 },
            { id: 126, value: 12126 }
          ]
        },
        {
          id: 13,
          value: 1313,
          show: false,
          children: [
            { id: 131, value: 13131 },
            { id: 132, value: 13132 },
            { id: 133, value: 13133 },
            { id: 134, value: 13134 },
            { id: 135, value: 13135 },
            { id: 136, value: 13136 }
          ]
        },
        {
          id: 14,
          value: 1414,
          show: false,
          children: [
            { id: 141, value: 14141 },
            { id: 142, value: 14142 },
            { id: 143, value: 14143 },
            { id: 144, value: 14144 },
            { id: 145, value: 14145 },
            { id: 146, value: 14146 }
          ]
        },
        {
          id: 15,
          value: 1515,
          show: false,
          children: [
            { id: 151, value: 15151 },
            { id: 152, value: 15152 },
            { id: 153, value: 15153 },
            { id: 154, value: 15154 },
            { id: 155, value: 15155 },
            { id: 156, value: 15156 }
          ]
        },
        {
          id: 16,
          value: 1616,
          show: false,
          children: [
            { id: 161, value: 16161 },
            { id: 162, value: 16162 },
            { id: 163, value: 16163 },
            { id: 164, value: 16164 },
            { id: 165, value: 16165 },
            { id: 166, value: 16166 }
          ]
        },
        {
          id: 17,
          value: 1717,
          show: false,
          children: [
            { id: 171, value: 17171 },
            { id: 172, value: 17172 },
            { id: 173, value: 17173 },
            { id: 174, value: 17174 },
            { id: 175, value: 17175 },
            { id: 176, value: 17176 }
          ]
        },
        {
          id: 18,
          value: 1818,
          show: false,
          children: [
            { id: 181, value: 18181 },
            { id: 182, value: 18182 },
            { id: 183, value: 18183 },
            { id: 184, value: 18184 },
            { id: 185, value: 18185 },
            { id: 186, value: 18186 }
          ]
        },
        {
          id: 19,
          value: 1919,
          show: false,
          children: [
            { id: 191, value: 19191 },
            { id: 192, value: 19192 },
            { id: 193, value: 19193 },
            { id: 194, value: 19194 },
            { id: 195, value: 19195 },
            { id: 196, value: 19196 }
          ]
        },
        {
          id: 20,
          value: 2020,
          show: false,
          children: [
            { id: 201, value: 20201 },
            { id: 202, value: 20202 },
            { id: 203, value: 20203 },
            { id: 204, value: 20204 },
            { id: 205, value: 20205 },
            { id: 206, value: 20206 }
          ]
        },
        {
          id: 21,
          value: 2121,
          show: false,
          children: [
            { id: 211, value: 21211 },
            { id: 212, value: 21212 },
            { id: 213, value: 21213 },
            { id: 214, value: 21214 },
            { id: 215, value: 21215 },
            { id: 216, value: 21216 }
          ]
        }
      ]
    }
  },
  mounted () {
    window.addEventListener('scroll', this.handleScroll,true)
  },
  methods: {
    handleScroll () {
      const eleOffsetTop = document.getElementsByClassName('content')
      console.log(eleOffsetTop)

      // console.log(this.$refs.home.scrollTop)
      console.log(this.$refs)
      // console.log('offsetTop:', this.$refs.add[1].offsetTop)
      console.log('content:', window.pageYOffset)
      // console.log('scrollTop:', this.$refs.box.scrollTop)
      // console.log('scrollHeight:', this.$refs.box.scrollHeight)
      // console.log('scrollWidth:', this.$refs.box.scrollWidth)
      // console.log('scrollLeft:', this.$refs.box.scrollLeft)

      // console.log('offsetTop:', this.$refs.content.offsetTop)
      // console.log('scrollTop:', this.$refs.content.scrollTop)
      // console.log('scrollHeight:', this.$refs.content.scrollHeight)
      // console.log('scrollWidth:', this.$refs.content.scrollWidth)
      // console.log('scrollLeft:', this.$refs.content.scrollLeft)

      // console.log('offsetTop:', this.$refs.home.offsetTop)
      // console.log('scrollTop:', this.$refs.home.scrollTop)
      // console.log('scrollHeight:', this.$refs.home.scrollHeight)
      // console.log('scrollWidth:', this.$refs.home.scrollWidth)
      // console.log('scrollLeft:', this.$refs.home.scrollLeft)
    }
  }
}
</script>
<style lang="less">
.home {
  height:100%;
  // position: relative;
  // padding-bottom: 50px;
  .top_box{
    height: 100px;
    width:100%;
    background-color: green;
  }
  .content{
    height: 800px;
    overflow: hidden;
    .box {
      height: 100%;
      overflow: scroll;
      .item {
        height: 50px;
        line-height: 50px;
        text-align: center;
        border-bottom: 1px solid red;
      }
    }
  }

}

// .box::-webkit-scrollbar {
//   width: 7px;
//   height: 7px;
//   background-color: #f5f5f5;
// }
// .box::-webkit-scrollbar-track {
//   box-shadow: inset 0 0 6px rgba(0, 0, 0, 0.3);
//   border-radius: 5px;
//   background-color: #f5f5f5;
// }
// .box::-webkit-scrollbar-thumb {
//   border-radius: 5px;
//   box-shadow: inset 0 0 6px rgba(0, 0, 0, 0.3);
//   background-color: #555;
// }
</style>
