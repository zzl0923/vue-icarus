<template>
  <button @click="handleSearchButtonClick">
    <Icon icon="search"></Icon>
  </button>
  <n-modal
    class="header-search-modal"
    v-model:show="showModal"
    preset="card"
    size="huge"
    :bordered="false"
  >
    <template #header>
      <n-input placeholder="搜索">
        <template #prefix>
          <Icon icon="Search"></Icon>
        </template>
      </n-input>
    </template>
  </n-modal>
</template>

<script lang="ts">
import { defineComponent, ref } from "vue";
import { Icon } from "~/components/Icon";
import { NModal, NInput } from "naive-ui";

export default defineComponent({
  components: {
    Icon,
    NModal,
    NInput,
  },
  setup() {
    const showModal = ref(false);
    const handleSearchButtonClick = () => {
      showModal.value = !showModal.value;
    };
    return {
      showModal,
      handleSearchButtonClick,
    };
  },
});
</script>