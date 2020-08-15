<template>
  <div class="message-wrap">
    <div v-for="msg in msgArray" :key="msg.accountId">
      <p class="name">{{msg.name}}</p>
      <p class="text">{{msg.text}}</p>
    </div>
  </div>
</template>

<script>
export default {
  name: 'MessageBoard',
  data () {
    return {
      msgArray: [
        {
          accountId: '01',
          name: '王小明',
          text: '我的天，真的太好聽了'
        },
        {
          accountId: '02',
          name: '辛普森',
          text: '我的天，真的太美了'
        },
        {
          accountId: '03',
          name: '川普',
          text: '我要請你駐唱'
        }
      ]
    }
  }
}
</script>

<style scoped>
</style>
