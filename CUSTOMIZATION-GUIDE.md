# Customization Guide - Crystal Clear Window Washing

This guide helps you customize and update your website easily.

## Quick Updates

### Change Phone Number

The phone number appears throughout the site. To update it globally:

1. Use Find & Replace (Ctrl+H or Cmd+H in most editors)
2. Find: `555-123-4567` or `+15551234567`
3. Replace with your actual phone number
4. Search in all `.html` files

**Locations:**
- Header CTA button
- Mobile menu
- Hero section
- Footer
- All service pages

### Change Email Address

1. Find: `info@crystalclearwashing.com`
2. Replace with: your actual email
3. Update in all HTML files

### Change Business Name

If you want to change "Crystal Clear Window Washing":

1. Find: `Crystal Clear Window Washing`
2. Replace with: Your Business Name
3. Update in all HTML files
4. Update in `sitemap.xml`
5. Update in Schema.org markup (in `<head>`)

### Update Business Address

1. Open `index.html`
2. Find the Schema.org JSON-LD section in `<head>`
3. Update the address object:

```json
"address": {
    "@type": "PostalAddress",
    "streetAddress": "Your Street Address",
    "addressLocality": "Your City",
    "addressRegion": "ON",
    "postalCode": "Your Postal Code",
    "addressCountry": "CA"
}
```

4. Update address in footer of all pages

### Update Service Areas

**Homepage:**
1. Open `index.html`
2. Scroll to "Service Area" section
3. Update the list of cities/areas

**Service Area Page:**
1. Open `pages/service-area.html`
2. Update the comprehensive list of service areas

## Color Customization

All colors are controlled by CSS variables in `css/styles.css`.

### Change Primary Color (Blue)

```css
:root {
    --color-primary: #1e6ba8;          /* Change this */
    --color-primary-light: #2b8ad6;    /* Lighter version */
    --color-primary-dark: #154a73;     /* Darker version */
}
```

### Change Accent Color (Yellow)

```css
:root {
    --color-accent: #ffc107;           /* Change this */
    --color-accent-dark: #e0a800;      /* Darker version */
}
```

### Recommended Color Combinations

**Professional Blue & Orange:**
```css
--color-primary: #2563eb;
--color-accent: #f97316;
```

**Green & Yellow:**
```css
--color-primary: #059669;
--color-accent: #fbbf24;
```

**Navy & Gold:**
```css
--color-primary: #1e3a8a;
--color-accent: #d97706;
```

## Typography Customization

### Change Font

Currently using "Public Sans" from Google Fonts.

**To change font:**

