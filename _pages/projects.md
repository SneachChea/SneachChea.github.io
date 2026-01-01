---
layout: single
title: Projects
permalink: /projects/
---

<style>
.projects-container {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
  gap: 20px;
  margin-top: 20px;
}

.project-card {
  border: 1px solid #e0e0e0;
  border-radius: 8px;
  padding: 20px;
  box-shadow: 0 2px 6px rgba(0,0,0,0.1);
  transition: transform 0.2s, box-shadow 0.2s;
}

.project-card:hover {
  transform: translateY(-4px);
  box-shadow: 0 4px 12px rgba(0,0,0,0.15);
}

.project-title {
  font-size: 1.3em;
  font-weight: bold;
  margin-bottom: 10px;
  text-align: center;
  color: #333;
}

.project-description {
  color: #666;
  margin-bottom: 15px;
  line-height: 1.6;
  text-align: center;
}

.project-thumbnail {
  width: 100%;
  height: 180px;
  object-fit: cover;
  border-radius: 6px;
  display: block;
  margin-bottom: 12px;
}

.project-tags {
  display: flex;
  flex-wrap: wrap;
  gap: 8px;
  margin-bottom: 15px;
} 

.tag {
  background-color: #f0f0f0;
  color: #333;
  padding: 4px 10px;
  border-radius: 12px;
  font-size: 0.85em;
}

.project-link {
  color: #0066cc;
  text-decoration: none;
  font-weight: 500;
  text-align: center;
}

.project-link:hover {
  text-decoration: underline;
}
</style>

## My Projects

Below are some of the projects I've worked on:

<div class="projects-container">
  <!-- Example Project 1 -->
  <div class="project-card">
    <img class="project-thumbnail" src="/imgs/projects/logo_footix.png" alt="Miniature de Footix" loading="lazy">
    <div class="project-title">Footix</div>
    <div class="project-description">
      Footix is your intelligent companion for football analysis and prediction.
    </div>
    <div class="project-tags">
      <span class="tag">Python</span>
      <span class="tag">Machine Learning</span>
    </div>
    <a href="https://github.com/SneachChea/footix" class="project-link">View on GitHub →</a>
  </div>

{% comment %}
  <!-- Example Project 2 -->
  <div class="project-card">
    <div class="project-title">Footix</div>
    <div class="project-description">
    brief
    </div>
    <div class="project-tags">
      <span class="tag">Python</span>
      <span class="tag">AI</span>
    </div>
    <a href="https://github.com/SneachChea/footix" class="project-link">View on GitHub →</a>
  </div>

  <!-- Example Project 3 -->
  <div class="project-card">
    <div class="project-title">Project Title 3</div>
    <div class="project-description">
      Brief description of your project. Explain what it does and what problem it solves.
    </div>
    <div class="project-tags">
      <span class="tag">React</span>
      <span class="tag">AI</span>
    </div>
    <a href="https://github.com" class="project-link">View on GitHub →</a>
  </div>
  {% endcomment %}
</div>
