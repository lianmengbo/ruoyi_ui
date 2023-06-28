<template>
  <div class="banner">
    <div style="font-size: 12px">

    </div>
    <el-container>
      <el-header style="display: flex">
        <div class="shop-head">
          <el-dropdown trigger="hover"class="ele-body">
            <span class="el-dropdown-link">{{ dropdownTitle }}</span>
            <el-dropdown-menu slot="dropdown">
              <el-dropdown-item v-for="item in dropdownItems" :key="item.id">{{ item.text }}</el-dropdown-item>
            </el-dropdown-menu>
          </el-dropdown>
          <el-link class="ele-body" type="danger" >亲,请登录</el-link>
          <el-link class="ele-body" href="https://element.eleme.io" target="_blank">免费注册</el-link>
          <el-link class="ele-body" href="https://element.eleme.io" target="_blank">手机逛淘宝</el-link>
          <el-link class="ele-body" href="https://element.eleme.io" target="_blank">网页无障碍</el-link>
        </div>
        <div class="shop-head"></div>
        <div class="shop-head">
          <el-link class="ele-body" href="https://element.eleme.io" target="_blank">我的淘宝</el-link>
          <el-link class="ele-body" href="https://element.eleme.io" target="_blank">购物车</el-link>
          <el-link class="ele-body" href="https://element.eleme.io" target="_blank">收藏夹</el-link>
          <el-link class="ele-body" href="https://element.eleme.io" target="_blank">商品分类</el-link>
          <el-link class="ele-body" href="https://element.eleme.io" target="_blank">免费开店</el-link>
          <el-link class="ele-body" href="https://element.eleme.io" target="_blank">千牛卖家中心</el-link>
          <el-link class="ele-body" href="https://element.eleme.io" target="_blank">联系客服</el-link>
        </div>
      </el-header>
      <el-main style="display: flex; background-color: #E7E4E5;">
        <div style="flex: 1;" >
          <img src="@/assets/images/taobao.png" alt="dark"/>
        </div>
        <div style="flex: 3">
          <div >
            <el-input placeholder="请输入内容" v-model="input3" class="input-with-select">
              <el-select ref="selectRef" v-model="select" slot="prepend">
                <el-option label="宝贝" value="1"></el-option>
                <el-option label="天猫" value="2"></el-option>
                <el-option label="店铺" value="3"></el-option>
              </el-select>
              <el-button slot="append" icon="el-icon-search">搜索</el-button>
            </el-input>
          </div>
        </div>
        <div style="flex: 1">

        </div>

      </el-main>
      <el-main style="display: flex; background-color: #E7E4E5;">

            <div style="flex :2" >

            </div>
            <div style="flex :8" class="main-body">
              <daohang></daohang>
              <div>猜你喜欢</div>
              <div>商品</div>
            </div>
            <div style="flex :2">

            </div>
      </el-main>

<!--      </el-container>-->
    </el-container>
    <el-footer>Footer</el-footer>



  </div>

</template>

<script>
  import daohang from "../components/shop/daohang";
  export default {
    name: "shop",
    components:{
      daohang,
    },
    data() {
      return {
        dropdownTitle: '中国大陆',
        dropdownItems: [
          { id: 1, text: '选项一' },
          { id: 2, text: '选项二' },
          { id: 3, text: '选项三' },
        ],
        options: [{
          value: '选项1',
          label: '黄金糕'
        }, {
          value: '选项2',
          label: '双皮奶'
        }, {
          value: '选项3',
          label: '蚵仔煎'
        }, {
          value: '选项4',
          label: '龙须面'
        }, {
          value: '选项5',
          label: '北京烤鸭'
        }],
        value: '中国大力',
        input3: '',
        select: '宝贝',
      }
    },
    mounted() {

    },
    methods:{
      openSelect(){

      }
    }
  }

</script>
<style>
  .el-select .el-input {
    width: 130px;
  }
  .input-with-select .el-input-group__prepend {
    background-color: #fff;
  }

</style>

<style scoped>
  .main-body{
    margin-top: -10px;
    border-radius: 18px 18px 18px 18px;
    background-color: #ffffff;

  }
  .banner{
    height: 35px;
  }
  .shop-head {
    flex: 1;
  }
  .ele-body{
    margin-right: 10px;
  }

  .el-header, .el-footer {
    background-color: #B3C0D1;
    color: #333;
    text-align: center;
    line-height: 60px;
  }

  .el-aside {
    background-color: #D3DCE6;
    color: #333;
    text-align: center;
    line-height: 200px;
  }

  .el-main {
    background-color: #FFFFFF;;
    color: #333;
    text-align: center;
    line-height: 80px;
  }

  body > .el-container {
    margin-bottom: 40px;

  }

  .el-container:nth-child(5) .el-aside,
  .el-container:nth-child(6) .el-aside {
    line-height: 260px;
  }

  .el-container:nth-child(7) .el-aside {
    line-height: 320px;
  }
</style>
