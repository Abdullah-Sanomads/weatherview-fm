# Weather Application

[![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)](https://developer.mozilla.org/en-US/docs/Web/HTML)
[![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)](https://developer.mozilla.org/en-US/docs/Web/CSS)
[![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)](https://developer.mozilla.org/en-US/docs/Web/JavaScript)
[![Open-Meteo](https://img.shields.io/badge/Open--Meteo-API-blue?style=for-the-badge)](https://open-meteo.com/)

## Overview

A comprehensive, responsive weather application built with vanilla HTML, CSS, and JavaScript. Features real-time weather data, location search, favorites system, and delightful animations powered by the Open-Meteo API.

### Links

- 🔗 **Live Site:** [View Demo](#)
- 💻 **Solution:** [Frontend Mentor Solution](https://www.frontendmentor.io/solutions/)
- 📦 **Repository:** [GitHub Repo](https://github.com/Abdullah-Sanomads/weatherview-fm.git)

## ✨ Features

### Core Functionality
- 🔍 **Location Search** - Search weather by city/location name
- 🌡️ **Current Weather** - Real-time temperature and conditions
- 📊 **Weather Metrics** - Feels like, humidity, wind speed, precipitation
- 📅 **7-Day Forecast** - Daily high/low temperatures with icons
- ⏰ **Hourly Forecast** - 24-hour detailed forecast with day selector
- 🔄 **Unit Toggle** - Switch between Imperial/Metric units
- 📱 **Responsive Design** - Optimized for mobile, tablet, and desktop

### Enhanced Features
- 📍 **Geolocation Support** - Automatic current location detection
- ⭐ **Favorites System** - Save frequently checked locations
- 🌓 **Dark/Light Mode** - Automatic theme switching based on time
- 🌈 **Weather Animations** - Dynamic backgrounds and particles
- 📈 **Additional Data** - UV index, visibility, air pressure, sunrise/sunset
- ♿ **Accessibility** - Full keyboard navigation and screen reader support
- ⚡ **Performance** - Debounced search and optimized animations

## 🖼️ Screenshots

| Desktop view | Mobile view |
| ------- | ------ |
| ![Desktop](https://github.com/Ayokanmi-Adejola/Weather-App/blob/main/design/desktop-design-imperial.jpg?raw=true) | ![Mobile](https://github.com/Ayokanmi-Adejola/Weather-App/blob/main/design/mobile-design-imperial.jpg?raw=true) |

## 🛠️ Built With

- **Semantic HTML5** markup with accessibility features
- **CSS3** custom properties and animations
- **Vanilla JavaScript** (ES6+) for all functionality
- **Open-Meteo API** for weather data (no API key required)
- **CSS Grid & Flexbox** for responsive layouts
- **Local Storage** for user preferences and favorites
- Mobile-first responsive design workflow

## 🚀 Getting Started

### Prerequisites

- Modern web browser (Chrome 90+, Firefox 88+, Safari 14+, Edge 90+)
- Internet connection for weather data
- HTTPS for geolocation features (in production)

### Installation

1. Clone the repository
```bash
git clone https://github.com/Ayokanmi-Adejola/Weather-App
```

2. Navigate to the project directory
```bash
cd Weather-App
```

3. Open `index.html` in your browser or use a local development server
```bash
# Using Python
python -m http.server 8000

# Using Node.js (http-server)
npx http-server
```

4. Allow location access for automatic weather detection (optional)

## 📖 How to Use

1. **Search Location** - Enter any city or location in the search bar
2. **Use Geolocation** - Click the location button for automatic detection
3. **Toggle Units** - Switch between Celsius/Fahrenheit and km/h or mph
4. **Save Favorites** - Click the star icon to save frequently checked locations
5. **View Forecasts** - Scroll to see 7-day and hourly forecasts
6. **Switch Themes** - Theme automatically adjusts based on time of day

## 📂 Project Structure

```
weather-app-main/
├── index.html          # Main HTML file with semantic structure
├── styles.css          # Complete CSS with design system
├── script.js           # JavaScript functionality and API logic
├── assets/
│   └── images/         # Weather icons and UI assets
├── design/             # Design mockups and previews
├── style-guide.md      # Design specifications
└── README.md           # This file
```

## 💡 What I Learned

This project helped me develop skills in:

- Working with third-party weather APIs and handling async data
- Creating responsive layouts with CSS Grid and Flexbox
- Building accessible web applications with ARIA labels
- Implementing local storage for persistent user preferences
- Creating performant animations using CSS transforms
- Managing application state in vanilla JavaScript
- Debouncing search inputs for better UX
- Building a favorites system with CRUD operations

### Code Highlights

**API Integration:**
```javascript
// Efficient weather data fetching with error handling
async function getWeatherData(latitude, longitude) {
  const url = `https://api.open-meteo.com/v1/forecast?latitude=${latitude}&longitude=${longitude}&current=temperature_2m,weathercode...`;
  const response = await fetch(url);
  return await response.json();
}
```

**Responsive Design:**
```css
/* Mobile-first approach with CSS Grid */
.forecast-container {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(150px, 1fr));
  gap: var(--spacing-4);
}
```

## 🎨 Design System

### Color Palette
- **Neutral Shades:** 9 levels from `hsl(243, 96%, 9%)` to `hsl(0, 0%, 100%)`
- **Accent Blue:** `hsl(233, 67%, 56%)`
- **Accent Orange:** `hsl(28, 100%, 52%)`
- **Dynamic Themes:** Weather-based background colors

### Typography
- **Primary:** DM Sans (300, 500, 600, 700)
- **Display:** Bricolage Grotesque (700)
- **Base Size:** 18px with responsive scaling

## 🔧 Customization

### Adding Weather Icons
1. Add icon files to `assets/images/`
2. Update `WEATHER_CODES` object in `script.js`
3. Map weather codes to new icons

### Modifying Themes
1. Update CSS custom properties in `:root` and `[data-theme]`
2. Add theme variants in theme management system

### Extending API Data
1. Modify API parameters in `getWeatherData` function
2. Update display functions for new data
3. Add corresponding HTML elements and CSS styles

## ♿ Accessibility Features

- Full keyboard navigation support
- Screen reader compatible with ARIA labels
- High contrast mode support
- Respects prefers-reduced-motion
- Skip links for quick navigation
- Focus indicators for all interactive elements

## 🐛 Known Issues & Limitations

- Weather particles may impact performance on older devices
- Some weather data may not be available for all locations
- Geolocation requires HTTPS in production environments
- API rate limits may apply for excessive usage

## 🚀 Future Enhancements

- [ ] Weather alerts and notifications
- [ ] Historical weather data visualization
- [ ] Interactive weather maps
- [ ] Social sharing capabilities
- [ ] Offline support with service workers
- [ ] Weather widgets for embedding
- [ ] Multi-language support
- [ ] Weather-based recommendations

## 📚 Useful Resources

- [Open-Meteo API Documentation](https://open-meteo.com/en/docs) - Weather API reference
- [MDN Web Docs](https://developer.mozilla.org/) - Web development documentation
- [CSS Tricks](https://css-tricks.com/) - CSS tips and techniques
- [Frontend Mentor](https://www.frontendmentor.io) - Design challenges

## 👨‍💻 Author

**Ahmed Abdullah**

- GitHub: [@abdullah-sanomads](https://github.com/Abdullah-Sanomads)
- Frontend Mentor: [@Abdullah-Sanomads](https://www.frontendmentor.io/profile/Abdullah-Sanomads)

## 🙏 Acknowledgments

- Challenge provided by [Frontend Mentor](https://www.frontendmentor.io)
- Weather data powered by [Open-Meteo](https://open-meteo.com/)
- Typography from [Google Fonts](https://fonts.google.com/)
- Community feedback and support during development

## 📄 License

This project is open source and available under the [MIT License](LICENSE).

---

⭐ **Enjoyed this project?** Give it a star and feel free to fork it for your own experiments!

**Happy coding!** 🌤️