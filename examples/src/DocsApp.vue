<template>
  <div class="app">
    <page-header></page-header>
    <div class="main-content">
      <p class="page-tip">查看 demo 请将浏览器切换到手机调试模式</p>
      <div class="page-container clearfix">
        <side-nav :data="navConfig['zh-CN']" base="/component"></side-nav>
        <div class="page-content">
          <router-view></router-view>
          <footer-nav></footer-nav>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import Vue from 'vue';
import 'highlight.js/styles/atom-one-dark.css';
import navConfig from './nav.config.json';
import SideNav from './components/side-nav';
import DemoBlock from './components/demo-block';
import FooterNav from './components/footer-nav';
import PageHeader from './components/page-header';

Vue.component('side-nav', SideNav);
Vue.component('demo-block', DemoBlock);
Vue.component('footer-nav', FooterNav);
Vue.component('page-header', PageHeader);

export default {
  data() {
    return {
      navConfig: navConfig
    };
  }
};
</script>
