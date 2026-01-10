# Deployment Guide - Crystal Clear Window Washing Website

This guide walks you through deploying your website to production.

## Pre-Deployment Checklist

Before deploying, make sure you've completed these tasks:

- [ ] Updated all contact information (phone, email, address)
- [ ] Replaced placeholder content with actual business details
- [ ] Added real images (logo, favicon, service photos)
- [ ] Updated Schema.org structured data with accurate information
- [ ] Tested all links and navigation
- [ ] Verified mobile responsiveness
- [ ] Checked all forms (if implemented)
- [ ] Updated domain name in sitemap.xml
- [ ] Updated domain name in robots.txt
- [ ] Configured SSL certificate (HTTPS)
- [ ] Set up Google Analytics (optional)
- [ ] Created Google Business Profile (for local SEO)

## Deployment Options

### Option 1: Netlify (Recommended for Beginners)

**Why Netlify?**
- Free hosting for static sites
- Automatic SSL certificate
- Global CDN for fast loading
- Easy drag-and-drop deployment
- Custom domain support

**Steps:**

1. **Create a Netlify Account**
   - Go to [netlify.com](https://www.netlify.com)
   - Sign up with email, GitHub, or GitLab

2. **Deploy Your Site**
   - Click "Add new site" → "Deploy manually"
   - Drag your entire project folder into the deployment zone
   - Wait 30 seconds - your site is now live!

3. **Configure Custom Domain**
   - Go to Site Settings → Domain Management
   - Click "Add custom domain"
   - Enter your domain name (e.g., crystalclearwashing.com)
   - Follow DNS configuration instructions from your domain registrar

4. **Enable HTTPS**
   - Automatic! Netlify provides free SSL certificates via Let's Encrypt
   - HTTPS will be enabled within a few minutes

5. **Configure Redirects** (Optional)
   - Create a `_redirects` file in your root directory:
     ```
     # Redirect www to non-www
     https://www.crystalclearwashing.com/* https://crystalclearwashing.com/:splat 301!
     ```

### Option 2: Vercel

**Steps:**

1. Go to [vercel.com](https://vercel.com)
2. Sign up and click "Add New Project"
3. Import your project (drag folder or connect GitHub)
4. Click "Deploy"
5. Add custom domain in project settings

### Option 3: GitHub Pages (Free)

**Steps:**

1. Create a GitHub account at [github.com](https://github.com)
2. Create a new repository named `your-username.github.io`
3. Upload your files to the repository
4. Go to Settings → Pages
5. Select branch (usually `main`) and save
6. Your site will be live at `https://your-username.github.io`

**Custom Domain:**
- Add a `CNAME` file with your domain name
- Configure DNS with your domain registrar

### Option 4: Traditional Web Hosting

**Popular Hosting Providers:**
- Bluehost
- SiteGround
- HostGator
- GoDaddy
- DreamHost

**Steps:**

1. **Purchase Hosting Plan**
   - Choose a shared hosting plan ($3-10/month)
   - Most include free SSL certificate

2. **Upload Files via FTP**
   - Use FileZilla, Cyberduck, or hosting control panel
   - Upload all files to `public_html` or `www` directory

3. **Configure Domain**
   - Point domain nameservers to hosting provider
   - Or update DNS A record to hosting IP address

4. **Enable SSL**
   - Most hosts offer free SSL via Let's Encrypt
   - Enable in hosting control panel (cPanel, Plesk, etc.)

5. **Activate .htaccess**
   - The `.htaccess` file is already included
   - Uncomment HTTPS redirect after SSL is configured

## Post-Deployment Tasks

### 1. Test Your Live Site

- [ ] Visit your domain and verify it loads correctly
- [ ] Test all pages and navigation
- [ ] Verify HTTPS is working (green padlock in browser)
- [ ] Test mobile responsiveness on actual devices
- [ ] Check page load speed at [PageSpeed Insights](https://pagespeed.web.dev/)
- [ ] Test all phone/email links
- [ ] Verify smooth scrolling and mobile menu

### 2. Set Up Google Search Console

1. Go to [search.google.com/search-console](https://search.google.com/search-console)
2. Add your property (domain or URL prefix)
3. Verify ownership (DNS record or HTML file upload)
4. Submit your sitemap: `https://yoursite.com/sitemap.xml`
5. Request indexing for key pages

### 3. Set Up Google Analytics (Optional)

1. Go to [analytics.google.com](https://analytics.google.com)
2. Create an account and property
3. Get your tracking code
4. Add to `<head>` section of all HTML files:

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

### 4. Set Up Google Business Profile

1. Go to [google.com/business](https://www.google.com/business)
2. Create or claim your business listing
3. Add accurate NAP (Name, Address, Phone)
4. Upload photos of your work
5. Select appropriate business categories
6. Add service areas
7. Verify your business (postcard, phone, email)

### 5. Submit to Local Directories

Submit your business to these directories for local SEO:

- [ ] Google Business Profile
- [ ] Bing Places for Business
- [ ] Yelp
- [ ] Yellow Pages
- [ ] HomeAdvisor
- [ ] Angie's List
- [ ] Better Business Bureau
- [ ] Local Hamilton business directories

### 6. Set Up Social Media

- [ ] Create Facebook Business Page
- [ ] Create Instagram Business Profile
- [ ] Update social media links in website footer
- [ ] Add website link to all social profiles

### 7. Monitor Performance

**Tools to Monitor:**
- Google Analytics - Traffic and user behavior
- Google Search Console - Search performance and indexing
- PageSpeed Insights - Site speed
- GTmetrix - Performance analysis
- Uptime Robot - Monitor site availability

## Domain & DNS Configuration

### Domain Registrars
- Namecheap
- Google Domains
- GoDaddy
- Cloudflare Registrar

### DNS Settings for Netlify

If using Netlify with custom domain:

```
A Record:  @  →  75.2.60.5
CNAME:  www  →  your-site-name.netlify.app
```

### DNS Settings for Traditional Hosting

```
A Record:  @  →  [Your hosting IP address]
CNAME:  www  →  yourdomain.com
```

## SSL Certificate Setup

### Automatic SSL (Netlify, Vercel)
- Automatically provided - no configuration needed

### Let's Encrypt (cPanel)
1. Log into cPanel
2. Go to "SSL/TLS Status"
3. Select your domain
4. Click "Run AutoSSL"

### After SSL is Enabled

Uncomment HTTPS redirect in `.htaccess`:

```apache
RewriteEngine On
RewriteCond %{HTTPS} off
RewriteRule ^(.*)$ https://%{HTTP_HOST}%{REQUEST_URI} [L,R=301]
```

## Troubleshooting

### Site Not Loading
- Check DNS propagation: [whatsmydns.net](https://www.whatsmydns.net)
- DNS can take 24-48 hours to propagate globally
- Clear browser cache and try incognito mode

### 404 Errors
- Verify all files uploaded to correct directory
- Check file names and paths are case-sensitive
- Ensure `index.html` is in root directory

### CSS/JS Not Loading
- Check file paths are correct (relative vs absolute)
- Verify files uploaded to `css/` and `js/` folders
- Check browser console for errors (F12)

### Images Not Displaying
- Verify images uploaded to `images/` folder
- Check file names match exactly (case-sensitive)
- Use relative paths: `images/logo.jpg` not `/images/logo.jpg`

### HTTPS Mixed Content Errors
- Ensure all resources (images, CSS, JS) use HTTPS
- Update external links to use HTTPS
- Check browser console for specific warnings

## Maintenance Schedule

### Weekly
- Check for broken links
- Monitor uptime
- Review analytics

### Monthly
- Update content if needed
- Add new testimonials
- Check and respond to contact form submissions
- Review and optimize SEO

### Quarterly
- Audit website performance
- Update service offerings
- Refresh images if needed
- Review and update pricing

### Yearly
- Renew domain and hosting
- Update copyright year in footer
- Major content refresh
- Technical SEO audit

## Performance Optimization Tips

1. **Optimize Images**
   - Use WebP format with JPEG/PNG fallbacks
   - Compress images (TinyPNG, ImageOptim)
   - Use responsive images with `srcset`

2. **Minimize HTTP Requests**
   - Combine CSS files if adding more
   - Use CSS sprites for icons (or stick with Material Symbols)

3. **Enable Caching**
   - `.htaccess` already configured for caching
   - Verify working with browser dev tools

4. **Use CDN**
   - Netlify/Vercel automatically use CDN
   - For traditional hosting, consider Cloudflare

## Support

### Need Help?
- Netlify Support: [docs.netlify.com](https://docs.netlify.com)
- Vercel Support: [vercel.com/support](https://vercel.com/support)
- Web Hosting Support: Contact your hosting provider

### Website Issues
- Check browser console for errors (F12 → Console tab)
- Validate HTML: [validator.w3.org](https://validator.w3.org)
- Test responsiveness: [responsivedesignchecker.com](https://responsivedesignchecker.com)

---

**Good luck with your deployment!**

Your Crystal Clear Window Washing website is ready to make a great first impression online.
