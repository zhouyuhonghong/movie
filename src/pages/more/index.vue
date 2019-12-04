<template>
  <div >
    <i-grid i-class="no-border">
    <i-grid-item v-for="grid in grids" :key="grid" i-class="no-border">
        <i-grid-icon>
            <image src="grid.image" />
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
        {name:"电影1",actors:"主演1",image:"https://i.loli.net/2017/08/21/599a521472424.jpg",remark:"介绍1"},
        {name:"电影2",actors:"主演2",image:"https://i.loli.net/2017/08/21/599a521472424.jpg",remark:"介绍2"},
        {name:"电影3",actors:"主演3",image:"https://i.loli.net/2017/08/21/599a521472424.jpg",remark:"介绍3"},
        {name:"电影4",actors:"主演4",image:"https://i.loli.net/2017/08/21/599a521472424.jpg",remark:"介绍4"}
      ],
    }
  },

  methods: {
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
