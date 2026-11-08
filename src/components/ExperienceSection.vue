<script setup>
defineProps({
  items: {
    type: Array,
    required: true,
  },
})
</script>

<template>
  <div id="experiencia" class="cv-subsection">
    <h3>Experiência</h3>
    <div class="timeline">
      <article v-for="item in items" :key="item.period" class="timeline-item shadow-sm">
        <p class="timeline-period">{{ item.period }}</p>
        <div class="timeline-body">
          <h4>{{ item.role }}</h4>
          <p class="timeline-company">{{ item.company }}</p>
          <p class="timeline-description">{{ item.description }}</p>
          <p class="experience-technologies">
            <strong>Tecnologias:</strong> {{ item.technologies }}
          </p>
        </div>
      </article>
    </div>
  </div>
</template>
