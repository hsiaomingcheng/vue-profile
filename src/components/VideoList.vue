<template>
  <div class="video-wrap">
    <div class="video-content" v-for="video in videoArray" :key="video.id">
      <img class="cover-image" :src="video.coverImage" alt="">
      <p class="name" :title="video.name">{{video.name}}</p>
    </div>
  </div>
</template>

<script>
export default {
  name: 'VideoList',
  data () {
    return {
      videoArray: [
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
  }
}
</script>

<style scoped>
.video-wrap {
  padding: 24px 24px 0 0;
}
.video-wrap .video-content {
  margin-bottom: 8px;
  display: flex;
  text-align: left;
}
.video-wrap .cover-image {
  margin-right: 8px;
  width: 168px;
  height: 94px;
}
.video-wrap .name {
  display: -webkit-box;
  height: 44px;
  overflow: hidden;
  text-overflow: ellipsis;
  -webkit-line-clamp: 2;
  -webkit-box-orient: vertical;
}
</style>
