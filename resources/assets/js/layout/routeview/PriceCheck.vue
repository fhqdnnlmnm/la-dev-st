<template>
    <div class="seachbar">
            <el-container>
              <el-header>
                {{message}}
              </el-header>
              <el-container>
                <el-aside>
                  {{message}}
                </el-aside>
                <el-container>
                  <el-main>
                     <el-row>
                         {{origin.value}}
                      <origin-port v-model="origin.value" col=4 placeholder="输入中/英文" label="始发港" v-bind:states ="origin.originports"
                        >
                      </origin-port>
                      {{dest.value}}
                      <dest-port v-model="dest.value" col=4 placeholder="输入中/英文" label="目的港" v-bind:options="dest.options">
                      </dest-port>
                      </el-row>
                  </el-main>
                  <el-footer>
                    {{message}}
                  </el-footer>
                </el-container>
              </el-container>
            </el-container>
    </div>
</template>
<script>
export default {
    name:'pricecheck',
    data () {
      return {
          message:'test',
          origin:{
            originports:["Alabama", "Alaska", "Arizona",
          "Arkansas", "California", "Colorado",
          "Connecticut", "Delaware", "Florida",
          "Georgia", "Hawaii", "Idaho", "Illinois",
          "Indiana", "Iowa", "Kansas", "Kentucky",
          "Louisiana", "Maine", "Maryland",
          "Massachusetts", "Michigan", "Minnesota",
          "Mississippi", "Missouri", "Montana",
          "Nebraska", "Nevada", "New Hampshire",
          "New Jersey", "New Mexico", "New York",
          "North Carolina", "North Dakota", "Ohio",
          "Oklahoma", "Oregon", "Pennsylvania",
          "Rhode Island", "South Carolina",
          "South Dakota", "Tennessee", "Texas",
          "Utah", "Vermont", "Virginia",
          "Washington", "West Virginia", "Wisconsin",
          "Wyoming"],
            value:''
          },
          dest:{
            value:'',
            options: [{
          label: '热门城市',
          options: [{
            value: 'Shanghai',
            label: '上海'
          }, {
            value: 'Beijing',
            label: '北京'
          }]
        }, {
          label: '城市名',
          options: [{
            value: 'Chengdu',
            label: '成都'
          }, {
            value: 'Shenzhen',
            label: '深圳'
          }, {
            value: 'Guangzhou',
            label: '广州'
          }, {
            value: 'Dalian',
            label: '大连'
          }]
        }]
          }
      }
    },
    methods: {
    },
    created () {

    },
    mounted () {
    }
}
</script>

<style>
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
    background-color: #E9EEF3;
    color: #333;
    text-align: center;
    line-height: 160px;
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
  .bg-purple-dark {
    background: #99a9bf;
  }
  .grid-content {
    border-radius: 4px;
    min-height: 36px;
  }
</style>

