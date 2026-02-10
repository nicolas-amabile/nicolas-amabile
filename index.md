---
layout: default
title: Nicolas Amabile Resume
---

<link rel="stylesheet" href="assets/style.css">

<script>
function toggleTheme(){
  const t = document.documentElement;
  t.setAttribute("data-theme", t.getAttribute("data-theme") === "dark" ? "light" : "dark");
}
function toggleResume(){
  const f = document.getElementById("full");
  const s = document.getElementById("short");
  if (f.style.display==="none") {
    f.style.display="block";
    s.style.display="none";
  } else {
    f.style.display="none";
    s.style.display="block";
  }
}
</script>

<div class="controls">
  <button class="toggle" onclick="toggleTheme()">🌗 Theme</button>
  <button class="toggle secondary" onclick="toggleResume()">📄 Version</button>
</div>

# Nicolás Amábile

**Senior SDET / QA Automation Architect · Hybrid Developer**

📍 Uruguay ·
🔗 [LinkedIn](https://linkedin.com/in/nico-amabile) ·
💻 [GitHub](https://github.com/nicolas-amabile)

<div id="full">
  {% capture fullresume %}
  {% include_relative resume.md %}
  {% endcapture %}
  {{ "" }}
  {{ fullresume | markdownify }}
</div>

<div id="short" style="display:none">
  {% capture shortresume %}
  {% include_relative resume-short.md %}
  {% endcapture %}
  {{ "" }}
  {{ shortresume | markdownify }}
</div>
