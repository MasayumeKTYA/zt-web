<template>
  <a-layout>
    <a-layout-sider
      class="sider"
      breakpoint="lg"
      collapsed-width="0"
      @collapse="onCollapse"
      @breakpoint="onBreakpoint"
    >
      <div class="logo" />
      <a-menu v-model:selectedKeys="selectedKeys" theme="dark" mode="inline">
        <a-menu-item key="1">
          <user-outlined />
          <span class="nav-text">功能A</span>
          <RightOutlined class="right" />
        </a-menu-item>
        <a-menu-item key="2">
          <video-camera-outlined />
          <span class="nav-text">功能B</span>
          <RightOutlined class="right" />
        </a-menu-item>
        <a-menu-item key="3">
          <upload-outlined />
          <span class="nav-text">功能C</span>
          <RightOutlined class="right" />
        </a-menu-item>
        <a-menu-item key="4">
          <user-outlined />
          <span class="nav-text">功能D</span>
          <RightOutlined class="right" />
        </a-menu-item>
        <a-menu-item key="5">
          <user-outlined />
          <span class="nav-text">功能E</span>
          <RightOutlined class="right" />
        </a-menu-item>
        <a-menu-item key="6">
          <user-outlined />
          <span class="nav-text">功能F</span>
          <RightOutlined class="right" />
        </a-menu-item>
      </a-menu>
    </a-layout-sider>
    <a-layout class="main">
      <a-layout-header class="main_header">
        <div class="header_box">
          <HomeFilled class="icon_font icon" />
          <span class="bgfff">首页</span>
        </div>
        <div class="header_box">
          <HddFilled class="icon_font icon" />

          <span class="bgfff">主数据</span>
        </div>
        <div class="header_box">
          <GiftFilled class="icon_font icon" />
          <span class="bgfff">辖区管理</span>
        </div>
        <div class="header_box">
          <MacCommandFilled class="icon_font icon" />
          <span class="bgfff">销讯通</span>
        </div>
      </a-layout-header>
      <a-layout-content class="layout-content">
        <div class="breadcrub">
          <a-breadcrumb>
            <a-breadcrumb-item>首页</a-breadcrumb-item>
            <a-breadcrumb-item>年度协议管理</a-breadcrumb-item>
            <a-breadcrumb-item>二级商协议</a-breadcrumb-item>
            <a-breadcrumb-item>新增二级商协议</a-breadcrumb-item>
          </a-breadcrumb>
          <div class="currentBreadcrumb">新增二级商协议</div>
        </div>

        <div class="dash_box">
          <div class="dash"></div>
          <div style="margin-right: 10px">
            <span class="dash_bir">1</span>
            <span class="dash_font">协议主体</span>
          </div>
          <div class="dash"></div>
        </div>

        <div
          class="content"
          :style="{ padding: '24px', background: '#fff', minHeight: '360px' }"
        >
          <div class="content_input">
            <div class="content_inp">
              <span style="color: red" class="small">*</span>
              <span>协议客户：</span>
              <a-input value="选择客户" class="antd_input" />
              <span class="content_font">上海正也医药有限公司</span>
            </div>
            <div class="content_inp">
              <span>协议状态：</span>
              <!-- <a-input value="正常" class="antd_input" /> -->
              <a-input-group compact class="antd_select">
                <a-select value="正常" class="antd_select">
                  <a-select-option value="正常">正常</a-select-option>
                  <a-select-option value="不正常">不正常</a-select-option>
                </a-select>
              </a-input-group>
            </div>
          </div>
          <div class="content_input">
            <div class="content_inp">
              <span class="small"></span>
              <span>购进指标：</span>
              <a-input-group compact style="width: 100px">
                <a-select value="金额" style="width: 100px">
                  <a-select-option value="正常">正常</a-select-option>
                  <a-select-option value="不正常">不正常</a-select-option>
                </a-select>
              </a-input-group>
              <a-input
                value="输入金额/数量"
                style="width: 300px"
                class="two_ant_inp"
              />
            </div>
            <div class="content_inp">
              <span>纯销指标：</span>
              <a-input-group compact style="width: 100px">
                <a-select value="金额" style="width: 100px">
                  <a-select-option value="正常">正常</a-select-option>
                  <a-select-option value="不正常">不正常</a-select-option>
                </a-select>
              </a-input-group>
              <a-input
                value="输入金额/数量"
                style="width: 300px"
                class="two_ant_inp"
              />
            </div>
          </div>
          <div class="content_input">
            <div class="content_inp">
              <span class="small"></span>
              <span>销售区域：</span>

              <a-input value="选择区域" style="width: 100px" />
              <a-button type="primary" ghost class="btn"
                >全国 <CloseOutlined
              /></a-button>
            </div>
            <div class="content_inp">
              <span>签订时间：</span>
              <a-input value="2024-02-28 19：39" style="width: 410px" />
            </div>
          </div>
          <div class="content_input">
            <div class="content_inp">
              <span class="small"></span>
              <span>购进渠道：</span>
              <a-input-group compact style="width: 100px">
                <a-select value="指定渠道" style="width: 100px">
                  <a-select-option value="指定渠道">指定渠道</a-select-option>
                  <a-select-option value="指定渠道">指定渠道</a-select-option>
                </a-select>
              </a-input-group>
              <a-input
                value="选择渠道"
                style="width: 100px; margin-left: 10px"
              />
            </div>
          </div>
          <a-table
            size="small"
            :pagination="false"
            class="antd_table"
            :columns="columns"
            :data-source="data"
          />
        </div>

        <div class="dash_box">
          <div class="dash"></div>
          <div style="margin-right: 10px">
            <span class="dash_bir">2</span>
            <span class="dash_font">产品政策</span>
          </div>
          <div class="dash"></div>
        </div>
        <Two />
        <div class="dash_box">
          <div class="dash"></div>
          <div style="margin-right: 10px">
            <span class="dash_bir">3</span>
            <span class="dash_font">补充协议</span>
          </div>
          <div class="dash"></div>
        </div>
        <Three />
      </a-layout-content>
      <!-- <a-layout-footer style="text-align: center">
        Ant Design ©2018 Created by Ant UED
      </a-layout-footer> -->
    </a-layout>
  </a-layout>
