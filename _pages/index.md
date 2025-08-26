---
title: Samuel B. Inman
permalink: /
layout: home
entries_layout: grid
show_excerpts: false
paginate: false   # <— stops the recent posts section
---


I study the **degradation and lifetime of structural and electrochemical materials**, focusing on understanding why materials fail and designing alloys that endure in demanding environments.  

My work bridges fundamental insights with practical applications to improve the reliability of the technologies we depend on every day.

---

## Highlights

<div class="slider-container">
  <div class="slider">
    <!-- Slide 1 -->
    <div class="slide active">
      <img src="/assets/images/MultiPhase.png" alt="Multi Phase Passivity">
      <p><strong>Corroison Behavior of Multi-Phase Alloys:</strong> How do we isolate the corrosion behavior of multi-phase alloys into contributions from each individual phase?  
      <a href="https://link.springer.com/article/10.1007/s11661-024-07572-9">Learn more →</a></p>
    </div>

    <!-- Slide 2 -->
    <div class="slide">
      <img src="/assets/images/FeCrAlTi.jpg" alt="Multi-cation Passivity">
      <p><strong>Multi-cation Passivity:</strong> How can multiple cations working together coexist in the passive film... and improve the long-term stability?  
      <a href="https://www.sciencedirect.com/science/article/abs/pii/S2589152925000377" target="_blank">Learn More</a></p>
    </div>

    <!-- Slide 3 -->
    <div class="slide">
      <img src="/assets/images/StochasticCreep.jpg" alt="Stochastic Room Temperature Creep">
      <p><strong>Stochastic Behavior of RT Creep:</strong> How much does sample-to-sample variation affect room temperature creep? Can this extrapolate into lifespen predictions?
      <a href="https://www.sciencedirect.com/science/article/abs/pii/S0749641925000853">Read more →</a></p>
    </div>
  </div>

  <!-- Navigation arrows -->
  <a class="prev" onclick="moveSlide(-1)">&#10094;</a>
  <a class="next" onclick="moveSlide(1)">&#10095;</a>
</div>

<script>
let currentSlide = 0;
let slides;

function showSlide(index) {
  slides.forEach((slide, i) => {
    slide.classList.remove("active");
    if (i === index) slide.classList.add("active");
  });
}

function moveSlide(step) {
  currentSlide = (currentSlide + step + slides.length) % slides.length;
  showSlide(currentSlide);
}

document.addEventListener("DOMContentLoaded", () => {
  slides = document.querySelectorAll(".slide");
  showSlide(currentSlide);
});
</script>

<style>
.slider-container {
  position: relative;
  max-width: 700px;
  margin: auto;
  overflow: hidden;
}

.slider .slide {
  display: none;
  text-align: center;
}

.slider .slide.active {
  display: block;
}

.slider img {
  width: 100%;
  max-height: 350px;
  object-fit: cover;
  border-radius: 10px;
}

.prev, .next {
  cursor: pointer;
  position: absolute;
  top: 50%;
  transform: translateY(-50%);
  padding: 12px;
  color: #333;
  font-weight: bold;
  font-size: 28px;
  transition: 0.3s;
  user-select: none;
  background: rgba(255, 255, 255, 0.7);
  border-radius: 50%;
  z-index: 1000;
}

.next { right: 10px; }
.prev { left: 10px; }

.prev:hover, .next:hover {
  background-color: rgba(0,0,0,0.2);
  color: white;
}
</style>
