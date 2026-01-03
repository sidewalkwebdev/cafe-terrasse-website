# Cafe Terrasse - Deployment Checklist

## ✅ COMPLETED ITEMS

### HTML Structure
- ✅ All 6 HTML pages created (index, menu, about, order, privacy, terms)
- ✅ Bootstrap 5.3.3 integrated
- ✅ Responsive navigation with mobile menu
- ✅ Footer with legal page links on all pages
- ✅ Semantic HTML5 markup

### Accessibility
- ✅ `aria-label="Toggle navigation"` added to all navbar toggles
- ✅ `title="Google Maps location of Cafe Terrasse"` added to all iframes
- ✅ Proper heading hierarchy (h1, h2, h3, etc.)
- ✅ Alt text on Bootstrap icons (bi class handles this)

### CSS & Styling
- ✅ Custom CSS with CSS variables
- ✅ Safari compatibility: `-webkit-backdrop-filter` prefix added
- ✅ Responsive design for mobile, tablet, desktop
- ✅ Smooth scroll behavior
- ✅ Fixed navbar and mobile order button

### Security
- ✅ `rel="noopener"` added to all external links (ordering platforms)
- ✅ Removed unsupported `referrerpolicy` attribute from iframes

### SEO Foundation
- ✅ `robots.txt` created with proper directives
- ✅ `sitemap.xml` created with all 6 pages
- ✅ Meta descriptions on all pages
- ✅ Canonical URLs on all pages
- ✅ Open Graph tags for social sharing
- ✅ Twitter Card tags
- ✅ Geo-location meta tags for local SEO
- ✅ Keywords meta tags
- ✅ Legal pages set to `noindex, follow`

### Legal & Compliance
- ✅ Privacy Policy page with comprehensive sections
- ✅ Terms of Service page with 13 detailed sections
- ✅ Footer links to legal pages on all main pages

---

## ⚠️ REQUIRED BEFORE DEPLOYMENT

### 1. Domain Configuration (CRITICAL)
**Files to update:**
- [ ] `robots.txt` - Replace `yourdomain.com` with your actual domain
- [ ] `sitemap.xml` - Replace all 6 instances of `yourdomain.com` with actual domain
- [ ] `index.html` - Update all Open Graph and Twitter meta tag URLs
- [ ] `menu.html` - Update canonical and social meta tag URLs
- [ ] `about.html` - Update canonical and social meta tag URLs
- [ ] `order.html` - Update canonical and social meta tag URLs
- [ ] `privacy.html` - Update canonical URL
- [ ] `terms.html` - Update canonical URL

**Search & Replace:** `yourdomain.com` → `your-actual-domain.com`

### 2. Images & Media (CRITICAL)
- [ ] Create and add `favicon.ico` to root directory
- [ ] Add `<link rel="icon" type="image/x-icon" href="/favicon.ico">` to all pages
- [ ] Create Open Graph images for social sharing:
  - `images/cafe-og-image.jpg` (1200x630px) for homepage
  - `images/cafe-menu-og.jpg` (1200x630px) for menu page
  - `images/cafe-about-og.jpg` (1200x630px) for about page
  - `images/cafe-order-og.jpg` (1200x630px) for order page
- [ ] Replace Bootstrap icon placeholders with actual food/drink images if desired
- [ ] Update Unsplash image URL in about.html with your own cafe photo

### 3. External Links & URLs
**Currently using placeholders - must update:**
- [ ] `order.html` - Update Order Direct URL (`https://order.online/store/cafe-terrasse-12345`)
- [ ] `order.html` - Update DoorDash URL (`https://www.doordash.com/store/cafe-terrasse`)
- [ ] `order.html` - Update Postmates URL (`https://postmates.com/store/cafe-terrasse`)
- [ ] All pages - Add actual social media links in footer (currently just `#` placeholders)

### 4. Google Maps
- [ ] Verify Google Maps embed URLs are correct for your location
- [ ] Consider adding Google Maps API key for advanced features (optional)

### 5. Contact Information
- [ ] Update business hours if different from "9:00 AM - 11:00 PM daily"
- [ ] Update address if different from "123 N. Western Ave, Los Angeles, CA 90004"
- [ ] Add phone number to footer/contact section
- [ ] Add email address for inquiries

---

## 🔍 RECOMMENDED IMPROVEMENTS

### Analytics & Tracking
- [ ] Add Google Analytics 4 (GA4) tracking code
- [ ] Add Google Tag Manager (GTM) container
- [ ] Set up Google Search Console and submit sitemap
- [ ] Set up Bing Webmaster Tools
- [ ] Add Facebook Pixel (optional, for ads)

### Performance Optimization
- [ ] Compress and optimize all images (use WebP format)
- [ ] Consider using a CDN for Bootstrap and Google Fonts
- [ ] Add lazy loading to images: `loading="lazy"`
- [ ] Minify CSS and consider critical CSS
- [ ] Add `preconnect` hints for external resources:
  ```html
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  ```

### Schema.org Structured Data
Add JSON-LD structured data for better SEO:
- [ ] Restaurant schema on homepage
- [ ] Menu schema on menu page
- [ ] LocalBusiness schema with hours, location, ratings
- [ ] BreadcrumbList schema for navigation

Example:
```html
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "Restaurant",
  "name": "Cafe Terrasse",
  "address": {
    "@type": "PostalAddress",
    "streetAddress": "123 N. Western Ave",
    "addressLocality": "Los Angeles",
    "addressRegion": "CA",
    "postalCode": "90004"
  },
  "servesCuisine": "Coffee, Cafe, Korean",
  "priceRange": "$$",
  "telephone": "+1-XXX-XXX-XXXX"
}
</script>
```

