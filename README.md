# Crystal Clear Window Washing Website

A professional, modern, and SEO-optimized website for Crystal Clear Window Washing, a window cleaning service based in Hamilton, Ontario.

## Features

- **Responsive Design**: Mobile-first approach ensuring perfect display on all devices
- **SEO Optimized**: Structured data (Schema.org), semantic HTML, optimized meta tags
- **Modern Tech Stack**: HTML5, CSS3, Vanilla JavaScript
- **Fast Loading**: Minimal dependencies, optimized assets
- **Accessible**: ARIA labels, semantic markup, keyboard navigation
- **Professional Design**: Clean blue and yellow color scheme with modern UI components

## Project Structure

```
WindowWashingVSC/
├── index.html                  # Homepage
├── css/
│   └── styles.css             # Custom styles and design system
├── js/
│   └── main.js                # Interactive functionality
├── images/                     # Image assets (logos, photos)
│   └── .gitkeep
├── pages/                      # Service and info pages
│   ├── residential.html       # Residential window cleaning
│   ├── commercial.html        # Commercial window cleaning
│   ├── high-rise.html         # High-rise window cleaning
│   ├── screen-services.html   # Screen cleaning & repair
│   ├── gutter-cleaning.html   # Gutter cleaning service
│   ├── pressure-washing.html  # Pressure washing service
│   ├── about.html             # About the company
│   ├── contact.html           # Contact page
│   └── service-area.html      # Service area map
├── .gitignore
└── README.md                   # This file
```

## Getting Started

### Prerequisites
- A modern web browser (Chrome, Firefox, Safari, Edge)
- A text editor (VS Code recommended)
- Optional: Local web server for testing (Live Server, Python SimpleHTTPServer, etc.)

### Installation

1. Clone or download this repository
2. Open `index.html` in your browser, or
3. Use a local development server:

```bash
# Using Python 3
python -m http.server 8000

# Using Python 2
python -m SimpleHTTPServer 8000

# Using Node.js http-server
npx http-server

# Using VS Code Live Server extension
# Right-click index.html -> "Open with Live Server"
```

4. Navigate to `http://localhost:8000` (or the port shown)

## Customization

### Update Business Information

1. **Contact Details**: Update phone numbers, email, and address throughout the site
   - Search for `555-123-4567` and replace with actual phone
   - Search for `info@crystalclearwashing.com` and replace with actual email
   - Update address in footer and Schema.org markup

2. **Schema.org Data** (in `<head>` of index.html):
   - Update business name, address, phone, coordinates
   - Update opening hours
   - Update social media URLs

3. **Service Areas**: Edit the location list in the service area section

### Design System

The website uses CSS custom properties (variables) for easy theming:

```css
:root {
    --color-primary: #1e6ba8;      /* Professional blue */
    --color-accent: #ffc107;        /* Bright yellow */
    --font-family-base: 'Public Sans', sans-serif;
    /* ... more variables in css/styles.css */
}
```

Edit these in [css/styles.css](css/styles.css) to change colors, fonts, spacing, etc.

### Add Images

1. Add your company logo to `images/logo.jpg` or `images/logo.png`
2. Create and add `images/favicon.ico` (16x16, 32x32, 48x48 sizes)
3. Add service photos to enhance visual appeal
4. Update image paths in HTML files

### Add Google Analytics

Add your Google Analytics tracking code before the closing `</head>` tag:

```html
<!-- Google Analytics -->
<script async src="https://www.googletagmanager.com/gtag/js?id=GA_MEASUREMENT_ID"></script>
<script>
  window.dataLayer = window.dataLayer || [];
  function gtag(){dataLayer.push(arguments);}
  gtag('js', new Date());
  gtag('config', 'GA_MEASUREMENT_ID');
</script>
```

## Features & Functionality

### Current Features
- ✅ Sticky navigation header
- ✅ Mobile hamburger menu
- ✅ Smooth scrolling to sections
- ✅ Active navigation highlighting on scroll
- ✅ Hover effects and animations
- ✅ Form validation (ready for contact forms)
- ✅ Phone link click tracking
- ✅ Responsive grid layouts
- ✅ SEO-optimized structure

### Optional Enhancements
- Add contact form with backend (PHP, Node.js, or form service)
- Integrate Google Maps for service area visualization
- Add image gallery/lightbox for before/after photos
- Implement testimonial slider/carousel
- Add blog section for content marketing
- Integrate online booking system
- Add live chat widget

## SEO Optimization

### On-Page SEO
- ✅ Semantic HTML5 structure
- ✅ Descriptive meta titles and descriptions
- ✅ Keyword-optimized headings (H1, H2, H3)
- ✅ Alt text ready for images
- ✅ Schema.org LocalBusiness markup
- ✅ Mobile-friendly responsive design
- ✅ Fast loading (minimal dependencies)

### Local SEO
- ✅ NAP (Name, Address, Phone) consistency
- ✅ Location-specific keywords (Hamilton, Ontario)
- ✅ Service area defined in Schema.org
- ✅ Local business structured data

### Next Steps for SEO
- [ ] Submit to Google Search Console
- [ ] Create and submit XML sitemap
- [ ] Set up Google Business Profile
- [ ] Build local citations (Yelp, Yellow Pages, etc.)
- [ ] Implement SSL certificate (HTTPS)
- [ ] Create robots.txt file
- [ ] Add Open Graph and Twitter Card meta tags

## Browser Compatibility

- Chrome (latest)
- Firefox (latest)
- Safari (latest)
- Edge (latest)
- Mobile browsers (iOS Safari, Chrome Mobile)

## Performance

- Minimal external dependencies (Tailwind CSS CDN, Google Fonts)
- Optimized CSS with CSS variables
- Vanilla JavaScript (no heavy frameworks)
- Lazy loading ready for images

## Accessibility

- Semantic HTML elements
- ARIA labels on interactive elements
- Keyboard navigation support
- Sufficient color contrast
- Responsive text sizing

## Deployment

### Option 1: Traditional Web Hosting
1. Choose a hosting provider (Bluehost, SiteGround, HostGator, etc.)
2. Upload files via FTP/SFTP or file manager
3. Configure domain and SSL certificate
4. Test all functionality

### Option 2: Modern Static Hosting (Free)
- **Netlify**: Drag & drop deployment, automatic SSL
- **Vercel**: GitHub integration, edge network
- **GitHub Pages**: Free hosting for static sites
- **Cloudflare Pages**: Fast CDN, free SSL

### Deploy to Netlify (Recommended)
1. Create account at [netlify.com](https://netlify.com)
2. Drag the project folder to Netlify dashboard
3. Your site is live with HTTPS in seconds!
4. Connect custom domain in settings

## License

This website template is created for Crystal Clear Window Washing. Modify as needed for your business.

## Support & Maintenance

### Regular Updates
- Update content as services change
- Add new testimonials regularly
- Keep contact information current
- Add blog posts for SEO (optional)

### Technical Maintenance
- Monitor website uptime
- Check for broken links
- Test forms and interactive features
- Update dependencies if using CDNs
- Backup files regularly

## Contact

For questions about this website:
- Email: info@crystalclearwashing.com
- Phone: (555) 123-4567

---

**Built with care for Crystal Clear Window Washing**
Last Updated: January 2026
