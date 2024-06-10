<template>
  <h1>영화정보</h1>
  <div v-for="(movie, i) in data" :key="i">
    <!-- v-for ="(item,index) in 데이터"-->
    <!-- :key="키값"-->
    <h3 class="bg-yellow" :style="textRed">{{ movie.title }}</h3>
    <!-- :속성명 = "데이터" -->
    <p>개봉: {{ movie.year }}</p>
    <p>장르: {{ movie.category }}</p>
  </div>
</template>

<script>
export default {
  name: "App", // 컴포넌트 명 여기에 적기
  data() {
    // 문서에 표시될 변수들 정의 - 상태 변수 (자주 변경되는 값)을 여기에 정의
    return {
      textRed: "color: red",
      data: [
        {
          title: "노량",
          year: 2023,
          category: "액션, 드라마",
        },
        {
          title: "아쿠아맨과 로스트 킹덤",
          year: 2023,
          category: "액션, 판타지, 어드벤처",
        },
        {
          title: "3일의 휴가",
          year: 2023,
          category: "판타지, 드라마",
        },
      ],
    };
  },
};
</script>

<style>
.bg-yellow {
  background: gold;
  padding: 10px;
}
</style>