</template>
<script setup>
import { ref } from "vue";
import Two from "../conponent/two.vue";
import Three from "../conponent/three.vue";
import {
  UserOutlined,
  VideoCameraOutlined,
  UploadOutlined,
  RightOutlined,
  HomeFilled,
  HddFilled,
  GiftFilled,
  MacCommandFilled,
  CloseOutlined,
} from "@ant-design/icons-vue";
const onCollapse = (collapsed, type) => {
  console.log(collapsed, type);
};

const onBreakpoint = (broken) => {
  console.log(broken);
};

const selectedKeys = ref(["1"]);
//表格
const columns = [
  {
    title: "指定渠道编码",
    dataIndex: "name",
  },

  {
    title: "指定渠道名称公司",
    dataIndex: "enterprise",
    sorter: {
      compare: (a, b) => a.math - b.math,
      multiple: 2,
    },
  },
  {
    title: "所在省",
    dataIndex: "prodvice",
    sorter: {
      compare: (a, b) => a.english - b.english,
      multiple: 1,
    },
  },
];

const data = [
  {
    key: "1",
    name: "BJ000090",

    enterprise: "宁波九州通药业有限公司",
    prodvice: "浙江省",
  },
  {
    key: "2",
    name: "BJ000092",

    enterprise: "国药控股精华有限公司",
    prodvice: "浙江省",
  },
  {
    key: "3",
    name: "BJ000094",

    enterprise: "老百姓药业有限公司",
    prodvice: "浙江省",
  },
];

function onChange(pagination, filters, sorter, extra) {
  console.log("params", pagination, filters, sorter, extra);
}
</script>
<style scoped>
.layout-content {
  overflow: auto;
}
.logo {
  height: 32px;
  background: rgba(255, 255, 255, 0.2);
  margin: 16px;
}

.right {
  margin-left: 70px;
}

.sider {
  height: 100vh;
}

.main {
  height: 100vh;
}

.header_box {
  margin-left: 40px;
  display: flex;
  align-items: center;
}

.main_header {
  background: #001529;
  padding: 0;
  display: flex;
  height: 74px;
}

.icon {
  padding: 10px;
  border-radius: 10px;
  background: rgb(81, 86, 92);
  font-size: 30px;
  color: rgb(187, 187, 187);
}

.bgfff {
  margin-left: 10px;
  color: rgb(187, 187, 187);
}

.breadcrub {
  padding: 20px;
  background: #fff;
}

.dash_box {
  margin-top: 20px;
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.dash {
  flex: 1;
  /* border: 1px dashed red; */
  border: 1px dashed #ccc;
}

.dash_bir {
  margin-left: 10px;
  margin-right: 10px;
  width: 15px;
  text-align: center;
  display: inline-block;
  background: rgb(78, 140, 254);
  border-radius: 50%;
  color: #fff;
  font-weight: bold;
  font-size: 14px;
}

.dash_font {
  font-weight: bold;
}

.currentBreadcrumb {
  margin-top: 10px;
  font-size: 20px;
}

.content {
  /* margin-top: 20px; */
  margin: 20px 10px 0 20px;
  padding: 20px;
}

.content_input {
  width: 100%;
  display: flex;
  align-items: center;
  margin-top: 10px;
}

.antd_input {
  width: 100px;
}

.antd_select {
  width: 200px;
}

.two_ant_inp {
  margin-left: 10px;
  background: rgb(248, 248, 248);
  color: #ccc;
}

.content_inp {
  display: flex;
  width: 50%;
  align-items: center;
}

.content_font {
  color: rgb(131, 131, 131);
  margin-left: 10px;
}

.small {
  display: inline-block;
  width: 10px;
}
.btn {
  margin-left: 10px;
  background: rgb(242, 248, 248);
}
.antd_table {
  width: 70%;
  margin: 30px auto 0 auto;
}

.site-layout-sub-header-background {
  background: #fff;
}

.site-layout-background {
  background: #fff;
}

[data-theme="dark"] .site-layout-sub-header-background {
  background: #141414;
}
</style>
