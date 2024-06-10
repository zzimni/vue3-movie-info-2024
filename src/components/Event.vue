<template>
  <div class="event">
    <p>{{ text }}</p>
  </div>
</template>

<script>
export default {
  name: "EventComponent",
  // 데이터를 받는 자식 컴포넌트에서 정의해줘야하는 부분
  props: {
    text: String, // (props)변수명: 자료형
  },
};
</script>

<style>
.event {
  background: #444;
  color: #fff;
  padding: 10px 20px;
  text-align: center;
  font-size: small;
}
.event p {
  margin: 0;
}
</style>
