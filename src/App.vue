<script setup>
import { computed, ref } from "vue";
import ProjectCard from "./components/ProjectCard.vue";

const projects = ref([
  { id: 1, name: "Admin Dashboard", status: "IN_PROGRESS", owner: "Minh" },
  { id: 2, name: "Gas Station Map", status: "TODO", owner: "An" },
  { id: 3, name: "Device Manager", status: "DONE", owner: "Khoa" },
]);

const search = ref("");

const filteredProjects = computed(() => {
  const keyword = search.value.trim().toLowerCase();
  if (!keyword) return projects.value;

  return projects.value.filter((project) =>
    project.name.toLowerCase().includes(keyword),
  );
});
</script>

<template>
  <main class="page-shell">
    <section class="hero">
      <p class="eyebrow">Git Teamwork Practice</p>
      <h1>Mini Project Board111</h1>
      <p class="subtitle">
        Project nhỏ để bạn luyện branch, commit, push, pull request và conflict.
      </p>
    </section>

    <section class="toolbar">
      <input
        v-model="search"
        class="search-input"
        type="search"
        placeholder="Tìm project..."
      />
      <button class="primary-btn" type="button">+ New Project</button>
    </section>

    <section class="project-grid">
      <ProjectCard
        v-for="project in filteredProjects"
        :key="project.id"
        :project="project"
      />
    </section>

    <p v-if="filteredProjects.length === 0" class="empty-state">
      Không tìm thấy project phù hợp.
    </p>
  </main>
</template>
