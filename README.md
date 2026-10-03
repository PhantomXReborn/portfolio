<div align="center">
  
  # ✦ PORTFOLIO ✦
  
  ### *Where Code Meets Identity*
  
  [![GitHub](https://img.shields.io/badge/🌌_PhantomXReborn-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/PhantomXReborn)
  [![Live Demo](https://img.shields.io/badge/✨_Student_Made-3b7dbd?style=for-the-badge&logo=vercel&logoColor=white)](https://beta-bite-website-4iwcyg76n-phantomxreborns-projects.vercel.app/)
  [![License](https://img.shields.io/badge/📜_MIT_License-blue?style=for-the-badge)](LICENSE)
  [![Made with](https://img.shields.io/badge/🔎_Made_by_Reece_Hannah-blue?style=for-the-badge)](https://github.com/PhantomXReborn)
  
  > *"Collecting Experience through Ideas and Creativity."*

</div>

---

## 🌠 **The Vision**

Welcome to my portfolio! A digital storage system where projects are set free, and innovation knows no bounds. This isn't just a website; it's an immersive journey through the creative cosmos, featuring:

<div align="center">
  
  | 🎮 **Projects** | ⚙️ **Coding Languages** |
  |:---:|:---:|
  | Yatzy • Resume • Emergency Waitlist | HTML5 • CSS • JavaScript |

</div>

---

## ✨ **Features**

<div align="center">
  
  | 🌌 **Galactic Canvas** | 🎠 **Project Carousel** | 📡 **Live GitHub Feed** |
  |:---:|:---:|:---:|
  | Animated particles, stars & code glyphs | Interactive slider with tech overlays | Real-time repository showcase |
  
  | 🔮 **Theme Shapeshifter** | 📊 **Scroll Alchemy** | ✨ **Responsive Magic** |
  |:---:|:---:|:---:|
  | Dark/Light mode with ⌨️ 't' shortcut | Animated counters & progress bar | Seamless across all dimensions |

</div>

## 🛸 **Tech**

<div align="center">
  
  ### Frontend
  ![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=flat-square&logo=html5&logoColor=white)
  ![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=flat-square&logo=css3&logoColor=white)
  ![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black)
  
  ### Visuals
  ![Font Awesome](https://img.shields.io/badge/Font_Awesome-528DD7?style=flat-square&logo=fontawesome&logoColor=white)
  ![Google Fonts](https://img.shields.io/badge/Google_Fonts-4285F4?style=flat-square&logo=google&logoColor=white)  
</div>

---

## 🗂️ **Cosmic Structure**

```mermaid
graph TD
    A[Portfolio/] --> B[portfolio.html]
    A --> C[style.css]
    A --> D[README.md]
    A --> E[License]
```

✨ Particle Theme
```javascript
  const particles = document.querySelectorAll('.particle');
  particles.forEach((p, i) => {
    p.style.left = (i * 10 + Math.random() * 5) + '%';
    p.style.animationDelay = (Math.random() * 8) + 's';
    p.style.animationDuration = (18 + Math.random() * 10) + 's';
  });
});
```
🎯 Smooth Scrolling
```javascript
filterButtons.forEach(btn => {
  btn.addEventListener('click', function() {
    filterButtons.forEach(b => b.classList.remove('active'));
    this.classList.add('active');

    const filterValue = this.getAttribute('data-filter');
      filterProjects(filterValue);
  });
});
}, { threshold: 0.5 });
```

 Filter Button Effect
```javascript
      document.querySelectorAll('a[href^="#"]').forEach(anchor => {
        anchor.addEventListener('click', function(e) {
          const href = this.getAttribute('href');
          if (href === '#') return; // skip empty links

          const target = document.querySelector(href);
          if (target) {
            e.preventDefault();
            target.scrollIntoView({
              behavior: 'smooth',
              block: 'start'
            });
          }
        });
      });
}, { threshold: 0.5 });
```

📜 License
<div>
This project is blessed under the MIT License — a sacred text that allows you to forge, enhance, and share your own cosmic creations. See the LICENSE file for the full incantation.
</div>

🌌 Fork the repository

✨ Create a feature branch (git checkout -b feature/cosmic-idea)

🚀 Commit your changes (git commit -m 'Add cosmic idea')

🌠 Push to the branch (git push origin feature/cosmic-idea)

🌟 Open a Pull Request to the universe

📡 Creator
<div align="center"> <br>
✦ Made By Reece Hannah ✦

<sub>2026 Reece Hannah • MIT License Used</sub>

</div>
