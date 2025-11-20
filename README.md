# 🍕 Forkify - Recipe Search & Management App

[![Live Demo](https://img.shields.io/badge/demo-live-brightgreen.svg)](https://your-demo-link.com)
[![License](https://img.shields.io/badge/license-MIT-blue.svg)](LICENSE)
[![JavaScript](https://img.shields.io/badge/JavaScript-ES6+-yellow.svg)](https://www.ecma-international.org/ecma-262/)
[![Parcel](https://img.shields.io/badge/Bundler-Parcel-orange.svg)](https://parceljs.org/)

A modern, feature-rich recipe application that allows users to search over 1,000,000 recipes, view detailed cooking instructions, bookmark favorites, and upload their own recipes.

![Forkify App Screenshot](src/img/logo.png)

## ✨ Features

- 🔍 **Smart Recipe Search** - Search through over 1 million recipes from various sources
- 📖 **Detailed Recipe View** - View ingredients, cooking time, servings, and step-by-step instructions
- 📊 **Dynamic Servings Adjustment** - Automatically recalculate ingredient quantities based on servings
- 🔖 **Bookmark System** - Save your favorite recipes with persistent local storage
- ➕ **Custom Recipe Upload** - Add your own recipes to the collection (requires API key)
- 📱 **Responsive Design** - Beautiful UI that works on all devices
- ⚡ **Fast Performance** - Optimized bundling with Parcel 2
- 🎯 **Pagination** - Navigate through search results easily

## 🛠️ Tech Stack

### Core Technologies

![JavaScript](https://img.shields.io/badge/JavaScript-ES6+-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)
![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)
![SASS](https://img.shields.io/badge/Sass-CC6699?style=for-the-badge&logo=sass&logoColor=white)
![MVC](https://img.shields.io/badge/Architecture-MVC-blue?style=for-the-badge)

- **JavaScript (ES6+)** - Modern JavaScript with async/await, modules, classes
- **HTML5** - Semantic markup
- **SASS/SCSS** - Advanced CSS with variables, mixins, and nesting
- **MVC Architecture** - Clean separation of concerns

### Build Tools & Libraries

![Parcel](https://img.shields.io/badge/Parcel-2.12.0-21374B?style=for-the-badge&logo=parcel)
![NPM](https://img.shields.io/badge/NPM-CB3837?style=for-the-badge&logo=npm&logoColor=white)
![Git](https://img.shields.io/badge/Git-F05032?style=for-the-badge&logo=git&logoColor=white)

- **Parcel 2.12.0** - Zero-config module bundler
- **Fraction.js 4.3.7** - Display recipe quantities as fractions (1/2, 3/4, etc.)
- **Core-js 3.39.0** - Polyfills for modern JavaScript features
- **Regenerator Runtime** - Async/await support

### API

![API](https://img.shields.io/badge/API-Forkify_v2-orange?style=for-the-badge&logo=fastapi&logoColor=white)

- **Forkify API v2** - Recipe data from multiple sources

## 🚀 Getting Started

### Prerequisites

- Node.js (v14 or higher)
- npm or yarn

### Installation

1. **Clone the repository**

   ```bash
   git clone https://github.com/theboylexis/forkify-app-2025.git
   cd forkify-app-2025
   ```

2. **Install dependencies**

   ```bash
   npm install
   ```

3. **Start development server**

   ```bash
   npm run dev
   ```

4. **Open in browser**
   ```
   http://localhost:1234
   ```

### Build for Production

```bash
npm run build
```

The production-ready files will be in the `dist/` folder.

## 📝 Usage

### Searching for Recipes

1. Enter an ingredient or recipe name in the search bar
2. Browse through paginated results
3. Click on any recipe to view details

### Viewing Recipe Details

- See cooking time and servings
- View all ingredients with precise measurements
- Adjust servings using +/- buttons (ingredients auto-update)
- Click "Directions" to view the full recipe on the source website

### Bookmarking Recipes

- Click the bookmark icon on any recipe
- Access bookmarks from the dropdown menu
- Bookmarks persist across browser sessions

### Uploading Your Own Recipe

1. Get a free API key from [Forkify API](https://forkify-api.jonas.io/v2)
2. Add your key to `src/js/config.js`:
   ```javascript
   export const KEY = 'your-api-key-here';
   ```
3. Click "Add Recipe" button
4. Fill in recipe details and submit

## 📂 Project Structure

```
forkify/
├── src/
│   ├── img/                  # Images and icons
│   ├── js/
│   │   ├── views/           # View components (MVC pattern)
│   │   │   ├── View.js
│   │   │   ├── recipeView.js
│   │   │   ├── searchView.js
│   │   │   ├── resultsView.js
│   │   │   ├── paginationView.js
│   │   │   ├── bookmarksView.js
│   │   │   └── addRecipeView.js
│   │   ├── model.js         # Application state and business logic
│   │   ├── controller.js    # Controllers connecting model and views
│   │   ├── config.js        # Configuration constants
│   │   └── helpers.js       # Utility functions
│   └── sass/                # SCSS stylesheets
│       ├── _base.scss
│       ├── _components.scss
│       ├── _header.scss
│       ├── _recipe.scss
│       └── main.scss
├── index.html               # HTML template
├── package.json            # Dependencies and scripts
└── .parcelrc              # Parcel configuration
```

## 🎯 Key Features Implementation

### MVC Architecture

- **Model** (`model.js`) - Manages application state, API calls, and data transformations
- **Views** (`views/`) - Responsible for rendering UI and handling user events
- **Controller** (`controller.js`) - Connects models and views, handles application logic

### API Integration

- Async/await for clean asynchronous code
- Error handling with try/catch
- Request timeout protection (30 seconds)
- Smart API key management

### State Management

- Centralized state object
- LocalStorage for bookmark persistence
- URL hash for recipe navigation

## 🌟 Updates from Original (2024 → 2025)

This version includes several improvements:

✅ **Updated Dependencies**

- Parcel 2.0.0-beta → 2.12.0 (stable)
- Sass 1.26.10 → 1.80.0
- Core-js 3.6.5 → 3.39.0
- Replaced deprecated `fractional` with `fraction.js 4.3.7`

✅ **Fixed Issues**

- Resolved Fraction library import/export issues
- Fixed API key validation for public recipe searches
- Increased timeout from 10s to 30s for better reliability
- Added Parcel configuration for optimized builds

✅ **Enhanced UX**

- Made logo clickable to return home
- Added ES6 module support
- Improved error handling

## 📱 Browser Support

- Chrome (latest)
- Firefox (latest)
- Safari (latest)
- Edge (latest)

## 🤝 Contributing

Contributions are welcome! Feel free to:

- Report bugs
- Suggest new features
- Submit pull requests

## 📄 License

This project is licensed under the MIT License.

## 👨‍💻 Author

**Alex Marfo** - [@theboylexis](https://github.com/theboylexis)

## 🙏 Acknowledgments

- Original concept from [Jonas Schmedtmann's JavaScript Course](https://www.udemy.com/course/the-complete-javascript-course/)
- Recipe data provided by [Forkify API](https://forkify-api.jonas.io/)
- Icons and design inspiration

## 📞 Support

For support, please open an issue in the GitHub repository.

---

⭐ If you found this project helpful, please give it a star!
