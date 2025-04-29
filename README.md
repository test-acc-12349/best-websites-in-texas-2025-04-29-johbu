# Texas Web Landing Page - Maintenance Guide

This guide will help you maintain and customize the Texas Web landing page. It's designed for beginners with no prior coding experience.

## Table of Contents
- [Updating Text and Styling](#updating-text-and-styling)
- [Managing Links](#managing-links)
- [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
- [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains the main navigation and logo. To modify:

1. Change the logo text:
```html
<!-- Find this line in the header section -->
<a href="/" class="text-2xl font-bold text-blue-600">Texas Web</a>
```
Simply replace "Texas Web" with your desired text.

### Hero Section
The hero section is your main banner area. To update:

1. Modify the main heading:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 mb-6">
    Best Websites In Texas
</h1>
```
Replace "Best Websites In Texas" with your headline.

2. Update the subheading:
```html
<p class="text-xl md:text-2xl text-gray-600 mb-12">
    Custom Websites For Your Business
</p>
```

### Understanding Tailwind Classes
Common classes used in this template:

- Text sizes: `text-xl`, `text-2xl`, etc.
- Colors: `text-blue-600`, `bg-white`, etc.
- Spacing: `px-6` (padding left/right), `py-4` (padding top/bottom)
- Responsive prefixes: `md:` (medium screens), `lg:` (large screens)

Example of modifying a button's color:
```html
<!-- Original blue button -->
<a href="#" class="bg-blue-600 hover:bg-blue-700">

<!-- Changed to green -->
<a href="#" class="bg-green-600 hover:bg-green-700">
```

## Managing Links

### Navigation Menu Links
Current navigation links are:

```html
<div class="hidden md:flex space-x-8">
    <a href="#features">Features</a>
    <a href="#benefits">Benefits</a>
    <a href="#faq">FAQ</a>
    <a href="#contact">Contact</a>
</div>
```

To update a link:
1. Locate the `<a>` tag
2. Modify the `href` attribute
3. Update the text between the tags

Example:
```html
<!-- Change this -->
<a href="#features" class="text-gray-600 hover:text-blue-600">Features</a>

<!-- To this -->
<a href="#services" class="text-gray-600 hover:text-blue-600">Services</a>
```

### Call-to-Action Links
The page contains several CTA buttons linking to "https://sigmaseo.io". To update:

1. Find all instances:
```html
<a href="https://sigmaseo.io" class="inline-block px-8 py-4 bg-blue-600">
```

2. Replace with your desired URL:
```html
<a href="https://your-domain.com" class="inline-block px-8 py-4 bg-blue-600">
```

## Adding Privacy and Terms Pages

### Footer Link Updates
The footer contains placeholder links for Privacy Policy and Terms of Service:

```html
<div>
    <h4 class="text-lg font-semibold mb-4">Legal</h4>
    <ul class="space-y-2">
        <li><a href="#" class="text-gray-400 hover:text-white">Privacy Policy</a></li>
        <li><a href="#" class="text-gray-400 hover:text-white">Terms of Service</a></li>
    </ul>
</div>
```

To link to your policy pages:

1. Create your policy pages (privacy.html and terms.html)
2. Update the href attributes:
```html
<li><a href="privacy.html" class="text-gray-400 hover:text-white">Privacy Policy</a></li>
<li><a href="terms.html" class="text-gray-400 hover:text-white">Terms of Service</a></li>
```

## Troubleshooting

Common issues and solutions:

1. **Links not working:**
   - Ensure file names match exactly (case-sensitive)
   - Verify files are in the correct directory
   - Check for typos in href attributes

2. **Styles not applying:**
   - Confirm Tailwind CSS CDN link is present in head section
   - Check for typos in class names
   - Ensure responsive classes use correct prefixes (md:, lg:)

3. **Animations not working:**
   - Verify AOS script is loaded at bottom of page
   - Check data-aos attributes are spelled correctly
   - Ensure AOS initialization script is present

For additional help:
- Review Tailwind CSS documentation
- Check browser console for errors
- Validate HTML at [W3C Validator](https://validator.w3.org/)

Remember to always test changes across different devices and browsers to ensure consistency.