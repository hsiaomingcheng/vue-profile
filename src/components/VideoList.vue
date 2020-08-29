<template>
  <div class="video-wrap">
    <div class="video-content" @click.prevent="handleGetVideoId(index)" v-for="(video, index) in videoArray" :key="video.id">
      <img class="cover-image" :src="video.coverImage" :alt="video.name">
      <p class="name" :title="video.name">{{video.name}}</p>
    </div>
  </div>
</template>

<script>
export default {
  name: 'VideoList',
  props: ['videoArray'],
  methods: {
    handleGetVideoId(index) {
      this.$emit('clicked', index);
    }
  },
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
  cursor: pointer;
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
