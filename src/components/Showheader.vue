<template>
    <div class="show-header-box">
        <cheader style="z-index: 599;"><span slot="title">Title as slot</span></cheader>
        <cheader style="top: 66px;z-index: 599;"
          :title="'Title as props'"></cheader>
        <cheader style="top: 130px;z-index: 599"
          :rightType="{showRight: false}"><span slot="title">header without right</span></cheader>
        <cheader style="top: 194px;z-index: 599"
          :rightType="{showType: 'dot'}"><span slot="title">dot right</span></cheader>
        <cheader style="top: 258px;z-index: 599">
            <span slot="title">custom right</span>
            <span slot="right">选项</span>
        </cheader>
        <cheader style="top: 322px;z-index: 599"
          :leftType="{showLeftText: false}"><span slot="title">left back without text</span></cheader>
        <cheader style="top: 386px;z-index: 599"
          :leftType="{showLeft: false}"><span slot="title">no left back</span></cheader>
          <div class="show-header-des">
              <h4>属性</h4>
                <c-table class="atrribute-table"
                  :responsive="true">  
                  <thead>
                      <tr>
                          <th>属性名</th>
                          <th>类型</th>
                          <th>默认值</th>
                          <th>说明</th>
                      </tr>
                  </thead>
                  <tbody>
                      <tr>
                          <td>title</td>
                          <td><span>String</span></td>
                          <td></td>
                          <td>标题</td>
                      </tr>
                      <tr>
                          <td>rightType.showRight</td>
                          <td><span>Boolean</span></td>
                          <td>true</td>
                          <td>是否显示右边</td>
                      </tr>
                      <tr>
                          <td>rightType.showType</td>
                          <td><span>String</span></td>
                          <td>text</td>
                          <td>右边显示类型，text文字，dot点</td>
                      </tr>
                      <tr>
                          <td>leftType.showLeft</td>
                          <td><span>Boolean</span></td>
                          <td>true</td>
                          <td>是否显示左边</td>
                      </tr>
                      <tr>
                          <td>leftType.showLeftText</td>
                          <td><span>Boolean</span></td>
                          <td>true</td>
                          <td>是否显示左边文字</td>
                      </tr>
                  </tbody>
              </c-table>
          </div>
          <h3>
            <a href="https://github.com/TYC-dev/little-toolkit/blob/master/src/components/Cheader/Cheader.vue">组件源码</a>
          </h3>
          <h3>
              <a href="https://github.com/TYC-dev/little-toolkit/blob/master/src/components/Showheader.vue">demo源码</a>
          </h3>
    </div>
</template>

<script>
    import Cheader from './Cheader/Cheader' 
    import CTable from './CTable/CTable'
    export default{
        name: 'showcheader',
        components: {
            Cheader,
            CTable
        }
    }
</script>

<style lang="less">
    .show-header-des{
        text-align: left;
        margin-top: 430px;
        //overflow-y: scroll;
        h4{
            padding-left: 10px;
        }
    }
</style>
