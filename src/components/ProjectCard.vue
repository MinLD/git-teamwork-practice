<script setup>
defineProps({
  project: {
    type: Object,
    required: true,
  },
})
</script>

<template>
  <article class="project-card">
    <div class="project-card__top">
      <span class="status-badge">{{ project.status }}</span>
      <button class="icon-btn" type="button" aria-label="Project menu">•••</button>
    </div>

    <h2>{{ project.name }}</h2>
    <p>Owner: {{ project.owner }}</p>

    <div class="project-card__actions">
      <button type="button">View</button>
      <button type="button">Edit</button>
    </div>
  </article>
</template>
