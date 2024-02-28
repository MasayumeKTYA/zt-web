<template>
  <div class="two_content">
    <a-button type="primary" class="two_btn">添加产品</a-button>
    <div class="two_font">
      购进总指标（万元）：<span class="two_font1">￥152.65元</span>
    </div>
    <div class="two_font">
      指标按季度分解（万元）：
      <span class="two_font1"
        >【Q1】￥12.5，【Q2】￥12.5，【Q3】￥12.5，【Q4】￥12.5</span
      >
    </div>
    <div class="two_font">
      纯销总指标（万元）：<span class="two_font1">￥152.65元</span>
    </div>
  </div>
  <div class="two_box">
    <div class="two_header">
      <div style="margin-left: 50px">
        产品: <a-button>选择产品</a-button>
        <span class="num">美复胶丸&nbsp&nbsp&nbsp24粒/盒</span>
      </div>
      <div style="margin-left: 50px" class="two_header_th">
        <span style="width: 50px">产品:</span>
        <a-input value="2020-02-01 ~ 2020-05-01" />
      </div>
      <a-button class="delect">删除</a-button>
    </div>
    <div class="input_box">
      <div class="input_box_header">
        <div style="flex: 1; padding: 10px">协议价（元）</div>
        <div style="flex: 1; padding: 10px">票折（元）</div>
        <div style="flex: 1; padding: 10px">购进指标量（大单位）</div>
        <div style="flex: 1; padding: 10px">购进指标量（小单位）</div>
        <div style="flex: 1; padding: 10px">购进金额（万元）</div>
        <div style="flex: 1; padding: 10px">纯销指标量（小单位）</div>
        <div style="flex: 1; padding: 10px">纯销指金额（万元）</div>
      </div>
      <div class="input_box_content">
        <a-input placeholder="请输入" class="a_inpit" />
        <a-input placeholder="请输入" class="a_inpit" />
        <a-input placeholder="请输入" class="a_inpit" />
        <a-input placeholder="请输入" class="a_inpit" />
        <a-input placeholder="请输入" class="a_inpit" />
        <a-input placeholder="请输入" class="a_inpit" />
        <a-input placeholder="请输入" class="a_inpit" />
      </div>
      <div class="input_box_header1">
        <div style="flex: 1; padding: 10px">分销奖励</div>
        <div style="flex: 1; padding: 10px">费用科目</div>
        <div style="flex: 1; padding: 10px">零配送</div>
        <div style="flex: 1; padding: 10px">费用科目</div>
        <div style="flex: 1; padding: 10px">医疗配送商</div>
        <div style="flex: 1; padding: 10px">费用科目</div>
        <div style="flex: 1; padding: 10px">自定义7</div>
        <div style="flex: 1; padding: 10px">自定义8</div>
      </div>
      <div class="input_box_content1">
        <a-input placeholder="请输入" class="a_inpit" />

        <a-select value="指定渠道" class="a_inpit">
          <a-select-option value="指定渠道">指定渠道</a-select-option>
          <a-select-option value="指定渠道">指定渠道</a-select-option>
        </a-select>

        <a-input placeholder="请输入" class="a_inpit" />
        <a-select value="指定渠道" class="a_inpit">
          <a-select-option value="指定渠道">指定渠道</a-select-option>
          <a-select-option value="指定渠道">指定渠道</a-select-option>
        </a-select>
        <a-input placeholder="请输入" class="a_inpit" />
        <a-select value="指定渠道" class="a_inpit">
          <a-select-option value="指定渠道">指定渠道</a-select-option>
          <a-select-option value="指定渠道">指定渠道</a-select-option>
        </a-select>
        <a-input placeholder="请输入" value="2020-05-15" class="a_inpit" />
        <a-input placeholder="请输入" value="2020-05-15" class="a_inpit" />
      </div>
    </div>
  </div>
</template>
<script setup></script>
<style scoped>
.two_btn {
  margin-left: 10px;
}
.two_content {
  margin-top: 10px;
  display: flex;
  align-items: center;
  border-bottom: 10px;
}
.two_font {
  margin-left: 40px;
  font-size: 16px;
}
.two_font1 {
  font-size: 18px;
  font-weight: bold;
}
.two_box {
  border-radius: 10px;
  /* padding: 24px 0; */
  background: #fff;

  margin: 20px 10px 0 20px;
  /* height: 200px; */
}
.two_header {
  width: 100%;
  height: 60px;
  display: flex;
  align-items: center;
  border-bottom: 2px solid #ccc;
}
.two_header_th {
  align-items: center;
  width: 500px;
  display: flex;
}
.num {
  margin-left: 30px;
  color: blue;
}
.delect {
  margin-left: 710px;
  color: rgb(253, 148, 1);
}

.input_box_header {
  background: rgb(248, 248, 248);
  width: 95%;
  margin: 10px auto 0 auto;
  /* margin-top: 10px; */
  display: flex;
  border: 2px solid rgb(221, 221, 221);
}
.input_box_content {
  height: 50px;
  width: 95%;
  margin: 0px auto 0 auto;
  /* margin-top: 10px; */
  display: flex;
  align-items: center;
  border: 2px solid rgb(221, 221, 221);
  border-top: none;
}
.a_inpit {
  margin: 0 10px;
  height: 30px;
  flex: 1;
  background: rgb(248, 248, 248);
}
.input_box_header1 {
  background: rgb(248, 248, 248);
  width: 95%;
  margin: 10px auto 0 auto;
  /* margin-top: 10px; */
  display: flex;
}
.input_box_content1 {
  height: 50px;
  width: 95%;
  margin: 0px auto 0 auto;
  /* margin-top: 10px; */
  display: flex;
  align-items: center;
}
</style>
