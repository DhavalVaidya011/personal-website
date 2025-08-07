# Personal Website

A modern, responsive personal website built with HTML, CSS, and JavaScript. Features a beautiful design with smooth animations, mobile-friendly navigation, and interactive elements.

## Features

- 🎨 **Modern Design**: Clean and professional layout with beautiful gradients and animations
- 📱 **Responsive**: Fully responsive design that works on all devices
- ⚡ **Fast Loading**: Optimized for performance with smooth animations
- 🎯 **Interactive**: Smooth scrolling, form validation, and dynamic content
- 🔧 **Customizable**: Easy to customize with your own content and styling

## Sections

1. **Hero Section**: Eye-catching introduction with animated title and call-to-action buttons
2. **About**: Personal information with animated statistics
3. **Skills**: Technical skills organized by category with icons
4. **Projects**: Portfolio showcase with project cards
5. **Contact**: Contact form with validation and social media links

## Getting Started

### Prerequisites

- A modern web browser
- Basic knowledge of HTML, CSS, and JavaScript (for customization)

### Installation

1. Download or clone the files to your local machine
2. Open `index.html` in your web browser
3. The website should load immediately with all features working

### Customization

#### Personal Information

Edit the following sections in `index.html`:

1. **Name and Title**:
   ```html
   <title>Your Name - Personal Website</title>
   <h1 class="hero-title">Hi, I'm <span class="highlight">Your Name</span></h1>
   <p class="hero-subtitle">Full Stack Developer & Creative Problem Solver</p>
   ```

2. **About Section**:
   ```html
   <p>I'm a passionate developer with a love for creating meaningful digital experiences...</p>
   ```

3. **Contact Information**:
   ```html
   <span>your.email@example.com</span>
   <span>+1 (555) 123-4567</span>
   <span>Your City, Country</span>
   ```

4. **Social Media Links**:
   ```html
   <a href="#" class="social-link"><i class="fab fa-github"></i></a>
   <a href="#" class="social-link"><i class="fab fa-linkedin"></i></a>
   ```

#### Skills

Update the skills section by modifying the skill items:

```html
<div class="skill-item">
    <i class="fab fa-html5"></i>
    <span>HTML5</span>
</div>
```

Available Font Awesome icons for skills:
- `fab fa-html5` - HTML5
- `fab fa-css3-alt` - CSS3
- `fab fa-js` - JavaScript
- `fab fa-react` - React
- `fab fa-node-js` - Node.js
- `fab fa-python` - Python
- `fab fa-git-alt` - Git
- `fab fa-docker` - Docker
- `fab fa-aws` - AWS

#### Projects

Add or modify project cards:

```html
<div class="project-card">
    <div class="project-image">
        <div class="image-placeholder">
            <i class="fas fa-laptop-code"></i>
        </div>
    </div>
    <div class="project-content">
        <h3>Project Name</h3>
        <p>Project description...</p>
        <div class="project-tech">
            <span>Technology 1</span>
            <span>Technology 2</span>
        </div>
        <div class="project-links">
            <a href="#" class="project-link"><i class="fab fa-github"></i> Code</a>
            <a href="#" class="project-link"><i class="fas fa-external-link-alt"></i> Live</a>
        </div>
    </div>
</div>
```

#### Colors and Styling

The website uses a modern color scheme. You can customize colors in `styles.css`:

```css
/* Primary colors */
--primary-color: #2563eb;
--secondary-color: #7c3aed;
--accent-color: #fbbf24;

/* Background gradients */
background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
```

#### Statistics

Update the statistics in the About section:

```html
<div class="stat">
    <h3>3+</h3>
    <p>Years Experience</p>
</div>
```

## File Structure

```
personal-website/
├── index.html          # Main HTML file
├── styles.css          # CSS styles and animations
├── script.js           # JavaScript functionality
└── README.md           # This file
```

## Features Explained

### Navigation
- Fixed navigation bar with smooth scrolling
- Mobile hamburger menu
- Active section highlighting

### Animations
- Typing animation for hero title
- Scroll-triggered animations for sections
- Hover effects on cards and buttons
- Parallax scrolling effect

### Form Handling
- Contact form with validation
- Success/error notifications
- Email format validation

### Responsive Design
- Mobile-first approach
- Flexible grid layouts
- Optimized for all screen sizes

## Browser Support

- Chrome (recommended)
- Firefox
- Safari
- Edge
- Internet Explorer 11+

## Performance Tips

1. **Optimize Images**: Replace placeholder icons with optimized images
2. **Minify Files**: Minify CSS and JavaScript for production
3. **CDN Usage**: The website uses CDN for Font Awesome and Google Fonts
4. **Lazy Loading**: Consider implementing lazy loading for images

## Deployment

### GitHub Pages
1. Create a GitHub repository
2. Upload your website files
3. Go to Settings > Pages
4. Select source branch and save

### Netlify
1. Drag and drop your website folder to Netlify
2. Your site will be live instantly
3. Customize domain if needed

### Vercel
1. Connect your GitHub repository
2. Deploy automatically
3. Get a custom domain

## Customization Examples

### Adding a Blog Section
```html
<section id="blog" class="blog">
    <div class="container">
        <h2 class="section-title">Blog</h2>
        <div class="blog-grid">
            <article class="blog-card">
                <h3>Blog Post Title</h3>
                <p>Blog post excerpt...</p>
                <a href="#" class="read-more">Read More</a>
            </article>
        </div>
    </div>
</section>
```

### Adding a Resume Download
```html
<div class="hero-buttons">
    <a href="#projects" class="btn btn-primary">View My Work</a>
    <a href="resume.pdf" class="btn btn-secondary" download>Download Resume</a>
</div>
```

## Troubleshooting

### Common Issues

1. **Font Awesome Icons Not Loading**: Check internet connection, the icons are loaded from CDN
2. **Animations Not Working**: Ensure JavaScript is enabled in your browser
3. **Mobile Menu Not Working**: Check if the hamburger menu JavaScript is properly loaded

### Performance Issues

1. **Slow Loading**: Optimize images and consider using a CDN
2. **Animations Lagging**: Reduce animation complexity on mobile devices
3. **Large File Size**: Minify CSS and JavaScript files

## Contributing

Feel free to fork this project and customize it for your needs. If you make improvements, consider sharing them with the community.

## License

This project is open source and available under the [MIT License](LICENSE).

## Support

If you need help customizing your website or encounter any issues, feel free to:

1. Check the troubleshooting section above
2. Review the code comments for guidance
3. Search for similar issues online
4. Contact the developer for assistance

## Updates and Maintenance

- Keep your content fresh and up-to-date
- Regularly update your projects and skills
- Monitor website performance
- Test on different devices and browsers
- Backup your files regularly

---

**Happy coding! 🚀** 