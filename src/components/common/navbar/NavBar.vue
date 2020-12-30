<template>
    <div class="nav-bar">
        <div class="left"><slot name="left"></slot></div>
        <div class="right">
            <slot name="right"></slot>
            <div class="nav" @click="btnShow()"></div>
            <div class="nav-son" :class="{l:isShow}">
                <div class="nav-bar-xiao">
                    <div class="nav-son-xiao" @click="btn2Show()">×</div>
                </div>
                <div class="item">
                    <ul>
                        <li><a href="#">首页</a></li>
                        <li><a href="#">关于 Lambda</a></li>
                        <li><a href="#">开发者文档</a></li>
                        <li><a href="#">钱包</a></li>
                        <li><a href="#">Lambda Eco</a></li>
                        <li><a href="#">技术探索</a></li>
                        <li><a href="#">公告栏</a></li>
                        <li><a href="#">中文</a></li>
                    </ul>
                </div>
            </div>
        </div>   
    </div>
</template>

<script>
export default {
    name: "NavBar",
    components: {
    },
    data: function(){
        return {
        isShow: true
        }
    },
    methods: {
        btnShow() {
            // console.log("....");
            this.isShow = true
        },
        btn2Show() {
            // console.log("....");
            this.isShow = false
        }
    }
}
</script>

<style scoped>
  .nav-bar {
      width: 100%;
      display: flex;
      height: 64px;
      line-height: 64px;
      padding: 0 15px;
      background-color: rgb(57, 65, 187);
  }

  .left {
      flex: 1;
  }

  .right {
      position: relative;
      width: 50px;
      height: 64px;
      /* background-color: red; */
  }



  .nav {
      position: absolute;
      right: 0;
      top:50%;
      transform: translateY(-50%);
      width: 25px;
      height: 25px;
      background-color: #fff;
      border:1px solid pink;
  }
  
  .nav-son {
      position: absolute;
      top: 0;
      right: -271px;
      width: 256px;
      height: 568px;
      background-color: blue;
      transition: all 0.5s;
      /* z-index: 9; */
  }

  .l {
    position: absolute;
    top: 0;
    right: -15px;
  }


  .nav-bar-xiao {
      width: 100%;
      display: flex;
      height: 64px;
      /* line-height: 64px; */
      /* padding: 0 15px; */
      background-color:#fff;
      border-bottom: 1px solid rgb(232, 232, 232);
  }

  .nav-son-xiao {
      position: absolute;
      top: 0;
      right: 0;
      width: 56px;
      height: 56px;
      font-size: 36px;
      line-height: 56px;
      text-align: center;
  }

  .item {
      /* position: absolute; */
      /* top:56px; */
      width: 256px;
      height: 432.03px;
      padding: 28px;
      background-color: yellowgreen;
      /* box-shadow: 0 3px 5px rgba(0,0,0,.3); */
  }
  
  .item ul {
      width: 208px;
      height: 384.03px;
  }

  .item ul li {
      width: 208px;
      height: 40px;
      line-height: 40px;
      font-size: 14px;
  }
</style>