1. Go to [Google Fonts](https://fonts.google.com)
2. Choose your font
3. Copy the `<link>` code
4. Replace the font link in the `<head>` of all HTML files
5. Update CSS variable in `css/styles.css`:

```css
:root {
    --font-family-base: 'Your Font Name', sans-serif;
}
```

### Adjust Font Sizes

All font sizes use variables for easy adjustment:

```css
:root {
    --font-size-xs: 0.75rem;      /* 12px */
    --font-size-sm: 0.875rem;     /* 14px */
    --font-size-base: 1rem;       /* 16px */
    --font-size-lg: 1.125rem;     /* 18px */
    --font-size-xl: 1.25rem;      /* 20px */
    --font-size-2xl: 1.5rem;      /* 24px */
    --font-size-3xl: 1.875rem;    /* 30px */
    --font-size-4xl: 2.25rem;     /* 36px */
}
```

## Adding Content

### Add a New Service

1. **Create service page:**
   - Copy an existing service page (e.g., `pages/residential.html`)
   - Rename it (e.g., `pages/new-service.html`)
   - Update the content

2. **Add to homepage:**
   - Open `index.html`
   - Find the "Services" section
   - Add a new service card:

```html
<div class="service-card">
    <div class="service-icon">
        <span class="material-symbols-outlined">icon_name</span>
    </div>
    <h3 class="service-title">Your Service Name</h3>
    <p class="service-description">Service description here.</p>
    <a href="pages/your-service.html" class="service-link">
        Learn More
        <span class="material-symbols-outlined" style="font-size: 1rem;">arrow_forward</span>
    </a>
</div>
```

3. **Add to navigation** (if desired)

4. **Update sitemap.xml:**
   - Add your new page to the sitemap

### Add Testimonials

1. Open `index.html`
2. Find the "Testimonials" section
3. Copy an existing testimonial `<div>` block
4. Update the content:

```html
<div style="background: white; padding: var(--spacing-6); border-radius: var(--radius-xl); box-shadow: var(--shadow-md);">
    <!-- Star rating -->
    <div style="display: flex; gap: 0.5rem; margin-bottom: var(--spacing-4); color: var(--color-accent);">
        <span class="material-symbols-outlined" style="font-size: 1.5rem;">star</span>
        <!-- Repeat for 5 stars -->
    </div>

    <!-- Testimonial text -->
    <p style="font-size: var(--font-size-lg); color: var(--color-gray-700); line-height: 1.7; margin-bottom: var(--spacing-5); font-style: italic;">
        "Your testimonial text here..."
    </p>

    <!-- Customer info -->
    <div style="display: flex; align-items: center; gap: var(--spacing-3);">
        <div style="width: 50px; height: 50px; border-radius: 50%; background: linear-gradient(135deg, var(--color-primary) 0%, var(--color-primary-light) 100%); display: flex; align-items: center; justify-content: center; color: white; font-weight: 700; font-size: var(--font-size-xl);">
            AB
        </div>
        <div>
            <div style="font-weight: 600; color: var(--color-gray-900);">Customer Name</div>
            <div style="font-size: var(--font-size-sm); color: var(--color-gray-600);">City, ON</div>
        </div>
    </div>
</div>
```

### Add Blog/News Section

1. Create a `blog/` directory
2. Create `blog/index.html` for blog listing
3. Create individual blog post pages
4. Add "Blog" link to navigation
5. Update sitemap.xml

## Images

### Add Company Logo

1. Create a logo image (recommended: PNG with transparent background)
2. Save as `images/logo.png`
3. Update the header logo in all HTML files:

```html
<a href="index.html" class="logo">
    <img src="../images/logo.png" alt="Crystal Clear Window Washing" style="height: 40px;">
    <span class="logo-text">Crystal Clear</span>
</a>
```

### Add Favicon

1. Create a favicon (16x16, 32x32, 48x48 sizes)
2. Use [favicon.io](https://favicon.io) to generate from image or text
3. Save as `images/favicon.ico`
4. Update in `<head>` section (already linked)

### Add Service Photos

1. Optimize images for web:
   - Max width: 1920px for hero images
   - Compress using [TinyPNG](https://tinypng.com)
   - Save in `images/` folder

2. Update hero sections in service pages:

```html
<section style="background-image: url('../images/your-photo.jpg'); background-size: cover; background-position: center;">
    <!-- Hero content -->
</section>
```

### Add Before/After Photos

Create a gallery section:

```html
<section class="section">
    <div class="container">
        <h2>Our Work</h2>
        <div style="display: grid; grid-template-columns: repeat(auto-fit, minmax(300px, 1fr)); gap: var(--spacing-6);">

            <div style="border-radius: var(--radius-xl); overflow: hidden; box-shadow: var(--shadow-lg);">
                <img src="images/before-after-1.jpg" alt="Before and after window cleaning" style="width: 100%; height: auto;">
                <div style="padding: var(--spacing-4); background: white;">
                    <h3>Residential Home - Ancaster</h3>
                    <p>Complete exterior window cleaning</p>
                </div>
            </div>

            <!-- Repeat for more photos -->

        </div>
    </div>
</section>
```

## SEO Optimization

### Update Page Titles

Each page should have a unique, descriptive title:

```html
<title>Service Name - Crystal Clear Window Washing | Hamilton, ON</title>
```

**Title Formula:**
- Homepage: "Company Name | Main Service | Location"
- Service Pages: "Service Name - Company Name | Location"
- Keep under 60 characters

### Update Meta Descriptions

```html
<meta name="description" content="Your unique description here (150-160 characters)">
```

**Tips:**
- Include target keywords
- Include location (Hamilton, Ontario)
- Include call-to-action
- Keep 150-160 characters
- Make each page unique

### Add Alt Text to Images

Always add descriptive alt text:

```html
<img src="images/photo.jpg" alt="Professional window cleaner working on residential home in Hamilton">
```

### Update Schema.org Data

In `index.html` `<head>`, update the JSON-LD structured data:

```json
{
    "@context": "https://schema.org",
    "@type": "LocalBusiness",
    "name": "Your Business Name",
    "telephone": "Your Phone",
    "address": { /* Your address */ },
    "geo": {
        "latitude": 43.2557,    /* Your coordinates */
        "longitude": -79.8711
    }
}
```

Get coordinates: [latlong.net](https://www.latlong.net)

## Advanced Customization

### Add Contact Form

Replace placeholder contact section with a working form using:

**Option 1: Formspree** (easiest)
```html
<form action="https://formspree.io/f/YOUR_FORM_ID" method="POST">
    <input type="text" name="name" placeholder="Your Name" required>
    <input type="email" name="email" placeholder="Your Email" required>
    <textarea name="message" placeholder="Your Message" required></textarea>
    <button type="submit">Send Message</button>
</form>
```

**Option 2: Netlify Forms** (if using Netlify)
```html
<form name="contact" method="POST" data-netlify="true">
    <!-- Form fields -->
</form>
```

### Add Google Maps

Replace map placeholder in service area section:

```html
<iframe
    src="https://www.google.com/maps/embed?pb=YOUR_EMBED_CODE"
    width="100%"
    height="450"
    style="border:0; border-radius: var(--radius-xl);"
    allowfullscreen=""
    loading="lazy">
</iframe>
```

Get embed code from Google Maps → Share → Embed a map

### Add Reviews/Rating Widget

**Google Reviews:**
```html
<script src="https://static.elfsight.com/platform/platform.js"></script>
<div class="elfsight-app-YOUR_ID"></div>
```

Sign up at [elfsight.com](https://elfsight.com)

## Testing Your Changes

After making changes:

1. **Test locally** - Open `index.html` in browser
2. **Test all links** - Click every link to ensure they work
3. **Test mobile** - Use browser dev tools (F12 → Device Toolbar)
4. **Validate HTML** - [validator.w3.org](https://validator.w3.org)
5. **Check load speed** - [PageSpeed Insights](https://pagespeed.web.dev)

## Backup

Before making major changes:

1. **Duplicate the entire project folder**
2. **Or use Git for version control:**

```bash
git init
git add .
git commit -m "Initial commit"
```

This way you can always revert changes if needed.

## Need Help?

### Resources
- HTML Tutorial: [w3schools.com/html](https://www.w3schools.com/html)
- CSS Tutorial: [w3schools.com/css](https://www.w3schools.com/css)
- Material Symbols: [fonts.google.com/icons](https://fonts.google.com/icons)
- Color Picker: [coolors.co](https://coolors.co)

### Common Issues

**Problem: Changes not showing**
- Solution: Clear browser cache (Ctrl+F5 or Cmd+Shift+R)

**Problem: Layout broken**
- Solution: Check for unclosed HTML tags or CSS syntax errors

**Problem: Links not working**
- Solution: Check file paths (case-sensitive on some servers)

---

**Happy customizing!**

Your website is designed to be easily customizable while maintaining professional quality.
