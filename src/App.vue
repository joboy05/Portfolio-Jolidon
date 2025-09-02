<style scoped>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

body {
  font-family: "Segoe UI", Tahoma, Geneva, Verdana, sans-serif;
  line-height: 1.6;
  color: #333;
  overflow-x: hidden;
}

/* Header */
header {
  position: fixed;
  top: 0;
  width: 100%;
  background: rgba(255, 255, 255, 0.95);
  backdrop-filter: blur(10px);
  z-index: 1000;
  padding: 1rem 0;
  transition: all 0.3s ease;
}

nav {
  max-width: 1200px;
  margin: 0 auto;
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 0 2rem;
}

.logo {
  font-size: 1.5rem;
  font-weight: bold;
  color: #4a5568;
}

.nav-links {
  display: flex;
  list-style: none;
  gap: 2rem;
}

.nav-links a {
  text-decoration: none;
  color: #4a5568;
  font-weight: 500;
  transition: color 0.3s ease;
}

.nav-links a:hover {
  color: #a0805a;
}

.social-links {
  display: flex;
  gap: 1rem;
}

.social-links a {
  color: #4a5568;
  font-size: 1.2rem;
  transition: color 0.3s ease;
}

.social-links a:hover {
  color: #a0805a;
}

/* Hero Section */
.hero {
  min-height: 100vh;
  display: flex;
  align-items: center;
  background: linear-gradient(135deg, #f7fafc 0%, #edf2f7 100%);
  position: relative;
  overflow: hidden;
}

.hero::before {
  content: "";
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background: url('data:image/svg+xml,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 100 100"><defs><pattern id="dots" x="0" y="0" width="10" height="10" patternUnits="userSpaceOnUse"><circle cx="5" cy="5" r="1" fill="%23cbd5e0" opacity="0.5"/></pattern></defs><rect width="100" height="100" fill="url(%23dots)"/></svg>');
  opacity: 0.3;
}

.hero-container {
  max-width: 1200px;
  margin: 0 auto;
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 4rem;
  align-items: center;
  padding: 0 2rem;
  position: relative;
  z-index: 1;
}

.hero-content h1 {
  font-size: 1.2rem;
  color: #718096;
  margin-bottom: 1rem;
  opacity: 0;
  animation: fadeInUp 1s ease 0.2s forwards;
}

.hero-name {
  font-size: 4rem;
  font-weight: 800;
  color: #4a5568;
  line-height: 0.9;
  margin-bottom: 1rem;
  opacity: 0;
  animation: fadeInUp 1s ease 0.4s forwards;
}

.hero-title {
  background: #a0805a;
  color: white;
  padding: 1rem 2rem;
  border-radius: 50px;
  font-size: 1.2rem;
  font-weight: 500;
  margin-bottom: 2rem;
  display: inline-block;
  opacity: 0;
  animation: fadeInUp 1s ease 0.6s forwards;
}

.hero-btn {
  background: #a0805a;
  color: white;
  padding: 1rem 2rem;
  border: none;
  border-radius: 50px;
  font-size: 1.1rem;
  font-weight: 500;
  cursor: pointer;
  transition: all 0.3s ease;
  opacity: 0;
  animation: fadeInUp 1s ease 0.8s forwards;
}

.hero-btn:hover {
  background: #8b6f47;
  transform: translateY(-2px);
  box-shadow: 0 10px 25px rgba(160, 128, 90, 0.3);
}

.hero-image {
  position: relative;
  display: flex;
  justify-content: center;
  align-items: center;
}

.hero-circle {
  width: 400px;
  height: 400px;
  background: #4a5568;
  border-radius: 50%;
  position: relative;
  overflow: hidden;
  box-shadow: 0 20px 60px rgba(74, 85, 104, 0.3);
  opacity: 0;
  animation: fadeInScale 1s ease 0.5s forwards;
}

.hero-circle::before {
  content: "";
  position: absolute;
  top: 20px;
  right: 20px;
  width: 80px;
  height: 80px;
  background: url('data:image/svg+xml,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 100 100"><defs><pattern id="dots-white" x="0" y="0" width="20" height="20" patternUnits="userSpaceOnUse"><circle cx="10" cy="10" r="2" fill="white" opacity="0.3"/></pattern></defs><rect width="100" height="100" fill="url(%23dots-white)"/></svg>');
}

.profile-img {
  width: 100%;
  height: 100%;
  object-fit: cover;
  border-radius: 50%;
}

/* Floating Elements */
.floating-shapes {
  position: absolute;
  width: 100%;
  height: 100%;
  pointer-events: none;
}

.shape {
  position: absolute;
  background: #a0805a;
  opacity: 0.1;
  animation: float 6s ease-in-out infinite;
}

.shape.circle {
  border-radius: 50%;
}

.shape:nth-child(1) {
  width: 60px;
  height: 60px;
  top: 20%;
  left: 10%;
  animation-delay: 0s;
}

.shape:nth-child(2) {
  width: 40px;
  height: 40px;
  top: 60%;
  left: 80%;
  animation-delay: 2s;
}

.shape:nth-child(3) {
  width: 30px;
  height: 30px;
  top: 80%;
  left: 20%;
  animation-delay: 4s;
}

/* About Section */
.section {
  padding: 5rem 0;
}

.container {
  max-width: 1200px;
  margin: 0 auto;
  padding: 0 2rem;
}

.section-title {
  font-size: 3rem;
  font-weight: 800;
  color: #4a5568;
  text-align: center;
  margin-bottom: 3rem;
}

.about-grid {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 4rem;
  align-items: center;
}

.about-text {
  font-size: 1.1rem;
  line-height: 1.8;
  color: #718096;
}

.skills-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
  gap: 2rem;
  margin-top: 3rem;
}

