<template>
  <div class="youtube-container">
    <div class="youtube-wrap">
      <iframe class="youtube-player" type="text/html" width="640" height="360" :src="combineLink" frameborder="0"></iframe>
      <div class="title-wrap">
        <p class="title">{{cuttentVideo.name}}</p>
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

    <VideoList @clicked="handleChangeVideo" v-bind:videoArray="videoArray"/>
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
  },
  data() {
    return {
      cuttentVideo: {
        id: '',
        name: ''
      },
      videoArray: [
        {
          id: 'wfO6fyIk0NM',
          name: '南西肯恩 - 塵緣｜例假日',
          coverImage: 'https://i.ytimg.com/vi/wfO6fyIk0NM/hqdefault.jpg?sqp=-oaymwEZCNACELwBSFXyq4qpAwsIARUAAIhCGAFwAQ==&rs=AOn4CLBaIz7qwe6mk9Mz_DuSsacKI27qYw'
        },
        {
          id: '7jYDYon4sGQ',
          name: '伍佰 Wu Bai&China Blue【Last dance】Official Music Video(HD)',
          coverImage: 'https://i.ytimg.com/vi/7jYDYon4sGQ/hqdefault.jpg?sqp=-oaymwEZCNACELwBSFXyq4qpAwsIARUAAIhCGAFwAQ==&rs=AOn4CLAowjVnedL8eRB_aLqmslzkaV3WUw'
        },
        {
          id: '_dW66owaCJs',
          name: '伍佰 & China Blue《讓水倒流》 Official Music Video',
          coverImage: 'https://i.ytimg.com/vi/_dW66owaCJs/hqdefault.jpg?sqp=-oaymwEZCNACELwBSFXyq4qpAwsIARUAAIhCGAFwAQ==&rs=AOn4CLA7f7yLF2HaNq8Niv9-LfiJEscAqg'
        },
        {
          id: '_dqLb1xG26Y',
          name: '【純享版】吳青峰/路嘉欣翻唱許美靜《蔓延》多年摯友呈現完美和聲《天賜的聲音》純享版No Noice /浙江衛視官方HD/',
          coverImage: 'https://i.ytimg.com/vi/_dqLb1xG26Y/hqdefault.jpg?sqp=-oaymwEZCNACELwBSFXyq4qpAwsIARUAAIhCGAFwAQ==&rs=AOn4CLC70dPPxoByedpx1KsP9k0RPOxfjw'
        }
      ] 
    }
  },
  computed: {
    combineLink() {
      return 'http://www.youtube.com/embed/' + this.cuttentVideo.id;
    }
  },
  methods: {
    handleChangeVideo(index) {
      this.cuttentVideo.id = this.videoArray[index].id;
      this.cuttentVideo.name = this.videoArray[index].name;
    }
  },
  mounted: function() {
    this.cuttentVideo.id = this.videoArray[0].id;
    this.cuttentVideo.name = this.videoArray[0].name;
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
