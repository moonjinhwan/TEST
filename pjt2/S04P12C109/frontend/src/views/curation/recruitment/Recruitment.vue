<template>
  <div class="container-box">
    <!-- 왼쪽 메뉴 부분 -->
    <div class="left-info">
        <!-- Curation -->
        <div class="title">
          <h4>curation</h4>
        </div>
        <!-- 해당 큐레이션 description -->
        <div class="description">
          <h4>채용일정</h4>
          <p>
            채용일정 너만아니<br>
            채용일정 나도알자
          </p>
        </div>
        <!-- 임박한 채용보기 -->
        <div class="due-date">
          임박한 채용일정 보여줄 리스트
          <DueDateItem />
          <DueDateItem />
          <DueDateItem />
          <DueDateItem />
        </div>
    </div>
    <div class="center-post">
      <!-- 캘린더 들어가는 부분 -->
      <div class="study-calendar">
        캘린더가 들어갈 부분
      </div>
      <!-- 검색 돋보기 아이콘 -->
      <div class="search-bar">
      🔍검색창 들어갈 부분
      </div>
      <!-- 게시글 작성 -->
      <div class="create-post">
      <button>게시글 작성 버튼</button>
      </div>
      <!-- 각각의 게시글 들어갈 부분 -->
      <Post 
        class="post-list"
      />
    </div>
  </div>
</template>

<script>
// 스터디 홍보글 게시물
import Post from "@/components/board/Post.vue"
import DueDateItem from "@/views/curation/recruitment/DueDateItem.vue"

export default {
  name:'Recruitment',
  components: {
    Post,
    DueDateItem,
  },
}
</script>

<style scoped>
.container-box {
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  margin: auto;
  border: 2px solid #000000;
  height: 100vh;
  margin: 1% 7%;
}
/* 왼쪽 메뉴바 부분 */
.container-box .left-info {
  display: flex;
  flex-direction: column;
  background-color: bisque;
  flex-basis: 32%;
}
/* 스터디 보드 설명 */
.left-info .description {
  border: 2px dotted;
  padding-top: 2%;
  padding-left: 4%;
  flex-basis: 20%;
}
/* 스터디 리스트 */
.left-info .study-list {
  display: flex;
  flex-direction: column;
  border: 2px inset #000000;
  margin-top: 5%;
}
/* 스터디 리스트 헤더 */
.study-list .hd {
  display: flex;
  flex-direction: row;
  border: 1px dotted;
}


/* 가운데 게시글 부분 */
.container-box .center-post {
  display: flex;
  flex-direction: column;
  justify-content: flex-start;
  align-items: center;
  background-color: pink;
  flex-basis: 63%;
  border: 4px solid;
}

/* 스터디 캘린더 */
.center-post .study-calendar {
  background-color: azure;
  width: 100%;
  height: 70%;
}

/* 검색창 */
.center-post .search-bar {
  align-self: flex-end;
}

/* 각각의 게시글들 */
.center-post .post-list {
  border: 2px dotted;
  margin: 2% 2%;
}

/* 모바일 웹화면 */
@media (max-width: 425px) {
  .container-box {
    flex-direction: column;
  }
  /* z-index 화면전환 구현하기 */
}
</style>