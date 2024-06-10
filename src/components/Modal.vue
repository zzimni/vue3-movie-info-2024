<template>
  <div class="modal" v-if="isModal">
    <div class="inner">
      <h3>{{ data[selectedMovie].title }}</h3>
      <p>영화 상세정보</p>
      <button @click="$emit('closeModal')">닫기</button>
      <!-- props로 전달받은 데이터는 부모만 변경 가능 -->
      <!-- 부모 컴포넌트에게 데이터 변경 요청하기 : $emit('이벤트명') -->
    </div>
  </div>
</template>

<script>
export default {
  name: "ModalComponent",
  props: {
    data: Array,
    isModal: Boolean,
    selectedMovie: Number,
  },
};
</script>

<style></style>
