<script setup>
defineProps({
  education: {
    type: Array,
    required: true,
  },
})
</script>

<template>
  <div id="formacao" class="cv-subsection">
    <h3>Formação</h3>
    <div class="education-list">
      <article v-for="item in education" :key="item.period" class="education-item shadow-sm">
        <p class="timeline-period">{{ item.period }}</p>
        <div>
          <h4>{{ item.course }}</h4>
          <p class="timeline-company">{{ item.school }}</p>
          <p class="timeline-description">{{ item.detail }}</p>
        </div>
      </article>
    </div>
  </div>
</template>
