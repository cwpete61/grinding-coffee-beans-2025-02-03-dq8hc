# CoffeeMax Landing Page - Maintenance Guide

This guide will help you maintain and customize the CoffeeMax landing page. Whether you're new to web development or need a quick reference, follow these detailed instructions.

## Table of Contents
1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Linking Privacy and Terms Pages](#linking-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Header Section
The header contains the logo and navigation menu:
```html
<div class="text-2xl font-bold text-gray-800">CoffeeMax</div>
```
To change the logo text:
1. Locate this div in the header section
2. Replace "CoffeeMax" with your desired text
3. Adjust size using `text-2xl` (options: `text-xl`, `text-3xl`, etc.)

### Hero Section
The main headline and subtitle are in the hero section:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 leading-tight mb-6">
    Create Great Coffee at Home
</h1>
<p class="text-xl md:text-2xl text-gray-600 mb-10 leading-relaxed">
    Master the art of grinding coffee beans for the perfect brew every time.
</p>
```
To modify:
1. Replace the text between the `<h1>` tags for the main headline
2. Update the paragraph text between the `<p>` tags
3. Keep the responsive classes (`md:text-5xl`, `lg:text-6xl`) to maintain mobile-friendly design

### Understanding Tailwind Classes
Common classes used in this page:
- `text-{size}`: Controls text size (xl, 2xl, 3xl, etc.)
- `font-{weight}`: Controls text weight (bold, semibold, etc.)
- `bg-{color}`: Sets background color
- `p-{size}`: Sets padding (4, 6, 8, etc.)
- `mb-{size}`: Sets margin bottom
- `md:`: Applies styles only on medium screens and up

## Fixing Broken Links

### Navigation Menu Links
Current navigation links:
```html
<div class="hidden md:flex space-x-8">
    <a href="#features">Features</a>
    <a href="#benefits">Benefits</a>
    <a href="#faq">FAQ</a>
    <a href="#contact">Contact</a>
</div>
```
To update:
1. Locate the `href` attribute in each `<a>` tag
2. For internal links (same page sections), use `#section-name`
3. For external links, use full URL: `https://example.com`

### CTA Button Links
Update the call-to-action buttons:
```html
<a href="https://coffeemax.com" class="inline-block bg-blue-600 text-white...">
    Start Brewing Better Coffee
</a>
```
Replace `https://coffeemax.com` with your desired URL.

### Social Media Links
In the footer section:
```html
<div class="flex space-x-4">
    <a href="#"><i class="fab fa-twitter"></i></a>
    <a href="#"><i class="fab fa-facebook"></i></a>
    <a href="#"><i class="fab fa-instagram"></i></a>
</div>
```
Replace the `#` with your social media profile URLs.

## Linking Privacy and Terms Pages

### Adding Privacy and Terms Links
Add these links to the footer's "Links" section:
```html
<ul class="space-y-2">
    <li><a href="#" class="hover:text-white transition-colors duration-300">About</a></li>
    <li><a href="#" class="hover:text-white transition-colors duration-300">Blog</a></li>
    <li><a href="privacy.html" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
    <li><a href="terms.html" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
</ul>
```

### Creating Policy Pages
1. Create two new files: `privacy.html` and `terms.html`
2. Use the same header and footer as `index.html`
3. Maintain consistent styling by copying Tailwind CSS classes

## Troubleshooting

### Common Issues
1. **Broken Internal Links**
   - Ensure section IDs match href attributes
   - Check for typos in IDs
   - IDs are case-sensitive

2. **Responsive Design Issues**
   - Keep all `md:` and `lg:` prefixed classes
   - Test on different screen sizes
   - Don't remove the viewport meta tag

3. **Icon Display Problems**
   - Verify Font Awesome CDN link is present
   - Check icon class names against Font Awesome documentation
   - Ensure internet connectivity for CDN access

### Need Help?
- Check the [Tailwind CSS documentation](https://tailwindcss.com/docs)
- Validate HTML at [W3C Validator](https://validator.w3.org/)
- Test responsiveness using browser developer tools

Remember to always test changes across different devices and browsers before deploying to production.