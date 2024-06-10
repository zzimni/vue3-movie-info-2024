<template>
  <h1>영화정보</h1>
  <div v-for="(movie, i) in data" :key="i">
    <!-- v-for ="(item,index) in 데이터"-->
    <!-- :key="키값"-->
    <h3 class="bg-yellow" :style="textRed">{{ movie.title }}</h3>
    <!-- :속성명 = "데이터" -->

    <!-- Vue.js에서 :style="..."와 같은 문법은 "바인딩 디렉티브" 중 하나입니다. 콜론 :은 v-bind 디렉티브의 축약형으로, JavaScript 표현식을 HTML 속성에 바인딩할 때 사용됩니다. 이 문법을 통해 Vue.js 컴포넌트에서 동적 스타일을 적용할 수 있습니다.
    - 바인딩 가능한 속성들
      v-bind 디렉티브(즉, :)를 사용하면 거의 모든 HTML 속성과 Vue.js 컴포넌트 속성에 JavaScript 표현식을 바인딩할 수 있습니다. 몇 가지 예시는 다음과 같습니다:

      HTML 속성:

      :href="dynamicUrl": 동적 URL을 href 속성에 바인딩합니다.
      :src="imageSrc": 동적 이미지 소스를 src 속성에 바인딩합니다.
      :alt="imageDescription": 동적 텍스트를 alt 속성에 바인딩합니다.
      
      Boolean 속성:

      :disabled="isDisabled": isDisabled가 true일 때 버튼을 비활성화합니다.
      :checked="isChecked": 체크박스를 동적으로 체크합니다.

      CSS 클래스:

      :class="{ active: isActive }": isActive가 true일 때 active 클래스를 추가합니다.
      :class="[class1, class2]": 배열 형태로 여러 클래스를 동적으로 추가합니다.

      -->

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
