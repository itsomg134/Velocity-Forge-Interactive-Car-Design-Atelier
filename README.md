# Velocity Forge — Interactive Car Design Atelier

![Preview](https://via.placeholder.com/1200x630/0a0c10/f97316?text=Velocity+Forge+Showcase)

> **Live configurator | Futuristic UI | Bespoke automotive design studio**

Velocity Forge is an immersive, single-page website that brings car design to life. It features an interactive color configurator, dynamic rim styling, and a bold visual identity — perfect for design portfolios, concept studios, or automotive branding.

##  Features

- ** Live Car Configurator**  
  Change exterior paint in real-time with a color picker.  
  Swap between three rim styles: *Dark Alloy*, *Silver Forged*, and *Gold Rush*.

- ** Dynamic Accent System**  
  Instantly adjust design accents (Neon Orange, Cyber Cyan, Phantom Purple) — strokes and details update live.

- ** Hero Section with Vector Art**  
  Custom SVG car illustration styled to match the configurator.

- ** Fully Responsive**  
  Fluid grid, mobile-friendly navigation, and smooth scrolling.

- ** Modern UI/UX**  
  Glassmorphism cards, gradient text, glow buttons, and a dark cosmic theme with orange highlights.

- ** Concept Gallery**  
  Placeholder image grid to showcase design studies (easily replaceable with actual renders).

- ** Call-to-Action**  
  "Start your design brief" button with interactive toast feedback.

---

##  Tech Stack

| Technology       | Purpose                         |
|------------------|---------------------------------|
| HTML5            | Semantic structure              |
| CSS3             | Custom styling, Flex/Grid, animations |
| JavaScript (ES6) | Dynamic configurator logic      |
| SVG              | Scalable vector car graphics    |
| Font Awesome 6   | Icons                           |
| Google Fonts     | Inter + Space Grotesk           |

---

##  Getting Started

### 1. Clone the repository

```bash
git clone https://github.com/yourusername/velocity-forge.git
cd velocity-forge
```

### 2. Open the project

Simply open `index.html` in your favorite browser — no build steps or dependencies required.

```bash
# Example (macOS/Linux)
open index.html

# Or just double-click the file
```

---

##  Customization Guide

### Change the car body color programmatically

The configurator uses an `<input type="color">` bound to the main SVG path.  
You can also predefine color palettes in the `updateCarColor()` function inside the script.

### Replace gallery images

Edit the `src` attributes inside the `.gallery-item img` tags in the `showcase` section.  
Use your own car renders or design sketches.

### Modify rim styles

Extend the `rimStyles` object in the JavaScript section:

```js
const rimStyles = {
  dark: { outer: "#1f2a3e", inner: "#2c354b", stroke: "#9aaebf" },
  // add your own:
  chrome: { outer: "#e0e5ec", inner: "#ffffff", stroke: "#4a5568" }
};
```

Then add a corresponding button in the `#rimStyleGroup` div.

### Update accent colors

Inside `applyAccent()`, add new color cases:

```js
else if(accentType === 'neonGreen') accentColor = "#4ade80";
```

---

##  Project Structure

```
velocity-forge/
│
├── index.html          # Main website (self-contained)
├── README.md           # You are here
└── assets/             (optional — you can add your own images)
    └── concept-*.jpg   # Replace placeholder images
```

>  *The entire project lives in a single HTML file — CSS, JS, and SVG are all embedded for simplicity.*

---

##  Key Code Snippets

### Live color update

```js
colorPicker.addEventListener('input', (e) => {
  bodyPath.setAttribute('fill', e.target.value);
});
```

### Rim style switcher

```js
function applyRimStyle(styleKey) {
  const style = rimStyles[styleKey];
  wheelRear.setAttribute('fill', style.outer);
  wheelFront.setAttribute('stroke', style.stroke);
  // ...
}
```

---

##  Browser Support

| Chrome | Firefox | Safari | Edge |
|--------|---------|--------|------|
|  yes   |  yes    |   yes  | yes  |

---

##  Future Improvements

- [ ] 3D model integration (Three.js)
- [ ] Save/Load configuration as JSON
- [ ] Realistic lighting & reflections on SVG
- [ ] Export design as image
- [ ] Backend form handler for design briefs

---

##  License

MIT — feel free to use, modify, and share for personal or commercial projects.  
Attribution is appreciated but not required.

---

##  Acknowledgments

- Icons by [Font Awesome](https://fontawesome.com)
- Fonts from [Google Fonts](https://fonts.google.com)
- Placeholder images from [Picsum](https://picsum.photos)

##  Contact

Om Gedam

GitHub: [https://github.com/itsomg134](https://github.com/itsomg134)

Email: [omgedam123098@gmail.com](mailto:omgedam123098@gmail.com)

Twitter (X): [https://twitter.com/omgedam](https://twitter.com/omgedam)

LinkedIn: [https://linkedin.com/in/omgedam](https://linkedin.com/in/omgedam)

Portfolio: [https://ogworks.lovable.app](https://ogworks.lovable.app)
