<script setup lang="ts">
import { ref } from 'vue'

const props = defineProps({
  repo: {
    type: String,
    default: 'chonkie-inc/chonkie',
  },
  width: {
    type: String,
    default: '100%',
  },
  height: {
    type: String,
    default: 'auto',
  },
})

const loaded = ref(false)
const error = ref(false)

const imageUrl = `https://api.star-history.com/svg?repos=${props.repo}`

const handleLoad = () => {
  loaded.value = true
}

const handleError = () => {
  error.value = true
}
</script>

<template>
  <div class="star-history-container" :style="{ width, height }">
    <div v-if="!loaded && !error" class="loading-state">
      <div class="spinner" />
      <p class="text-sm opacity-75">Loading star history...</p>
    </div>

    <div v-if="error" class="error-state">
      <p class="text-sm opacity-75">Unable to load star history chart</p>
      <a
        :href="`https://github.com/${repo}`"
        target="_blank"
        class="text-blue-500 hover:underline"
      >
        View on GitHub
      </a>
    </div>

    <img
      v-show="loaded && !error"
      :src="imageUrl"
      alt="Star History Chart"
      class="star-history-image"
      @load="handleLoad"
      @error="handleError"
    />
  </div>
</template>

<style scoped>
.star-history-container {
  position: relative;
  min-height: 300px;
  display: flex;
  align-items: center;
  justify-content: center;
}

.loading-state, .error-state {
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 1rem;
}

.spinner {
  width: 40px;
  height: 40px;
  border: 3px solid rgba(75, 85, 99, 0.2);
  border-top-color: #2B90B6;
  border-radius: 50%;
  animation: spin 1s linear infinite;
}

@keyframes spin {
  to { transform: rotate(360deg); }
}

.star-history-image {
  width: 100%;
  height: auto;
  border-radius: 8px;
  box-shadow: 0 4px 6px -1px rgba(0, 0, 0, 0.1);
}
</style>
