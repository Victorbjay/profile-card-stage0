# 🎨 Testable Profile Card - HNG Stage 0

A modern, accessible, and fully responsive profile card component built with semantic HTML, CSS, and vanilla JavaScript. Features a stunning dark mode design with smooth animations and complete test coverage support.

![Profile Card Preview](https://img.shields.io/badge/Status-Complete-success?style=for-the-badge)
![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)

## 🚀 Live Demo

**[View Live Demo →](https://profilecard-autotest.netlify.app)** 

## ✨ Features

- ✅ **Fully Testable** - All elements include `data-testid` attributes for automated testing
- ✅ **Semantic HTML** - Proper use of `<article>`, `<figure>`, `<nav>`, `<section>` elements
- ✅ **Accessible** - ARIA labels, keyboard navigation, and visible focus states
- ✅ **Responsive Design** - Adapts beautifully from mobile (320px) to desktop (1920px+)
- ✅ **Dark Mode UI** - Modern glassmorphic design with gradient accents
- ✅ **Live Timestamp** - Real-time display of `Date.now()` in milliseconds
- ✅ **Avatar Upload** - Accept both URL images and file uploads
- ✅ **Smooth Animations** - Micro-interactions and hover effects throughout
- ✅ **Social Links** - Properly secured external links with `rel="noopener noreferrer"`

## 📋 Requirements Met

### Required Content (with data-testids)
- [x] Profile card root container — `data-testid="test-profile-card"`
- [x] Name — `data-testid="test-user-name"`
- [x] Biography — `data-testid="test-user-bio"`
- [x] Current time (milliseconds) — `data-testid="test-user-time"`
- [x] Avatar image — `data-testid="test-user-avatar"`
- [x] Social links list — `data-testid="test-user-social-links"`
- [x] Individual social links — `data-testid="test-user-social-<network>"`
- [x] Hobbies list — `data-testid="test-user-hobbies"`
- [x] Dislikes list — `data-testid="test-user-dislikes"`

### Technical Requirements
- [x] Semantic HTML tags throughout
- [x] Responsive layout (mobile/tablet/desktop)
- [x] Keyboard navigation support
- [x] Avatar accepts URL or file upload
- [x] Time updates using `Date.now()`
- [x] Social links open in new tab safely
- [x] Modern CSS (Flexbox & Grid)
- [x] Reduced motion support for accessibility

## 🛠️ Tech Stack

- **HTML5** - Semantic markup
- **CSS3** - Custom properties, Flexbox, Grid, animations
- **Vanilla JavaScript** - No frameworks or dependencies
- **FileReader API** - For avatar image uploads

## 📦 Installation & Setup

### Option 1: Direct Use
1. Download `index.html`
2. Open in any modern browser
3. That's it! No build process needed.

### Option 2: Local Development
```bash
# Clone the repository
git clone https://github.com/victorbjay/profile-card-stage0.git

# Navigate to project directory
cd profile-card-stage0

# Open with your preferred local server
# Using Python 3:
python -m http.server 8000

# Using Node.js (http-server):
npx http-server

# Using VS Code Live Server:
# Right-click index.html → "Open with Live Server"
```

Then visit `http://localhost:8000` in your browser.

## 🚢 Deployment

### Deploy to Netlify
1. Drag and drop `index.html` to [Netlify Drop](https://app.netlify.com/drop)
2. Or connect your GitHub repo for continuous deployment

### Deploy to GitHub Pages
```bash
# Push to GitHub
git add .
git commit -m "Initial commit"
git push origin main

# Enable GitHub Pages
# Go to Settings → Pages → Source: main branch
```
## 🧪 Testing

All elements are tagged with `data-testid` attributes for automated testing. Example test queries:

```javascript
// Using Testing Library
const card = screen.getByTestId('test-profile-card');
const name = screen.getByTestId('test-user-name');
const bio = screen.getByTestId('test-user-bio');
const time = screen.getByTestId('test-user-time');
const avatar = screen.getByTestId('test-user-avatar');
const socialLinks = screen.getByTestId('test-user-social-links');
const githubLink = screen.getByTestId('test-user-social-github');
const hobbies = screen.getByTestId('test-user-hobbies');
const dislikes = screen.getByTestId('test-user-dislikes');
```

### Verify Time Accuracy
```javascript
// Time should be within reasonable delta of Date.now()
const displayedTime = parseInt(screen.getByTestId('test-user-time').textContent);
const currentTime = Date.now();
expect(Math.abs(displayedTime - currentTime)).toBeLessThan(2000); // Within 2 seconds
```

## 🎨 Customization

### Change Colors
Edit the CSS custom properties in the `:root` selector if you want:
```css
:root {
    --primary: #6366f1;        /* Primary accent color */
    --secondary: #ec4899;      /* Secondary accent color */
    --bg-dark: #0f172a;        /* Background color */
    --bg-card: #1e293b;        /* Card background */
    /* ... etc */
}
```

### Change Avatar
- **URL**: Replace the `src` attribute in the `<img>` tag
- **Upload**: Click the camera button/icon or avatar image to upload your own

### Update Content
Simply edit the HTML content within the appropriate `data-testid` elements:
- Name: Edit text in `<h2 data-testid="test-user-name">`
- Bio: Edit text in `<p data-testid="test-user-bio">`
- Hobbies/Dislikes: Edit `<li>` items in respective lists

## 📱 Browser Support

- ✅ Chrome/Edge (latest)
- ✅ Firefox (latest)
- ✅ Safari (latest)
- ✅ Mobile browsers (iOS Safari, Chrome Mobile)

## ♿ Accessibility Features

- Semantic HTML structure
- ARIA labels for all interactive elements
- Keyboard navigation with visible focus states
- Alt text for images
- Reduced motion support for users with vestibular disorders
- High contrast color scheme
- Touch-friendly tap targets (48x48px minimum)

## 📄 License

MIT License - feel free to use this project for learning or personal use.

## 👨‍💻 Author

**Alex Rivera** (Sample Profile)
- GitHub: [@victorbjay](#)
- Twitter: [@victorbjay](#)
- LinkedIn: [/in/Emkajnr](#)

---

## 🎯 Stage 0 Task Completion

This project fully satisfies all requirements for the Frontend Wizards Stage 0 task:
- ✅ All required elements with correct data-testids
- ✅ Semantic HTML throughout
- ✅ Fully responsive design
- ✅ Avatar accepts URL or upload
- ✅ Live timestamp in milliseconds
- ✅ Accessible and keyboard-navigable
- ✅ Modern design with animations
- ✅ Ready for automated testing

**Submission Date:** October 19, 2025  
**Task Video:** [TikTok Explainer](https://vm.tiktok.com/ZMAXLFy8s/)

---

Made with 💜 for Frontend Wizards