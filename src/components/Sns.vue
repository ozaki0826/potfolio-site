<template>
  <ul class="sns">
    <li class="sns-item"><a href="#" target="_blank"><Twitter />Twitter</a></li>
    <li class="sns-item"><a href="https://github.com/ozaki0826" target="_blank"><Github />Github</a></li>
    <li class="sns-item"><a href="https://www.instagram.com/ozaki_0826/" target="_blank"><Instagram />Instagram</a></li>
  </ul>
</template>

<script>
import Twitter from '@/icon/Twitter.vue'
import Github from '@/icon/Github.vue'
import Instagram from '@/icon/Instagram.vue'

export default {
  components: {
    Twitter,
    Github,
    Instagram
  },
}
</script>

<style lang="scss" scoped>
.sns {
  padding: 64px 0;
  background-color: #39C;
  color: #fff;
  position: relative;
  overflow: hidden;
  text-align: center;
  &:after {
    margin: 0 auto;
    position: absolute;
    display: block;
    content: '';
    width: 2000px;
    height: 2000px;
    background-color: rgba(0, 0, 0, 0.1);
    transform: rotate(15deg);
    top: -1000px;
    left: -2300px;
    right: 0;
  }
}

.sns-item {
  display: inline-block;
  margin: 16px 24px;
  font-size: 18px;
  & svg {
    vertical-align: middle;
    margin-right: 8px;
  }
  & a {
    color: #fff;
    text-decoration: none;
    &:hover {
      opacity: 0.8;
    }
  }
  @media screen and (max-width:600px) {
    display: block;
  }
}
</style>