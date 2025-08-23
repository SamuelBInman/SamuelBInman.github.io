---
title: Samuel B. Inman
permalink: /
layout: home
entries_layout: grid
show_excerpts: false
paginate: false   # <— stops the recent posts section
---

# Thank you for the patience while this site is under construction

I study the **degradation and lifetime of structural and electrochemical materials**, focusing on understanding why materials fail and designing alloys that endure in demanding environments.  

My work bridges fundamental insights with practical applications to improve the reliability of the technologies we depend on every day.

---

## Highlights

<div class="slider-container">
  <div class="slider">
    <!-- Slide 1 -->
    <div class="slide active">
      <img src="/assets/images/slide1.jpg" alt="Research Highlight 1">
      <p><strong>Research Highlight:</strong> Microstructure as a tool for predicting corrosion resistance.  
      <a href="/research/">Learn more →</a></p>
    </div>

    <!-- Slide 2 -->
    <div class="slide">
      <img src="/assets/images/slide2.jpg" alt="Teaching Highlight">
      <p><strong>Teaching Highlight:</strong> Developing future leaders in materials science.  
      <a href="/teaching/">See teaching →</a></p>
    </div>

    <!-- Slide 3 -->
    <div class="slide">
      <img src="/assets/images/slide3.jpg" alt="Publications Highlight">
      <p><strong>Publications:</strong> Selected works in corrosion and alloy design.  
      <a href="/publications/">Read more →</a></p>
    </div>
  </div>

  <!-- Navigation arrows -->
  <a class="prev" onclick="moveSlide(-1)">&#10094;</a>
  <a class="next" onclick="moveSlide(1)">&#10095;</a>
</div>

<script>
let currentSlide = 0;
const slides = document.querySelectorAll(".slide");

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

document.addEventListener("DOMContentLoaded", () => showSlide(currentSlide));
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
  padding: 12px;
  color: #333;
  font-weight: bold;
  font-size: 24px;
  transition: 0.3s;
  user-select: none;
}

.next { right: 0; }
.prev { left: 0; }

.prev:hover, .next:hover {
  background-color: rgba(0,0,0,0.1);
  border-radius: 50%;
}
</style>
