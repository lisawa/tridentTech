﻿<template>
  <div class="exam">
    <div class="side">
      <h2>
        <div class="burger" :class="{'close': showbar}" v-on:click="clickShow()"><div></div></div>
        白頭翁不吃小米
      </h2>
      <div class="sub select" :class="{'show': showbar}">白頭翁的特性</div>
      <div class="sub" :class="{'show': showbar}">白頭翁的故事</div>
      <div class="sub" :class="{'show': showbar}">白頭翁的美照</div>
      <div class="sub" :class="{'show': showbar}">白頭翁的危機</div>
      <div class="logoPos">
        <div class="logo">
          <div></div>
        </div>
      </div>
    </div>
    <div class="content">
      <div class="imgblock">
        <img src="/banner.png" />
        <div class="imgContent">
          <div class="name">{{name}}</div>
          <div class="desc">{{desc}}</div>
        </div>
      </div>
      <div class="subTitle">
        <template v-for="d in textDesc" :key="d.title">
          <SubDesc :data="d" />
        </template>
      </div>
    </div>
  </div>
</template>

<style scoped lang="scss">
@import "./ExamPage.css";
</style>

<script setup>
import SubDesc from './SubDesc.vue';
import { ref } from 'vue';
const name = '白頭翁 (Chinese bulbul)';
const desc = '又名白頭鵯。以果實、昆蟲為主食，無法消化小米、穀類。平均壽命約 8~10 年。';
const textDesc = [{
  title: '外觀',
  desc: '白頭鵯體長約17到22公分，額至頭頂純黑色而富有光澤，兩眼上方至後枕白色，形成一白色枕環。耳羽後部有一白斑，此白環與白斑在黑色的頭部均極為醒目，老鳥的枕羽(後頭部)更潔白，所以又叫「白頭翁」。',
},{
  title: '棲地',
  desc: '白頭翁和麻雀、綠繡眼合稱「城市三寶」，常成群出現在平原區灌木叢、丘陵樹林地帶，以及校園、公園、庭院、行道中的各種高高的電線與樹上。',
},{
  title: '食性',
  desc: '以果樹的漿果和種子為主食，並時常飛入果園偷吃果實，還會吃嫩葉嫩芽，尤其是胡蝶蘭的嫩葉嫩芽葉，偶爾啄食昆蟲。',
}];
let showbar = ref(false);
function clickShow () {
  showbar.value = !showbar.value;
}
</script>