# Ephemeral Equilibrium - Nature Website

A stunning, interactive nature and sustainability-themed website featuring advanced animations, smooth scrolling, and immersive visual effects.

![Website Preview](https://img.shields.io/badge/Status-Active-success)
![HTML5](https://img.shields.io/badge/HTML5-E34F26?logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?logo=javascript&logoColor=black)

## 🌿 Overview

This project showcases a modern, animated website promoting environmental sustainability and the harmony between nature and humanity. It features smooth scrolling, interactive image effects, and carefully crafted animations to create an immersive user experience.

## ✨ Features

- **Smooth Scrolling**: Locomotive Scroll for buttery-smooth page navigation
- **Interactive Animations**: GSAP-powered entrance and scroll animations
- **Advanced Image Effects**: Shery.js distortion and hover effects on images
- **Responsive Design**: Optimized for various screen sizes
- **Video Integration**: Interactive video elements with hover effects
- **Modern UI**: Clean, minimalist design with focus on nature imagery

## 🎨 Sections

1. **Hero Section** - "Ephemeral Equilibrium" headline with animated cards
2. **Sustainability Card** - Highlighting eco-friendly commitment
3. **Gallery Preview** - Call-to-action for visual exploration
4. **Our Motive** - Mission statement with interactive capsule elements
5. **Synergy & Harmony** - Dual image showcase with distortion effects
6. **Biodegradable Packaging** - Product focus section
7. **Future Vision** - Video background with call-to-action button

## 🛠️ Technologies Used

### Core Technologies
- **HTML5** - Semantic markup
- **CSS3** - Custom styling (external stylesheet)
- **JavaScript (ES6+)** - Interactive functionality

### Libraries & Frameworks

| Library | Version | Purpose |
|---------|---------|---------|
| [GSAP](https://greensock.com/gsap/) | 3.13.0 | Core animation engine |
| [ScrollTrigger](https://greensock.com/scrolltrigger/) | 3.12.2 | Scroll-based animations |
| [Locomotive Scroll](https://locomotivemtl.github.io/locomotive-scroll/) | 3.5.4 | Smooth scrolling |
| [Shery.js](https://sheryjs.com/) | Latest | Image effects & distortions |
| [Three.js](https://threejs.org/) | 0.155.0 | 3D effects support |
| [Remix Icon](https://remixicon.com/) | 4.5.0 | Icon system |
| [ControlKit](https://github.com/automat/controlkit.js) | Latest | Debug panel for effects |

## 📁 Project Structure

```
project-root/
│
├── index.html              # Main HTML file
├── style.css               # Custom styles
├── script.js               # JavaScript animations
│
└── assets/
    ├── images/
    │   ├── pinkgreenplant.jpg
    │   ├── pinkplant.jpg
    │   ├── sea.jpg
    │   ├── cloud.jpg
    │   ├── bottle.jpg
    │   └── nigggaaaa.jpeg
    │
    └── videos/
        └── fort.mp4
```

## 🚀 Getting Started

### Prerequisites
- Modern web browser (Chrome, Firefox, Safari, Edge)
- Local server (optional, but recommended for best performance)

### Installation

1. **Clone or download the repository**
   ```bash
   git clone <your-repo-url>
   cd nature-website
   ```

2. **Ensure all assets are in place**
   - Place images in `/assets/images/`
   - Place video in `/assets/videos/`

3. **Run the project**
   
   **Option A: Using VS Code Live Server**
   - Install "Live Server" extension
   - Right-click `index.html` → "Open with Live Server"
   
   **Option B: Using Python**
   ```bash
   # Python 3
   python -m http.server 8000
   ```
   
   **Option C: Using Node.js**
   ```bash
   npx serve
   ```

4. **Open in browser**
   ```
   http://localhost:8000
   ```

## 🎭 Animation Details

### Navigation Animation
```javascript
gsap.from(".navLink", {
  y: 15,
  opacity: 0,
  duration: 1,
  stagger: 0.2,
  ease: "power3.out"
});
```
- Links slide down and fade in sequentially

### Text Effects
```javascript
Shery.textAnimate("#heading h1", {
  style: 2,
  y: 10,
  delay: 0.3,
  duration: 1.5
});
```
- Animated text with style 2 (wave/distortion effect)

### Image Effects

**Style 3** - Gooey distortion (`.imgntext img`)
- Interactive displacement on hover
- Liquid-like morphing effect

**Style 5** - Static distortion (`#sus_Image img`)
- Subtle warping without mouse interaction

**Style 2** - Wave distortion (Synergy & Harmony images)
- Different modes (-8 and 7) for variety
- Mouse-responsive ripple effects

**Style 6** - Noise distortion (`#pckgImg`)
- Continuous animated texture
- Gooey morphing effect

### Video Interaction
```javascript
// Video fades in on button hover
document.querySelector("#textnBtn button")
  .addEventListener("mouseover", () => {
    gsap.to("#future video", {
      opacity: 1,
      duration: 1
    });
});
```

## 🎨 Customization

### Changing Colors
Edit `style.css` to modify the color scheme:
```css
:root {
  --primary-color: #your-color;
  --secondary-color: #your-color;
  --text-color: #your-color;
}
```

### Adjusting Animation Speed
In `script.js`, modify duration values:
```javascript
duration: 1,  // Change this value (in seconds)
```

### Modifying Image Effects
Each Shery.js effect has a `config` object with customizable parameters:
```javascript
config: {
  noiseDetail: { value: 9.92, range: [0, 100] },
  distortionAmount: { value: 1.15, range: [0, 10] },
  // Adjust these values
}
```

## 📱 Responsive Design

The website is designed to work across different screen sizes. Key breakpoints:
- **Desktop**: 1200px+
- **Tablet**: 768px - 1199px
- **Mobile**: 320px - 767px

## ⚡ Performance Tips

1. **Optimize Images**
   - Compress images using tools like TinyPNG
   - Convert to WebP format for better compression
   - Recommended max size: 500KB per image

2. **Lazy Loading**
   - Add `loading="lazy"` to images
   - Defer non-critical JavaScript

3. **Reduce Animation Complexity**
   - Lower `quality` values in Shery.js configs
   - Disable debug mode in production

## 🐛 Troubleshooting

### Images Not Loading
- Check file paths in HTML
- Ensure images are in `/assets/images/`
- Verify correct file extensions

### Animations Not Working
- Check browser console for errors
- Ensure all CDN libraries are loading
- Verify JavaScript file is linked correctly

### Locomotive Scroll Issues
- Make sure `#main` wrapper exists
- Check for CSS conflicts with `overflow` properties
- Ensure content height is sufficient

## 🌐 Browser Support

| Browser | Version | Support |
|---------|---------|---------|
| Chrome | 90+ | ✅ Full |
| Firefox | 88+ | ✅ Full |
| Safari | 14+ | ✅ Full |
| Edge | 90+ | ✅ Full |
| Opera | 76+ | ✅ Full |

## 📄 License

This project is open source and available under the [MIT License](LICENSE).

## 👥 Contributing

Contributions are welcome! Please follow these steps:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📧 Contact

For questions or feedback, please reach out:

- **GitHub**: [@yourusername](https://github.com/yourusername)
- **Email**: your.email@example.com

## 🙏 Acknowledgments

- [GSAP](https://greensock.com/) - For powerful animation capabilities
- [Shery.js](https://sheryjs.com/) - For stunning image effects
- [Locomotive Scroll](https://locomotivemtl.github.io/locomotive-scroll/) - For smooth scrolling
- [Remix Icon](https://remixicon.com/) - For beautiful icons

---

**Built with 🌱 for a sustainable future**

Last Updated: October 25, 2025