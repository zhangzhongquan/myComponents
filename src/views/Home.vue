<template>
  <div class="home">
    <ul class="tab_box">
      <template v-for="v in tabList" >
          <li  :key="v.value"  style="width:50%;height:60px;fontSize:24px;background:gray">
            <p>{{v.tabName}}</p>
            <div class= "select_border" ></div>
          </li>

      </template>
    </ul>
    <ul >
      <li style="marginBottom:30px;background:gray;" v-for="item in list" :key="item.id" @click="clickItem(item)">
        <p>{{item.title}}</p>
         <transition name='fade'>
        <ul v-if="item.isShow">
          <li style="background:#fff;height:30px" v-for="citem in item.childList" :key="citem.id" @click='clickToAbout(citem.title)'>
            <p>{{citem.title}}</p>
          </li>
        </ul>
          </transition>
      </li>
    </ul>
  </div>
</template>
<script>
export default {
  name: 'home',
  data () {
    return {
      list: [
        {
          id: 1,
          title: '鸡蛋',
          isShow: false,
          childList: []
        },
        {
          id: 2,
          title: '水产',
          isShow: false,
          childList: []
        },
        {
          id: 3,
          title: '生鲜',
          isShow: false,
          childList: []
        }
      ],
      childList1: [
        {
          id: 11,
          title: '鸡蛋11'
        },
        {
          id: 12,
          title: '水产12'
        },
        {
          id: 13,
          title: '生鲜13',
          isShow: false
        }
      ],
      childList2: [
        {
          id: 21,
          title: '鸡蛋21'
        },
        {
          id: 22,
          title: '水产22'
        },
        {
          id: 23,
          title: '生鲜23'

        }
      ],
      childList3: [
        {
          id: 31,
          title: '鸡蛋31'
        },
        {
          id: 32,
          title: '水产32'
        },
        {
          id: 33,
          title: '生鲜33'
        }
      ],
      tabList: [{
        value: 0,
        tabName: '左边'
      }, {
        value: 1,
        tabName: '右边'
      }]
    }
  },
  components: {

  },
  methods: {
    clickItem (val) {
      this.list.forEach((item, index) => {
        if (val.id === item.id) {
          item.isShow = !item.isShow
          switch (index) {
            case 0:
              item.childList = this.childList1
              break
            case 1:
              item.childList = this.childList2
              break
            case 2:
              item.childList = this.childList3
              break
          }
        }
      })

      console.log(val)
    }
  }
}
</script>

<style lang="less" scoped>
.fade-enter-active,.fade-leave-active{
  transition: opacity 0.5s;
}
.fade-enter,.fade-leave-to{
  opacity: 0.1 ;
}

.tab_box{
  display: flex;
   background-color: gray;
}
.select_border{
  color:red
}
</style>