.skill-card {
  background: white;
  padding: 2rem;
  border-radius: 15px;
  box-shadow: 0 10px 30px rgba(0, 0, 0, 0.1);
  transition: transform 0.3s ease;
}

.skill-card:hover {
  transform: translateY(-5px);
}

.skill-header {
  display: flex;
  align-items: center;
  gap: 1rem;
  margin-bottom: 1.5rem;
}

.skill-card i {
  font-size: 2.5rem;
  color: #a0805a;
}

.skill-info h3 {
  font-size: 1.3rem;
  color: #4a5568;
  margin-bottom: 0.5rem;
}

.skill-level {
  font-size: 0.9rem;
  color: #718096;
  font-weight: 500;
}

.progress-bar {
  width: 100%;
  height: 8px;
  background: #e2e8f0;
  border-radius: 10px;
  overflow: hidden;
  margin-bottom: 0.5rem;
}

.progress-fill {
  height: 100%;
  background: linear-gradient(90deg, #a0805a, #8b6f47);
  border-radius: 10px;
  transition: width 2s ease;
  width: 0;
}

.progress-fill.animate {
  width: var(--progress);
}

/* Projects Section */
.projects {
  background: #f7fafc;
}

.projects-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(350px, 1fr));
  gap: 2rem;
}

.project-card {
  background: white;
  border-radius: 15px;
  overflow: hidden;
  box-shadow: 0 10px 30px rgba(0, 0, 0, 0.1);
  transition: transform 0.3s ease;
}

.project-card:hover {
  transform: translateY(-5px);
}

