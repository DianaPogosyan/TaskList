<template>
    <div class="main">
        <div class="main__head" style="background-color: black; width: 100%; height: 50px; position: absolute; z-index: 10;"><h2>Доски</h2></div>
        <el-row class="tac">
          <el-col :span="12">
            <el-menu 
              default-active="2"
              class="el-menu-vertical-demo main__bar"
              @open="handleOpen"
              @close="handleClose"
              background-color="#545c64"
              text-color="#fff"
              active-text-color="#ffd04b">
              <el-button type="success" icon="el-icon-plus">Добавить список</el-button>
              <el-submenu index="1">
                <template slot="title">
                  <span>Доска 1</span>
                </template>
                <el-menu-item-group title="Group One">
                  <el-menu-item index="1-1">item one</el-menu-item>
                  <el-menu-item index="1-2">item one</el-menu-item>
                </el-menu-item-group>
                <el-menu-item-group title="Group Two">
                  <el-menu-item index="1-3">item three</el-menu-item>
                </el-menu-item-group>
                <el-submenu index="1-4">
                  <template slot="title">item four</template>
                  <el-menu-item index="1-4-1">item one</el-menu-item>
                </el-submenu>
              </el-submenu>
              <el-submenu index="2">
                <template slot="title">
                  <span>Доска 2</span>
                </template>
                <el-menu-item-group title="Group One">
                  <el-menu-item index="1-1">item one</el-menu-item>
                  <el-menu-item index="1-2">item one</el-menu-item>
                </el-menu-item-group>
                <el-menu-item-group title="Group Two">
                  <el-menu-item index="1-3">item three</el-menu-item>
                </el-menu-item-group>
                <el-submenu index="1-4">
                  <template slot="title">item four</template>
                  <el-menu-item index="1-4-1">item one</el-menu-item>
                </el-submenu>
              </el-submenu>
              <el-submenu index="3">
                <template slot="title">
                  <span>Доска 3</span>
                </template>
                <el-menu-item-group title="Group One">
                  <el-menu-item index="1-1">item one</el-menu-item>
                  <el-menu-item index="1-2">item one</el-menu-item>
                </el-menu-item-group>
                <el-menu-item-group title="Group Two">
                  <el-menu-item index="1-3">item three</el-menu-item>
                </el-menu-item-group>
                <el-submenu index="1-4">
                  <template slot="title">item four</template>
                  <el-menu-item index="1-4-1">item one</el-menu-item>
                </el-submenu>
              </el-submenu>
              <el-submenu index="4">
                <template slot="title">
                  <span>Доска 4</span>
                </template>
                <el-menu-item-group title="Group One">
                  <el-menu-item index="1-1">item one</el-menu-item>
                  <el-menu-item index="1-2">item one</el-menu-item>
                </el-menu-item-group>
                <el-menu-item-group title="Group Two">
                  <el-menu-item index="1-3">item three</el-menu-item>
                </el-menu-item-group>
                <el-submenu index="1-4">
                  <template slot="title">item four</template>
                  <el-menu-item index="1-4-1">item one</el-menu-item>
                </el-submenu>
              </el-submenu>
            </el-menu>
          </el-col>
        </el-row>
       <el-row class="main__gallery">
            <el-card :body-style="{ padding: '0px' }">
              <img src="../img/card_4.jpg" class="image">
              <span>Планируемые покупки</span>  
            </el-card>
            <el-card :body-style="{ padding: '0px' }">
              <img src="../img/card_3.jpg" class="image">
              <span>Планы на вечер</span>  
            </el-card>
            <el-card :body-style="{ padding: '0px' }">
              <img src="../img/card_1.jpg" class="image">
              <span>Кино</span>  
            </el-card>
            <el-card :body-style="{ padding: '0px' }">
              <img src="../img/card_2.jpg" class="image">
              <span>Домашние обязанности</span>  
            </el-card>
        </el-row>
    </div>
</template>

<style>
  .el-menu-vertical-demo:not(.el-menu--collapse) {
    width: 200px;
    min-height: 400px;
  }
</style>

<script>

  export default {
    methods: {
      handleOpen(key, keyPath) {
        console.log(key, keyPath);
      },
      handleClose(key, keyPath) {
        console.log(key, keyPath);
      }
    }
  }

import Vue from 'vue';
import ElementUI from 'element-ui';
import 'element-ui/lib/theme-chalk/index.css';

Vue.use(ElementUI);

</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">

.main {
  display: flex;
  }
h2 {
  display: block;
  padding: 0;
  line-height: 50px;
  padding-left: 40px;
  color: white;
  background-color: black;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}

.main__bar {
  height: 100vh;
  padding: 70px 0 0;
}
.el-submenu__icon-arrow {
  content: none;
}

.main__gallery {
  width: 100%;
  display: flex;
  flex-direction: row;
  justify-content: flex-start;
  flex-wrap: wrap;
  padding: 70px 30px;
  position: relative;
}

.el-card{
    position: relative;
    height: 150px;
    margin: 0 3%;
}
.el-card span{
  position: absolute;
  top: 0;
  text-align: center;
  color: #fff;
  width: 100%;
  font-weight: 500;
  line-height: 50px;
  background: rgba(0,0,0,.4);
}
.el-col {
width: 200px;
margin: 0 0 40px;
}
a {
  color: #42b983;
}
.time {
  font-size: 13px;
  color: #999;
}
.bottom {
  margin-top: 13px;
  line-height: 12px;
}
.button {
  padding: 0;
  float: left;
}
.el-button {
  margin-left: 15px;
}
.image {
  width: 200px;
  height: 150px;
  display: block;
  
}

</style>