### Additional SEO
- [ ] Create custom 404 error page
- [ ] Create `humans.txt` file
- [ ] Add `manifest.json` for PWA support (optional)
- [ ] Create Apple Touch icons for iOS bookmarking
- [ ] Add breadcrumb navigation on interior pages

### User Experience
- [ ] Add loading states/animations
- [ ] Add form validation if you add contact forms
- [ ] Consider adding a newsletter signup
- [ ] Add "Back to Top" button on long pages
- [ ] Test all forms and interactive elements

### Security Headers
Add via server configuration or meta tags:
- [ ] Content Security Policy (CSP)
- [ ] X-Frame-Options
- [ ] X-Content-Type-Options
- [ ] Referrer-Policy

### Accessibility Enhancements
- [ ] Run WAVE accessibility checker
- [ ] Test with screen readers (NVDA, JAWS, VoiceOver)
- [ ] Verify keyboard navigation works everywhere
- [ ] Check color contrast ratios (WCAG AA minimum)
- [ ] Add skip navigation link

---

## 🧪 PRE-LAUNCH TESTING

### Cross-Browser Testing
- [ ] Chrome (latest)
- [ ] Firefox (latest)
- [ ] Safari (latest)
- [ ] Edge (latest)
- [ ] Mobile Safari (iOS)
- [ ] Chrome Mobile (Android)

### Device Testing
- [ ] Desktop (1920x1080, 1366x768)
- [ ] Tablet (iPad, iPad Pro)
- [ ] Mobile (iPhone 12/13/14, Samsung Galaxy)
- [ ] Small mobile (iPhone SE)

### Functionality Testing
- [ ] All navigation links work
- [ ] All external links open in new tabs
- [ ] Mobile menu toggle works
- [ ] Smooth scroll to menu sections works
- [ ] Google Maps loads correctly
- [ ] Order platform links work
- [ ] Footer links work (privacy, terms)
- [ ] Forms submit correctly (if any)

### SEO/Performance Testing Tools
- [ ] Google PageSpeed Insights
- [ ] GTmetrix
- [ ] Lighthouse audit (Chrome DevTools)
- [ ] Mobile-Friendly Test (Google)
- [ ] Rich Results Test (Google)
- [ ] Structured Data Testing Tool

### Validation
- [ ] W3C HTML Validator
- [ ] W3C CSS Validator
- [ ] Check for broken links (dead link checker)
- [ ] Spell check all content

---

## 📋 DEPLOYMENT STEPS

1. **Domain & Hosting Setup**
   - [ ] Register domain name
   - [ ] Set up web hosting (recommend: Netlify, Vercel, AWS, or traditional hosting)
   - [ ] Configure DNS records
   - [ ] Set up SSL certificate (Let's Encrypt or via hosting provider)

2. **Final Code Updates**
   - [ ] Complete all items in "REQUIRED BEFORE DEPLOYMENT" section
   - [ ] Run final validation checks
   - [ ] Test all links one more time

3. **Upload Files**
   - [ ] Upload all HTML files
   - [ ] Upload CSS files
   - [ ] Upload images folder
   - [ ] Upload robots.txt
   - [ ] Upload sitemap.xml
   - [ ] Upload favicon.ico

4. **Post-Deployment**
   - [ ] Submit sitemap to Google Search Console
   - [ ] Submit sitemap to Bing Webmaster Tools
   - [ ] Test live site on multiple devices
   - [ ] Set up Google My Business listing
   - [ ] Create social media profiles (if not done)
   - [ ] Set up monitoring (uptime, analytics)

5. **Marketing & Launch**
   - [ ] Announce on social media
   - [ ] Update Google My Business with website URL
   - [ ] Add website to email signatures
   - [ ] Create QR code for in-store promotion
   - [ ] Consider Google Ads or social media ads

---

## 📝 NOTES

### Current Placeholders
- Domain: `yourdomain.com` (appears in 16+ locations)
- Social links: `#` in footer
- Review links: Yelp and Google Reviews URLs are generic
- Order platform URLs: Need specific restaurant IDs
- OG Images: Need to be created
- Favicon: Missing

### File Structure is Ready
```
/
├── index.html
├── menu.html
├── about.html
├── order.html
├── privacy.html
├── terms.html
├── styles.css
├── robots.txt
├── sitemap.xml
├── favicon.ico (TO BE ADDED)
└── images/ (TO BE ADDED)
    ├── cafe-og-image.jpg
    ├── cafe-menu-og.jpg
    ├── cafe-about-og.jpg
    └── cafe-order-og.jpg
```

### Technical Stack
- **Framework:** Bootstrap 5.3.3
- **Icons:** Bootstrap Icons
- **Fonts:** Google Fonts (DM Serif Display, Montserrat)
- **Maps:** Google Maps Embed
- **No Build Process:** Pure HTML/CSS (no Node.js/npm required)

---

## 🎯 PRIORITY LEVELS

**HIGH PRIORITY (Must do before launch):**
1. Replace all `yourdomain.com` with actual domain
2. Add favicon
3. Update ordering platform URLs
4. Create and add Open Graph images
5. Test on mobile devices

**MEDIUM PRIORITY (Should do before launch):**
1. Add Google Analytics
2. Set up Google Search Console
3. Add phone number and email
4. Update social media links
5. Run performance tests

**LOW PRIORITY (Can do after launch):**
1. Add Schema.org structured data
2. Create custom 404 page
3. Add newsletter signup
4. Implement PWA features
5. Advanced performance optimization

---

**Last Updated:** January 2, 2026
**Status:** Ready for domain configuration and final testing
