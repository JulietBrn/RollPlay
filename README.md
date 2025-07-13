# 🎮 RollPlay

**RollPlay** is a responsive landing page designed for selling online games. It includes multiple sections such as product info, policy pages, and contact forms. The project uses Webpack for asset bundling and optimization, but without any code minification as per client requirements.

## 🌐 Live Demo

[🌐 View Live Demo](https://julietbrn.github.io/RollPlay/public/)

## 📁 Project Structure

```
ROLLPLAY/
│
├── public/                # Final production build
│   ├── _.html             # HTML pages
│   ├── assets/            # Images and media
│   ├── script.js          # Compiled JavaScript
│   ├── style.css          # Stylesheet
│   └── New_v9_RollPlay.zip# Auto-generated ZIP archive
│
├── src/                   # Source files
│   ├── assets/            # Original images and media
│   ├── ext_files/         # External PHP files (e.g., form handling)
│   │   └── thanks_form.php
│   ├── js/                # JavaScript modules
│   │   ├── burger.js
│   │   ├── faq.js
│   │   └── ... etc.
│   ├── scss/              # SCSS files (optional)
│   ├── _.html             # HTML page templates
│
├── webpack.config.js      # Webpack configuration
└── package.json           # Project dependencies and scripts
```

## 🚀 Features

- Multiple HTML pages with Webpack-powered generation
- Image optimization (JPEG, PNG, SVG)
- Static asset copying
- ZIP packaging of the final build
- Prettier formatting with lint-staged

> ❗ **Note:** Minification of HTML, SCSS, and JavaScript is intentionally disabled based on the client's request.

## 📦 Installation & Development

```bash
# Install dependencies
npm install

# Build project for production
npm run build

```

You can open index.html directly with a Live Server extension (e.g., in VS Code) for testing.

## 🧠 Code Example

A simple "Show More" button logic from show-more.js:

```javascript
// show-more.js
const showWraps = document.querySelectorAll(".show-wrap");

if (showWraps.length) {
  showWraps.forEach((wrap) => {
    const showMoreBtn = wrap.querySelector(".show-more-btn");
    if (showMoreBtn) {
      showMoreBtn.addEventListener("click", function () {
        wrap.classList.add("show");
        showMoreBtn.classList.add("hide");
      });
    }
  });
}
```

## 🛠️ Technologies Used

- **Webpack** – Module bundler for managing assets and dependencies
- **Sass** – SCSS support (optional, for advanced styling)
- **ImageMinimizerPlugin** – Image compression and optimization
- **HtmlWebpackPlugin** – HTML template generation and handling
- **CopyWebpackPlugin** – Static asset copying to the build folder
- **ZipWebpackPlugin** – Automatic packaging of the final build into a ZIP archive
- **Prettier + lint-staged** – Automated code formatting and linting
