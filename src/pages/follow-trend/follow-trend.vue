<template>
  <div class="container">
    <ul class="trend-container">
      <li class="trend-item">
        <a class="user-avatar">
          <!-- https://cube.elemecdn.com/3/7c/3ea6beec64369c2642b92c6726f1epng.png -->
          <img class="avatar-item" src="https://img2.imgtp.com/2024/05/04/DdkME2jI.jpg" />
        </a>
        <div class="main">
          <div class="info">
            <div class="user-info">
              <a class>可乐</a>
            </div>
            <div class="interaction-hint"><span>1天前</span></div>
            <div class="interaction-content">具体内容</div>
            <div class="interaction-imgs">
                <ul role="list" class="grid grid-cols-2 gap-x-4 gap-y-8 sm:grid-cols-3 sm:gap-x-6 lg:grid-cols-4 xl:gap-x-8">
                    <li v-for="file in files" :key="file.source" class="relative">
                        <div class="group aspect-h-7 aspect-w-10 block w-full overflow-hidden rounded-lg bg-gray-100 focus-within:ring-2 focus-within:ring-indigo-500 focus-within:ring-offset-2 focus-within:ring-offset-gray-100">
                            <img :src="file.source" alt="" class="pointer-events-none object-cover group-hover:opacity-75" />
              
                        </div>
                       
                    </li>
                </ul>
            </div>

            <div class="interaction-footer">
              <div class="icon-item"><Star style="width: 1em; height: 1em" /><span class="count">12</span></div>
              <div class="icon-item"><ChatRound style="width: 1em; height: 1em" /><span class="count">51</span></div>
              <div class="icon-item"><More style="width: 1em; height: 1em" /></div>
            </div>
          </div>
        </div>
      </li>
      <li class="trend-item">
        <a class="user-avatar">
          <!-- https://cube.elemecdn.com/3/7c/3ea6beec64369c2642b92c6726f1epng.png -->
          <img class="avatar-item" src="https://img2.imgtp.com/2024/05/04/DdkME2jI.jpg" />
        </a>
        <div class="main">
          <div class="info">
            <div class="user-info">
              <a class>可悲</a>
            </div>
            <div class="interaction-hint"><span>2天前</span></div>
            <div class="interaction-content">具体内容</div>
              <div class="interaction-imgs">
                  <ul role="list" class="grid grid-cols-2 gap-x-4 gap-y-8 sm:grid-cols-3 sm:gap-x-6 lg:grid-cols-4 xl:gap-x-8">
                      <li v-for="file in files" :key="file.source" class="relative">
                          <div class="group aspect-h-7 aspect-w-10 block w-full overflow-hidden rounded-lg bg-gray-100 focus-within:ring-2 focus-within:ring-indigo-500 focus-within:ring-offset-2 focus-within:ring-offset-gray-100">
                              <img :src="file.source" alt="" class="pointer-events-none object-cover group-hover:opacity-75" />
                           
                          </div>
                      </li>
                  </ul>
              </div>
            <div class="interaction-footer">
              <div class="icon-item"><Star style="width: 1em; height: 1em" /><span class="count">25</span></div>
              <div class="icon-item"><ChatRound style="width: 1em; height: 1em" /><span class="count">83</span></div>
              <div class="icon-item"><More style="width: 1em; height: 1em" /></div>
            </div>
          </div>
        </div>
      </li>
    </ul>
  </div>
</template>
<script lang="ts" setup>
import { Star, ChatRound, More } from "@element-plus/icons-vue";
const files = [
    {
        source:'https://img2.imgtp.com/2024/05/04/pHawEm7c.jpg',
    },
    {
        source:'https://img2.imgtp.com/2024/05/04/GCdcnmrW.jpg',
    },
    {
        source:'https://img2.imgtp.com/2024/05/04/UrqunCaV.jpg',
    },
    {
        source:'https://img2.imgtp.com/2024/05/04/Ebbe4lQa.jpg',
    },

]
</script>

<style scoped>

.container {
  flex: 1;
  padding-top: 72px;
  width: calc(90vw - 24px);
  max-width: 840px;
  margin: 0 auto;
}
.trend-container{
    width: 100%;
    justify-items: center;
    align-items: center;
    display: flex;
    flex-direction: column;
}
.container .trend-container .trend-item {
  display: flex;
  flex-direction: row;
  padding-top: 24px;
    max-width: 840px;
}
.container .trend-container .trend-item .user-avatar {
  margin-right: 24px;
  flex-shrink: 0;
}
.container .trend-container .trend-item .user-avatar .avatar-item {
  width: 48px;
  height: 48px;
  display: flex;
  align-items: center;
  justify-content: center;
  cursor: pointer;
  border-radius: 100%;
  border: 1px solid rgba(0, 0, 0, 0.08);
  object-fit: cover;
}
.container .trend-container .trend-item .main {
  flex-grow: 1;
  flex-shrink: 1;
  display: flex;
  flex-direction: row;
  padding-bottom: 12px;
  border-bottom: 1px solid rgba(0, 0, 0, 0.08);
}
.container .trend-container .trend-item .main .info {
  flex-grow: 1;
  flex-shrink: 1;
}
.container .trend-container .trend-item .main .info .user-info {
  display: flex;
  flex-direction: row;
  align-items: center;
  font-size: 16px;
  font-weight: 600;
  margin-bottom: 4px;
}
.container .trend-container .trend-item .main .info .user-info a {
  color: #333;
}
.container .trend-container .trend-item .main .info .interaction-hint {
  font-size: 14px;
  color: rgba(51, 51, 51, 0.6);
  margin-bottom: 8px;
}
.container .trend-container .trend-item .main .info .interaction-content {
  display: flex;
  font-size: 14px;
  color: #333;
  margin-bottom: 12px;
  line-height: 140%;
  cursor: pointer;
}
.container .trend-container .trend-item .main .info .interaction-imgs {
  display: flex;
}
.container .trend-container .trend-item .main .info .interaction-imgs .details-box {
  width: 25%;
  border-radius: 4px;
  margin: 8px 12px 0 0;
  cursor: pointer;
}
.container .trend-container .trend-item .main .info .interaction-imgs .details-box img {
  width: 100%;
  height: 230px;
  display: flex;
  border-radius: 4px;
  align-items: center;
  justify-content: center;
  cursor: pointer;
  border: 1px solid rgba(0, 0, 0, 0.08);
  object-fit: cover;
}
.container .trend-container .trend-item .main .info .interaction-footer {
  margin: 8px 12px 0 0;
  padding: 0 12px;
  display: flex;
  justify-content: space-between;
  align-items: center;
}
.container .trend-container .trend-item .main .info .interaction-footer .icon-item {
  display: flex;
  justify-content: left;
  align-items: center;
  color: rgba(51, 51, 51, 0.929);
}
.container .trend-container .trend-item .main .info .interaction-footer .icon-item .count {
  margin-left: 3px;
}

</style>
