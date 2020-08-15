<template>
  <div class="youtube-container">
    <div class="youtube-wrap">
      <iframe class="youtube-player" type="text/html" width="640" height="360" src="http://www.youtube.com/embed/y3BE3QVLDVA" frameborder="0"></iframe>
      <div class="title-wrap">
        <p class="title">辛普森卡通2020年預言！辛普森家庭預言了2020年川普下台，美國破產？辛普森家庭曾預言中了三眼魚，馬肉風波，智能手機，美國監聽人民</p>
      </div>

      <div class="author-wrap">
        <p class="name">阿斗归来了</p>
        <p class="text">我是阿斗，他们说我有一种让人沉迷在电影故事中的魔力，你觉得呢？微信公众号：阿斗归来了</p>
      </div>

      <input type="text" placeholder="新增公開留言">
      <div>
        <span>取消</span>
        <span>留言</span>
      </div>

      <MessageBoard/>
    </div>

    <VideoList/>
  </div>
</template>

<script>
import MessageBoard from '../components/MessageBoard';
import VideoList from '../components/VideoList';
export default {
  name: 'Youtube',
  components: {
    MessageBoard,
    VideoList,
  }
}
</script>

<style scoped>
.youtube-container {
  display: flex;
}
.youtube-wrap {
  padding: 24px;
  width: 1014px;
  box-sizing: border-box;
  text-align: left;
}
.youtube-player {
  width: 966px;
  height: 543px;
}
.youtube-wrap .title-wrap {
  border-bottom: solid 1px #000;
  padding: 20px 0 8px;
}

.youtube-wrap .author-wrap {
  border-bottom: solid 1px #000;
  padding: 16px 0;
}
</style>
