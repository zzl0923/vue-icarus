<template>
  <div class="grid md:grid-cols-2 lg:grid-cols-3 md:gap-x-4 gap-y-4">
    <n-card class="site-card w-full md:w-96" v-for="value in list" :key="value">
      <template #cover>
        <img
            src="https://07akioni.oss-cn-beijing.aliyuncs.com/07akioni.jpeg"
            alt=""
            class="h-36"
        />
      </template>
      <template #header>
        <span>GoLang + Vue + Naive UI 开发个人博客</span>
      </template>
      <template #default>
        <div class="article-meta">
          <div class="article-meta-item">
            <n-avatar
                :style="{ border: '1px solid #f7f7f7' }"
                :round="true"
                :src="avatar"
                :size="22"
            >
            </n-avatar>
            <span>ZZL</span>
          </div>
          <n-divider vertical></n-divider>
          <div class="article-meta-item">
            <icon icon="FolderOpen"></icon>
            <span>分类</span>
          </div>
          <n-divider vertical></n-divider>
          <div class="article-meta-item">
            <icon icon="Tags"></icon>
            <span>标签</span>
          </div>
          <n-divider vertical></n-divider>
          <div class="article-meta-item">
            <icon icon="Tags"></icon>
            <span>标签</span>
          </div>
        </div>
        <n-divider class="article-divider"></n-divider>
        <div>这是简介这是简介这是简介这是简介这是简介</div>
      </template>
      <template #footer>
        <div class="article-date">
          <icon icon="CalendarAlt"/>
          <span>创建于两个月以前</span>
        </div>
        <div class="article-date">
          <icon icon="PencilAlt"/>
          <span>更新于两个月以前</span>
        </div>
      </template>
    </n-card>
  </div>
</template>

<script lang="ts">
import {defineComponent} from "vue";
import {NCard, NDivider, NAvatar, NGrid, NGridItem} from "naive-ui";
import {Icon} from "~/components/Icon";
import avatar from "~/assets/images/avatar.jpg";

export default defineComponent({
  components: {
    NCard,
    Icon,
    NDivider,
    NAvatar,
  },
  setup() {
    const list = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12];
    return {avatar, list};
  },
});
</script>