.project-img {
  height: 200px;
  background: linear-gradient(45deg, #a0805a, #4a5568);
  display: flex;
  align-items: center;
  justify-content: center;
  color: white;
  font-size: 3rem;
}

.project-content {
  padding: 2rem;
}

.project-title {
  font-size: 1.5rem;
  font-weight: 700;
  color: #4a5568;
  margin-bottom: 1rem;
}

.project-desc {
  color: #718096;
  margin-bottom: 1.5rem;
}

.project-tech {
  display: flex;
  gap: 0.5rem;
  flex-wrap: wrap;
}

.tech-tag {
  background: #a0805a;
  color: white;
  padding: 0.3rem 0.8rem;
  border-radius: 20px;
  font-size: 0.9rem;
}

/* Contact Section */
.contact {
  background: #4a5568;
  color: white;
}

.contact .section-title {
  color: white;
}

.contact-grid {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 4rem;
}

.contact-info h3 {
  font-size: 1.5rem;
  margin-bottom: 1rem;
  color: #a0805a;
}

.contact-item {
  display: flex;
  align-items: center;
  gap: 1rem;
  margin-bottom: 1rem;
}

.contact-item i {
  color: #a0805a;
  font-size: 1.2rem;
}

.contact-form {
  display: grid;
  gap: 1rem;
}

.form-group {
  display: grid;
  gap: 0.5rem;
}

.form-group label {
  color: #a0805a;
  font-weight: 500;
}

.form-group input,
.form-group textarea {
  padding: 1rem;
  border: none;
  border-radius: 10px;
  font-size: 1rem;
  font-family: inherit;
}

.form-group textarea {
  height: 120px;
  resize: vertical;
}

.form-btn {
  background: #a0805a;
  color: white;
  padding: 1rem 2rem;
  border: none;
  border-radius: 10px;
  font-size: 1rem;
  cursor: pointer;
  transition: background 0.3s ease;
}

.form-btn:hover {
  background: #8b6f47;
}

/* Footer */
footer {
  background: #2d3748;
  color: white;
  text-align: center;
  padding: 2rem 0;
}

/* Animations */
@keyframes fadeInUp {
  from {
    opacity: 0;
    transform: translateY(30px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

@keyframes fadeInScale {
  from {
    opacity: 0;
    transform: scale(0.8);
  }
  to {
    opacity: 1;
    transform: scale(1);
  }
}

@keyframes float {
  0%,
  100% {
    transform: translateY(0px) rotate(0deg);
  }
  50% {
    transform: translateY(-20px) rotate(180deg);
  }
}

/* Mobile Responsiveness */
@media (max-width: 1024px) {
  .hero-container {
    gap: 3rem;
  }

  .hero-circle {
    width: 350px;
    height: 350px;
  }

  .hero-name {
    font-size: 3.5rem;
  }
}

@media (max-width: 768px) {
  .nav-links {
    display: none;
  }

  .logo {
    font-size: 1rem;
  }

  .social-links {
    gap: 0.5rem;
  }

  .hero-container {
    grid-template-columns: 1fr;
    text-align: center;
    gap: 2rem;
    padding: 2rem 1rem;
  }

  .hero-name {
    font-size: 2.8rem;
  }

  .hero-circle {
    width: 280px;
    height: 280px;
  }

  .hero-title {
    font-size: 1rem;
    padding: 0.8rem 1.5rem;
  }

  .section {
    padding: 3rem 0;
  }

  .section-title {
    font-size: 2.2rem;
  }

  .about-grid,
  .contact-grid {
    grid-template-columns: 1fr;
    gap: 2rem;
  }

  .projects-grid {
    grid-template-columns: 1fr;
  }

  .skills-grid {
    grid-template-columns: 1fr;
  }

  .container {
    padding: 0 1rem;
  }
}

@media (max-width: 480px) {
  .hero-name {
    font-size: 2.2rem;
  }

  .hero-circle {
    width: 250px;
    height: 250px;
  }

  .section-title {
    font-size: 1.8rem;
  }

  .skill-card {
    padding: 1.5rem;
  }

  .project-card {
    margin: 0 0.5rem;
  }

  nav {
    padding: 0 1rem;
  }

  .logo {
    font-size: 0.9rem;
  }

  .social-links a {
    font-size: 1rem;
  }
}

/* Scroll animations */
.fade-in {
  opacity: 0;
  transform: translateY(30px);
  transition: all 0.8s ease;
}

.fade-in.visible {
  opacity: 1;
  transform: translateY(0);
}
</style>
<template>
  <!-- Header -->
  <header>
    <nav>
      <div class="logo">jolidonhoungue30@gmail.com</div>
      <ul class="nav-links">
        <li><a href="#home">Contact</a></li>
        <li><a href="#projects">Project</a></li>
        <li><a href="#about">Resume</a></li>
      </ul>
      <div class="social-links">
        <a href="#"><i class="fab fa-linkedin"></i></a>
        <a href="mailto:jolidonhoungue30@gmail.com"><i class="fas fa-envelope"></i></a>
        <a href="#"><i class="fas fa-phone"></i></a>
      </div>
    </nav>
  </header>

  <!-- Hero Section -->
  <section class="hero" id="home">
    <div class="floating-shapes">
      <div class="shape circle"></div>
      <div class="shape circle"></div>
      <div class="shape circle"></div>
    </div>

    <div class="hero-container">
      <div class="hero-content">
        <h1>Hello Everyone, I Am</h1>
        <div class="hero-name">Jolidon<br />HOUNGUE</div>
        <div class="hero-title">Web Designer & Development</div>
        <button class="hero-btn" onclick="scrollToSection('contact')">Contact Me</button>
      </div>
      <div class="hero-image">
        <div class="hero-circle">
          <!-- Remplacez cette div par votre image -->
          <img
            src="./assets/WhatsApp Image 2025-09-02 at 01.45.10.jpeg"
            style="
              width: 100%;
              height: 100%;
              background: linear-gradient(45deg, #4a5568, #718096);
              display: flex;
              align-items: center;
              justify-content: center;
              color: white;
            "
          />
        </div>
      </div>
    </div>
  </section>

  <!-- About Section -->
  <section class="section" id="about">
    <div class="container">
      <h2 class="section-title fade-in">À Propos</h2>
      <div class="about-grid">
        <div class="about-text fade-in">
          <p>
            Je suis un développeur web passionné avec une expertise en design et
            développement moderne. J'aime créer des expériences utilisateur
            exceptionnelles et des solutions web innovantes.
          </p>
          <p>
            Avec plusieurs années d'expérience, je maîtrise les dernières technologies web
            et j'aide les entreprises à réaliser leurs visions numériques.
          </p>
        </div>
        <div class="skills-grid fade-in">
          <div class="skill-card">
            <div class="skill-header">
              <i class="fab fa-html5"></i>
              <div class="skill-info">
                <h3>HTML5</h3>
                <div class="skill-level">Avancé - 90%</div>
              </div>
            </div>
            <div class="progress-bar">
              <div class="progress-fill" style="--progress: 90%"></div>
            </div>
          </div>

          <div class="skill-card">
            <div class="skill-header">
              <i class="fab fa-css3-alt"></i>
              <div class="skill-info">
                <h3>CSS3</h3>
                <div class="skill-level">Avancé - 85%</div>
              </div>
            </div>
            <div class="progress-bar">
              <div class="progress-fill" style="--progress: 85%"></div>
            </div>
          </div>

          <div class="skill-card">
            <div class="skill-header">
              <i class="fab fa-js-square"></i>
              <div class="skill-info">
                <h3>JavaScript</h3>
                <div class="skill-level">Intermédiaire - 75%</div>
              </div>
            </div>
            <div class="progress-bar">
              <div class="progress-fill" style="--progress: 75%"></div>
            </div>
          </div>

          <div class="skill-card">
            <div class="skill-header">
              <i class="fab fa-css3"></i>
              <div class="skill-info">
                <h3>Tailwind CSS</h3>
                <div class="skill-level">Intermédiaire - 80%</div>
              </div>
            </div>
            <div class="progress-bar">
              <div class="progress-fill" style="--progress: 80%"></div>
            </div>
          </div>

          <div class="skill-card">
            <div class="skill-header">
              <i class="fas fa-mobile-alt"></i>
              <div class="skill-info">
                <h3>Flutter (Dart)</h3>
                <div class="skill-level">Débutant - 45%</div>
              </div>
            </div>
            <div class="progress-bar">
              <div class="progress-fill" style="--progress: 45%"></div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>

  <!-- Projects Section -->
  <section class="section projects" id="projects">
    <div class="container">
      <h2 class="section-title fade-in">Mes Projets</h2>
      <div class="projects-grid">
        <div class="project-card fade-in">
          <div class="project-img">
            <i class="fas fa-laptop-code"></i>
          </div>
          <div class="project-content">
            <h3 class="project-title">Site E-commerce</h3>
            <p class="project-desc">
              Une plateforme e-commerce moderne avec panier d'achat, paiement sécurisé et
              administration.
            </p>
            <div class="project-tech">
              <span class="tech-tag">React</span>
              <span class="tech-tag">Node.js</span>
              <span class="tech-tag">MongoDB</span>
            </div>
          </div>
        </div>

        <div class="project-card fade-in">
          <div class="project-img">
            <i class="fas fa-mobile-alt"></i>
          </div>
          <div class="project-content">
            <h3 class="project-title">Application Mobile</h3>
            <p class="project-desc">
              Application mobile responsive avec interface utilisateur moderne et
              animations fluides.
            </p>
            <div class="project-tech">
              <span class="tech-tag">React Native</span>
              <span class="tech-tag">Firebase</span>
              <span class="tech-tag">Redux</span>
            </div>
          </div>
        </div>

        <div class="project-card fade-in">
          <div class="project-img">
            <i class="fas fa-chart-line"></i>
          </div>
          <div class="project-content">
            <h3 class="project-title">Dashboard Analytics</h3>
            <p class="project-desc">
              Tableau de bord interactif pour la visualisation de données en temps réel.
            </p>
            <div class="project-tech">
              <span class="tech-tag">Vue.js</span>
              <span class="tech-tag">D3.js</span>
              <span class="tech-tag">API REST</span>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>

  <!-- Contact Section -->
  <section class="section contact" id="contact">
    <div class="container">
      <h2 class="section-title fade-in">Me Contacter</h2>
      <div class="contact-grid">
        <div class="contact-info fade-in">
          <h3>Restons en contact</h3>
          <div class="contact-item">
            <i class="fas fa-envelope"></i>
            <span>jolidonhoungue30@gmail.com</span>
          </div>
          <div class="contact-item">
            <i class="fas fa-phone"></i>
            <span>+229 XX XX XX XX</span>
          </div>
          <div class="contact-item">
            <i class="fas fa-map-marker-alt"></i>
            <span>Cotonou, Bénin</span>
          </div>
        </div>

        <form class="contact-form fade-in" onsubmit="handleSubmit(event)">
          <div class="form-group">
            <label for="name">Nom</label>
            <input type="text" id="name" name="name" required />
          </div>
          <div class="form-group">
            <label for="email">Email</label>
            <input type="email" id="email" name="email" required />
          </div>
          <div class="form-group">
            <label for="message">Message</label>
            <textarea id="message" name="message" required></textarea>
          </div>
          <button type="submit" class="form-btn">Envoyer le message</button>
        </form>
      </div>
    </div>
  </section>

  <!-- Footer -->
  <footer>
    <div class="container">
      <p>&copy; 2025 Jolidon HOUNGUE. Tous droits réservés.</p>
    </div>
  </footer>
</template>
<script setup>
// Smooth scrolling
function scrollToSection(sectionId) {
  document.getElementById(sectionId).scrollIntoView({
    behavior: "smooth",
  });
}

// Scroll animations
function isElementInViewport(el) {
  const rect = el.getBoundingClientRect();
  return (
    rect.top >= 0 &&
    rect.left >= 0 &&
    rect.bottom <= (window.innerHeight || document.documentElement.clientHeight) &&
    rect.right <= (window.innerWidth || document.documentElement.clientWidth)
  );
}

// Animate progress bars
function animateProgressBars() {
  const progressBars = document.querySelectorAll(".progress-fill");
  progressBars.forEach((bar) => {
    if (isElementInViewport(bar.parentElement)) {
      bar.classList.add("animate");
    }
  });
}

function handleScrollAnimations() {
  const elements = document.querySelectorAll(".fade-in");
  elements.forEach((el) => {
    if (isElementInViewport(el)) {
      el.classList.add("visible");
    }
  });
  animateProgressBars();
}

// Header background on scroll
function handleHeaderScroll() {
  const header = document.querySelector("header");
  if (window.scrollY > 100) {
    header.style.background = "rgba(255, 255, 255, 0.98)";
    header.style.boxShadow = "0 2px 20px rgba(0,0,0,0.1)";
  } else {
    header.style.background = "rgba(255, 255, 255, 0.95)";
    header.style.boxShadow = "none";
  }
}

// Form submission
function handleSubmit(event) {
  event.preventDefault();
  const formData = new FormData(event.target);
  const data = Object.fromEntries(formData);

  // Simuler l'envoi
  alert("Message envoyé avec succès! Merci pour votre contact.");
  event.target.reset();
}

// Event listeners
window.addEventListener("scroll", () => {
  handleScrollAnimations();
  handleHeaderScroll();
});

window.addEventListener("load", handleScrollAnimations);

// Smooth scroll for navigation
document.querySelectorAll('a[href^="#"]').forEach((anchor) => {
  anchor.addEventListener("click", function (e) {
    e.preventDefault();
    const target = document.querySelector(this.getAttribute("href"));
    if (target) {
      target.scrollIntoView({
        behavior: "smooth",
        block: "start",
      });
    }
  });
});

// Typing effect for hero name
function typeWriter(element, text, speed = 100) {
  let i = 0;
  element.innerHTML = "";
  function type() {
    if (i < text.length) {
      element.innerHTML += text.charAt(i);
      i++;
      setTimeout(type, speed);
    }
  }
  type();
}

// Initialize typing effect
window.addEventListener("load", () => {
  setTimeout(() => {
    const heroName = document.querySelector(".hero-name");
    typeWriter(heroName, "Jolidon\nHOUNGUE", 80);
  }, 1500);
});
</script>
