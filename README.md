# DishwasherFix Landing Page Maintenance Guide

This guide provides detailed instructions for maintaining and customizing the DishwasherFix landing page. Whether you're new to web development or need a quick reference, you'll find step-by-step guidance for common maintenance tasks.

## Table of Contents
1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Linking Privacy and Terms Pages](#linking-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Header Section
```html
<header class="fixed w-full bg-white shadow-md z-50">
```
To update the company name:
1. Locate the `<span>` tag containing "DishwasherFix"
2. Replace the text while maintaining the classes:
```html
<span class="text-xl font-bold text-gray-800">Your Company Name</span>
```

### Hero Section
To modify the main headline:
1. Find the `<h1>` tag in the hero section
2. Update the text while preserving the classes:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 mb-6 leading-tight">
    Your New Headline Here
</h1>
```

### Tailwind CSS Class Guide
Common classes used in this landing page:
- `text-{size}`: Controls text size (xl, 2xl, 3xl, etc.)
- `font-{weight}`: Controls text weight (bold, semibold)
- `bg-{color}`: Sets background color
- `text-{color}`: Sets text color
- `p-{size}`: Sets padding
- `m-{size}`: Sets margin
- `rounded-{size}`: Controls border radius

Example of modifying a button:
```html
<!-- Original -->
<a href="#" class="bg-blue-600 text-white px-8 py-4 rounded-lg">

<!-- Modified (changing color and padding) -->
<a href="#" class="bg-green-600 text-white px-6 py-3 rounded-lg">
```

## Fixing Broken Links

### Navigation Menu Links
Current navigation links are:
```html
<a href="#features">Features</a>
<a href="#benefits">Benefits</a>
<a href="#faq">FAQ</a>
<a href="#contact">Contact</a>
```

To update a link:
1. Locate the `<a>` tag
2. Modify the `href` attribute:
   ```html
   <!-- Internal link to section -->
   <a href="#section-id">Section Name</a>
   
   <!-- External link -->
   <a href="https://example.com">External Link</a>
   ```

### CTA Button Links
The main CTA buttons currently point to:
```html
<a href="https://shrsl.com/4ub6p">
```

To update:
1. Locate the CTA buttons in the hero and CTA sections
2. Replace the `href` value with your new URL
3. Ensure the URL includes the full path (including https://)

## Linking Privacy and Terms Pages

### Footer Legal Links
Current placeholder links:
```html
<div>
    <h3 class="text-xl font-semibold mb-4">Legal</h3>
    <ul class="space-y-2">
        <li><a href="#" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="#" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

To add proper links:
1. Create your privacy.html and terms.html pages
2. Update the href attributes:
```html
<li><a href="privacy.html" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
```

## Troubleshooting

### Common Issues

1. **Broken Layout**
   - Check that you haven't removed any essential Tailwind classes
   - Verify all opening tags have corresponding closing tags
   - Ensure the Tailwind CDN link is working:
   ```html
   <script src="https://cdn.tailwindcss.com"></script>
   ```

2. **Non-Working Links**
   - Verify file paths are correct
   - Check for typos in URLs
   - Ensure internal links match section IDs exactly

3. **Missing Icons**
   - Confirm Font Awesome is properly linked:
   ```html
   <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css">
   ```
   - Verify icon class names are correct (e.g., `fas fa-tools`)

### Need Help?
If you encounter issues:
1. Check the browser's developer tools (F12) for errors
2. Verify all external resources are loading
3. Test the page across different browsers
4. Ensure all changes maintain mobile responsiveness

Remember to always backup your files before making changes, and test thoroughly after each modification.