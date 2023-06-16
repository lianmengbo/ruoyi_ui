<template>
  <div class="app-container home">
    <div class="box-pie" style="height: 400px" ref="chart"></div>
    <index_2></index_2>
  </div>

</template>
<script>
import echarts from 'echarts'
import index_2 from "./components/index/index_2";
export default {
  components:{
    index_2
  },
  name: "Index",
  data(){
    return {
      chart:null,
      // 配置可视化图形
      option:  {
        title: {
          text: '今天我们过周五啊',
          subtext: '可不可以啊',
          left: 'center'
        },
        tooltip: {
          trigger: 'item'
        },
        legend: {
          orient: 'vertical',
          left: 'left'
        },
        series: [
          {
            name: '有点东西哈',
            type: 'pie',
            radius: '50%',
            data: [
              { value: 1048, name: '花里胡哨' },
              { value: 735, name: '乱七八糟' },
              { value: 580, name: '牛逼的很' },
              { value: 484, name: '吃屎去吧' },
              { value: 300, name: '今天周五' }
            ],
            emphasis: {
              itemStyle: {
                shadowBlur: 10,
                shadowOffsetX: 0,
                shadowColor: 'rgba(0, 0, 0, 0.5)'
              }
            }
          }
        ]
      }
    }
  },
  mounted() {
    this.getPage();
  },
  methods:{
    getPage() {
      // 引用chart并初始化
      this.chart = this.$echarts.init(this.$refs.chart);
      // 使用刚指定的配置项和数据显示图表。
      this.chart.setOption(this.option);
    }
  }

};
</script>

<style scoped lang="scss">
.home {
  blockquote {
    padding: 10px 20px;
    margin: 0 0 20px;
    font-size: 17.5px;
    border-left: 5px solid #eee;
  }
  hr {
    margin-top: 20px;
    margin-bottom: 20px;
    border: 0;
    border-top: 1px solid #eee;
  }
  .col-item {
    margin-bottom: 20px;
  }

  ul {
    padding: 0;
    margin: 0;
  }

  font-family: "open sans", "Helvetica Neue", Helvetica, Arial, sans-serif;
  font-size: 13px;
  color: #676a6c;
  overflow-x: hidden;

  ul {
    list-style-type: none;
  }

  h4 {
    margin-top: 0px;
  }

  h2 {
    margin-top: 10px;
    font-size: 26px;
    font-weight: 100;
  }

  p {
    margin-top: 10px;

    b {
      font-weight: 700;
    }
  }

  .update-log {
    ol {
      display: block;
      list-style-type: decimal;
      margin-block-start: 1em;
      margin-block-end: 1em;
      margin-inline-start: 0;
      margin-inline-end: 0;
      padding-inline-start: 40px;
    }
  }
}
</style>

