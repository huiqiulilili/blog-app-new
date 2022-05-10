<template>
  <el-card>
    <h1 class="me-author-name">追月亮的猫</h1>
    <div class="me-author-description">
      <span><i class="el-icon-location-outline"></i> &nbsp;陕西&西安</span>
      <span><i class="me-icon-job"></i> &nbsp;java爱好者</span>
    </div>
    <div class="me-author-tool">
<!--      <i @click="showTool(qq)" :title="qq.title" class="iconfont icon-qq"></i>-->
<!--      <i @click="showTool(bilibili)" :title="bilibili.title" class="iconfont icon-bilibili-fill"></i>-->
      <section>
        <div class="r1-head">
          <img
            src="/static/img/img01.jpg"
            alt=""
          />
        </div>
        <div class="r1-body">
          <div class="catch-me">
            <div class="">
              <el-tooltip class="item" content="Github" placement="top">
                <a :href="catchMeObj.git" target="_blank"
                ><i class="fa fa-fw fa-github">github</i
                ></a>
              </el-tooltip>
              <el-tooltip
                class="item"
                effect="dark"
                content="CSDN"
                placement="top"
              >
                <a :href="catchMeObj.csdn" target="_blank"><i class="">CSDN</i></a>
              </el-tooltip>
            </div>

          </div>
        </div>
      </section>
    </div>
  </el-card>

</template>

<script>
  export default {
    name: 'CardMe',
    data() {
      return {
        qq: {title: 'QQ', message: '723663826'},
        bilibili: {
          title: '哔哩哔哩',
          message: '<a target="_blank" href="https://space.bilibili.com/473844125">https://space.bilibili.com/473844125</a>'
        },
        catchMeObj: {
          //个人信息
          git: "https://github.com/huiqiulilili?tab=repositories",
          csdn: "https://mp.csdn.net/mp_blog/manage/article?spm=1011.2415.3001.5448",
        },
      }
    },
    methods: {
      showTool(tool) {
        this.$message({
          duration: 0,
          showClose: true,
          dangerouslyUseHTMLString: true,
          message: '<strong>' + tool.message + '</strong>'
        });
      }
    }
  }
</script>

<style scoped>
  .me-author-name {
    text-align: center;
    font-size: 30px;
    border-bottom: 1px solid #5FB878;
  }

  .me-author-description {
    padding: 8px 0;
  }

  .me-icon-job {
    padding-left: 16px;
  }

  .me-author-tool {
    text-align: center;
    padding-top: 10px;
  }

  .me-author-tool i {
    cursor: pointer;
    padding: 4px 10px;
    font-size: 30px;
  }

  img{
    width: 100%;
    height: 100%;
  }

</style>
