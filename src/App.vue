<script setup>
import { education, experience, languages, skills } from './data/cv.js'
import EducationSection from './components/EducationSection.vue'
import ExperienceSection from './components/ExperienceSection.vue'

const navigation = [
  { label: 'Quem Sou Eu?', href: '#quem-sou-eu' },
  { label: 'O que faço?', href: '#o-que-faco' },
  { label: 'Hobbies', href: '#hobbies' },
]
</script>

<template>
  <div class="page-shell">
    <header id="inicio" class="site-header">
      <a class="wordmark" href="#inicio" aria-label="Voltar ao início">
        <span class="first-letter">C</span><span class="second-letter">V</span>
      </a>
      <nav class="main-navigation" aria-label="Navegação principal">
        <a v-for="item in navigation" :key="item.href" :href="item.href">
          {{ item.label }}
        </a>
      </nav>
    </header>

    <main>
      <div class="introduction">
        <h1>Tasso Lamar Nunes Lima</h1>
        <p>Fullstack Developer</p>
        <a href="mailto:tassolima2@gmail.com">tassolima2@gmail.com</a>
      </div>
      <section id="quem-sou-eu" class="section-block">
        <h2>Quem Sou Eu?</h2>
        <p>
          Fullstack Developer com 3 anos de experiência a criar aplicações web escaláveis usando
          React e Next.js. Experiência em TypeScript, optimização de desempenho e desenvolvimento de
          interfaces responsivas, com atenção ao design e à experiência de utilização.
        </p>
        <div id="idiomas" class="cv-subsection">
          <h3>Idiomas</h3>
          <ul class="tag-list">
            <li v-for="language in languages" :key="language">{{ language }}</li>
          </ul>
        </div>
        <EducationSection :education="education" />
      </section>

      <section id="o-que-faco" class="section-block">
        <h2>O que faço?</h2>
        <div id="competencias" class="cv-subsection">
          <h3>Competências</h3>
          <ul class="tag-list">
            <li v-for="skill in skills" :key="skill">{{ skill }}</li>
          </ul>
        </div>
        <ExperienceSection :items="experience" />
      </section>

      <section id="hobbies" class="section-block">
        <h2>Hobbies</h2>
        <ul class="hobbies-list">
          <li>Produção musical</li>
          <li>Gaming</li>
        </ul>
      </section>
    </main>

    <footer class="site-footer">
      <p>© 2026 Tasso Lima</p>
      <nav class="social-links" aria-label="Redes sociais">
        <a
          href="https://github.com/NinfarZ"
          target="_blank"
          rel="noopener noreferrer"
          aria-label="GitHub"
        >
          <svg viewBox="0 0 24 24" aria-hidden="true">
            <path
              d="M12 2.5a9.7 9.7 0 0 0-3.1 18.9c.5.1.7-.2.7-.5v-1.8c-2.8.6-3.4-1.2-3.4-1.2-.5-1.1-1.1-1.4-1.1-1.4-.9-.6.1-.6.1-.6 1 .1 1.6 1 1.6 1 .9 1.5 2.3 1.1 2.8.8.1-.6.4-1.1.6-1.3-2.2-.3-4.5-1.1-4.5-4.8 0-1.1.4-2 1-2.7-.1-.3-.4-1.3.1-2.7 0 0 .8-.3 2.7 1a9.4 9.4 0 0 1 4.9 0c1.9-1.3 2.7-1 2.7-1 .5 1.4.2 2.4.1 2.7.6.7 1 1.6 1 2.7 0 3.7-2.3 4.5-4.5 4.8.4.3.7.9.7 1.8v2.7c0 .3.2.6.7.5A9.7 9.7 0 0 0 12 2.5Z"
            />
          </svg>
        </a>
        <a
          href="https://www.linkedin.com/in/tasso-lima-6b7220198/"
          target="_blank"
          rel="noopener noreferrer"
          aria-label="LinkedIn"
        >
          <svg viewBox="0 0 24 24" aria-hidden="true">
            <path
              d="M5.2 3.5a2 2 0 1 1 0 4 2 2 0 0 1 0-4ZM3.5 9h3.4v11.5H3.5V9Zm5.5 0h3.2v1.6h.1c.5-.9 1.6-1.9 3.4-1.9 3.6 0 4.3 2.3 4.3 5.3v6.5h-3.4v-5.8c0-1.4 0-3.1-1.9-3.1s-2.2 1.5-2.2 3v5.9H9V9Z"
            />
          </svg>
        </a>
        <a
          href="https://ninfarz.github.io/"
          target="_blank"
          rel="noopener noreferrer"
          aria-label="Portefólio"
        >
          <svg viewBox="0 0 24 24" aria-hidden="true">
            <path
              d="M14 3h7v7h-2V6.4l-9.3 9.3-1.4-1.4L17.6 5H14V3ZM5 5h6v2H5v12h12v-6h2v8H3V5h2Z"
            />
          </svg>
        </a>
      </nav>
    </footer>
  </div>
</template>
