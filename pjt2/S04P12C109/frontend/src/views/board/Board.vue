<template>
  <div id="board">
    <b-container class="board">
      <b-row>
        <b-col sm="3" class="board-aside">
          <BoardDescription/>
          <button
            class="btn-subscribe b-title"
            @click="onSubscribe"
          >Subscribe</button>
          <hr>
          <div class="board-function">보드특수기능들</div>
          <div class="add-board-function">보드기능 추가</div>
        </b-col>
        <b-col sm="9" class="board-section">
          <div class="post-search">
            <div>찾기</div>
          </div>
          <div class="post-write">
            <!-- <b-button variant="light">글쓰기</b-button> -->
            <PostWrite/>
          </div>
          <PostList/>
        </b-col>
      </b-row>
    </b-container>
  </div>
</template>

<script>
import BoardDescription from '@/components/board/BoardDescription.vue'

import PostWrite from '@/components/board/PostWrite.vue'
import PostList from '@/components/board/PostList.vue'

export default {
  name:'Board',
  components: {
    BoardDescription,
    PostList,
    PostWrite,
  },
  methods:{
    onSubscribe(){
      return
    }
  }
}
</script>

<style scoped>

.board{
  max-width: 1200px !important;
  margin: 0 auto;
  margin-top:30px;
  /* width:80%;
  margin-left:10%;
  margin-right:10%; */
}

/* .post-write {
  display: inline-block;
  position:sticky;
} */
.post-search{
  display: flex;
  justify-content: flex-end;
}
.btn-subscribe{
  /* position: inherit;  */
  height: 50px;
  width:100%;
  font-size: 24px;
  margin-top: 10px; 
  margin-bottom: 10px;
  text-align: center;
}
.btn-subscribe:hover,
.btn-subscribe:active {
  background-color: #000 !important;
  color: #fff;
}

@media screen and (max-width:576px){
  .btn-subscribe{
    width: 100%;
    background-color: #000 !important;
    color: #fff;
  }
  .post-search{
    display:none;
  }
  .add-board-function{
    display: none;
  }
}
</style>