<template>
  <div >
    <i-grid i-class="no-border">
      <i-grid-item @click="goType(grid)" v-for="grid in grids" :key="grid" i-class="no-border">
        <i-grid-icon>
            <image :src="grid.image" />
            
        </i-grid-icon>
        <i-grid-label>{{grid.title}}</i-grid-label>
      </i-grid-item>
    </i-grid>
<i-panel :title="title_name">
    <view style="padding: 15px;">
      <i-card v-for="item in top" :key="item" i-class="split" :extra="item.name" :thumb="item.image">
          <view slot="content">{{item.remark}}</view>
          <view slot="footer">{{item.actors}}</view>
      </i-card>
    </view>
</i-panel>
</div>
</template>

<script>
export default {
  data () {
    return{
      title_name: "热门",
      grids: [
        {title:"爱情",image:"/static/images/1.png"},
        {title:"喜剧",image:"/static/images/1.png"},
        {title:"科幻",image:"/static/images/1.png"},
        {title:"惊悚",image:"/static/images/1.png"},
        {title:"犯罪",image:"/static/images/1.png"}
      ],
      top: [
        {name:"淘金记",actors:"查理·卓别林、佐治雅·凯尔等",image:"https://p1.ssl.qhimg.com/t0134ae84c70352997e.jpg",remark:"一个流浪汉从淘金到成为富翁并收获爱情的故事。"},
        {name:"少年的你",actors:"周冬雨、易烊千玺等",image:"http://mobile.pic.people.com.cn/thumbs/320/448/data/cms/NMediaFile/2018/0911/WIRELESS201809111410000124518414336.jpg",remark:"在高考前夕，被一场校园意外改变命运的两个少年，如何守护彼此成为想成为的成年人的故事。"},
        {name:"我和我的祖国",actors:"葛优、黄渤等",image:"https://p1.ssl.qhimg.com/t01dec5a57b19c3c59d.png",remark:"新中国成立70年间普通百姓与共和国息息相关的故事。"},
        {name:"罗生门",actors:"三船敏郎、京町子等",image:"https://p1.ssl.qhimg.com/t019b43beca6be258bd.jpg",remark:"一起由武士被杀而引起的一宗案件以及案件发生后人们之间互相指控对方是凶手的的种种事情以及经过。"}
      ],
    }
  },

  methods: {
    goType(type){
      console.log(type)
      let url = '../list/main?type=' + type.title
      mpvue.navigateTo({ url })
    }
  },

  created () {
  }
}
</script>

<style scoped>
div >>> .no-border {
  border-width: 0pt;
}
div >>> .split {
  margin-bottom: 10pt;
}
</style>
