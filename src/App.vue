          //el-menu-item index="/donate">
          //打赏/改需求
          //el-menu-item>
          //el-menu-item index="/group">
          //交流/进群聊
          //el-menu-item>
<template>
  <el-card>
    <el-row type="flex" justify="center">
      <el-col :span="2">

        <el-menu 
          router
          background-color="#545c64" 
          text-color="#ffffff"
          :default-active="$route.path"
          style="height: 750px;"
        >
          <el-menu-item index="/">
            首页/生成器
          </el-menu-item>

        </el-menu>
      </el-col>
      <el-col :span="22">
        <router-view></router-view>
      </el-col>
    </el-row>
  </el-card>

  <div id="kefu">
    <el-popover width="200" placement="left-end" trigger="hover">
      <p style="text-align: center;扫一扫联系我"><b></b></p>
      <img src="./assets/wechat.jpg" style="width: 100%;" />
      <template #reference>
        <el-icon>
          <User />
        </el-icon>
      </template>
    </el-popover>
    <el-popover width="200" placement="left-end" trigger="hover">
      <p style="text-align: center;扫一扫关注微信公众号"><b></b></p>
      <img src="./assets/gzh.jpg" style="width: 100%;" />
      <template #reference>
        <el-icon>
          <ChatDotRound />
        </el-icon>
      </template>
    </el-popover>
    <el-popover width="200" placement="left-end" trigger="hover">
      <p style="text-align: center;"><b>欢迎关注我的主页</b></p>
      <p style="text-align: center; margin: .2rem 0;">龙的主页: <el-link href="https://home.long0617.cn/" target="_blank" type="primary">点击访问➢</el-link></p>
      <template #reference>
        <el-icon>
          <Link />
        </el-icon>
      </template>
    </el-popover>
  </div>
</template>

<script>
</script>

<style scoped>
#kefu .el-icon {
  width: 40px;
  height: 40px;
  color: #E65A65;
  border: 1px gray dashed;
  border-radius: 50%;
  margin: 0.3rem 0;
  cursor: pointer;
}

#kefu {
  position: fixed;
  right: 10px;
  bottom: 50%;
  z-index: 999;
  width: 60px;
  height: 60px;
}
</style>
