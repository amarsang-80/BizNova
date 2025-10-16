
---

## ⚙️ How It Works

### 1️⃣ Navigation Bar
- Sticky top navbar with smooth scroll to sections.
- Includes a “Get Quote” button linked to the Contact section.

### 2️⃣ Hero Section
- Main headline, subtext, CTA buttons, and stats.
- Right side image: `assets/images/hero.jpg`.

### 3️⃣ Services Section
- Three service cards with icons and descriptions.
- Uses Font Awesome icons (`fa-code`, `fa-palette`, `fa-shield-halved`).

### 4️⃣ Projects / Portfolio
- 3 project cards with image and brief description.
- Each card uses Bootstrap grid + shadow.

### 5️⃣ Pricing
- 3-tier pricing layout (Starter, Business, Enterprise).
- Highlighted “Business” plan with primary border.

### 6️⃣ Testimonials
- Swiper carousel showing client feedback.
- Each card has client photo, name, and role.

### 7️⃣ Team
- 4 team members with names, roles, and images.
- Bootstrap grid used for layout.

### 8️⃣ Contact Form
- Simple Bootstrap form with demo JS alert (no backend yet).
- Contact details (location, email, phone) shown beside the form.

### 9️⃣ Footer
- 3 columns: About, Quick Links, Subscribe form.
- Auto year update using JavaScript (`document.getElementById('year')`).

---

## 🧠 JavaScript Functionality

```javascript
// Auto update year
document.getElementById('year').innerText = new Date().getFullYear();

// AOS animation initialization
AOS.init({ duration: 700, once: true });

// Swiper slider setup
const swiper = new Swiper('.swiper-container', {
  slidesPerView: 1,
  loop: true,
  autoplay: { delay: 3500 },
});

// Smooth scroll behavior
document.querySelectorAll('a[href^=\"#\"]').forEach(a => {
  a.addEventListener('click', e => {
    e.preventDefault();
    document.querySelector(a.getAttribute('href')).scrollIntoView({ behavior: 'smooth' });
  });
});
