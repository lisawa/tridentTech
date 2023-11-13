<template>
  <div class="subDesc">
    <div class="title">{{props.data.title}}</div>
    <div class="desc">{{props.data.desc}}</div>
  </div>
</template>

<style>
.subDesc {
  flex: 0 0 calc(33% - 100px);
  display: flex;
  gap: 40px;
  padding: 50px;
}

.title {
  position: relative;
  font-family: Noto Sans;
  font-size: 36px;
  font-weight: 700;
  line-height: 40px;
  letter-spacing: 0em;
  text-align: left;
  gap: 20px;
}

.title::before {
  position: absolute;
  content: "";
  border: 8px solid #AA666699;
  width: 9px;
  height: 9px;
  border-radius: 50%;
  right: -15px;
  top: 65px;
}

.desc {
  font-family: Noto Sans;
  font-size: 16px;
  font-weight: 400;
  line-height: 22px;
  letter-spacing: 0em;
  text-align: left;
}

</style>

<script setup>
import { defineProps } from 'vue';

const props = defineProps({
  data: {
    title: String,
    desc: String
  }
});

</script>
