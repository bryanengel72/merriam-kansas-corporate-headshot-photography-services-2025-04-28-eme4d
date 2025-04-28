# 101Headshots Landing Page Maintenance Guide

This guide will help you maintain and customize the 101Headshots landing page. Whether you're new to web development or need a quick reference, follow these detailed instructions for common updates.

## Table of Contents
1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Linking Privacy and Terms Pages](#linking-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Main Sections Overview
The landing page is divided into these key sections:
- Header (Navigation)
- Hero Section
- Services Section
- Benefits Section
- FAQ Section
- Contact Section
- Footer

### Updating Text Content

#### Hero Section
Located near the top of the page, find this code:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold leading-tight tracking-tight text-gray-900 mb-6">
    Merriam, Kansas Corporate Headshot Photography Services
</h1>
```
To update:
1. Locate the text between the `<h1>` tags
2. Replace with your new heading
3. Keep the existing classes to maintain styling

#### Services Cards
Find the services section with three cards:
```html
<div class="bg-gray-50 rounded-2xl p-8 hover:shadow-xl transition-shadow duration-300">
    <h3 class="text-xl font-semibold mb-4">Image Boost</h3>
    <p class="text-gray-600">Professional headshots that elevate your personal brand...</p>
</div>
```
To update:
1. Locate each card within the services section
2. Change the `<h3>` title text
3. Update the description in the `<p>` tag

### Modifying Tailwind CSS Classes

#### Understanding Basic Classes
Common classes used throughout:
- `container mx-auto`: Centers content with auto margins
- `px-6`: Adds horizontal padding
- `py-24`: Adds vertical padding
- `text-xl`: Sets text size
- `font-semibold`: Sets font weight

#### Responsive Design Classes
Example of responsive text sizing:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl">
```
Breaking down the classes:
- `text-4xl`: Default size on mobile
- `md:text-5xl`: Medium screens (768px+)
- `lg:text-6xl`: Large screens (1024px+)

## Fixing Broken Links

### Navigation Menu Links
Current navigation links in the header:
```html
<div class="hidden md:flex space-x-8">
    <a href="#services">Services</a>
    <a href="#benefits">Benefits</a>
    <a href="#faq">FAQ</a>
    <a href="#contact">Contact</a>
</div>
```

To update:
1. Locate the `href` attribute
2. For internal sections, use `#section-name`
3. For external links, use the full URL: `https://www.example.com`

### Book Now Button
Find this code:
```html
<a href="https://www.101headshots.com" class="bg-blue-600 text-white px-6 py-2 rounded-full">
```
To update:
1. Replace the URL in `href=""`
2. Test the link after updating

## Linking Privacy and Terms Pages

### Footer Legal Links
Located at the bottom of the page:
```html
<div>
    <h3 class="text-white text-lg font-semibold mb-4">Legal</h3>
    <ul class="space-y-2 text-sm">
        <li><a href="#" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="#" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

To add privacy and terms pages:
1. Create `privacy.html` and `terms.html` in your root directory
2. Update the href attributes:
```html
<li><a href="privacy.html" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
```

## Troubleshooting

### Common Issues

1. **Broken Internal Links**
   - Ensure section IDs match the href attributes
   - Check for typos in IDs
   - IDs should not contain spaces

2. **Responsive Design Issues**
   - Check mobile view using browser dev tools
   - Verify responsive classes (md:, lg:) are correct
   - Test on different screen sizes

3. **Missing Styles**
   - Confirm Tailwind CSS CDN link is present
   - Check for typos in class names
   - Verify all closing tags are present

### Need Help?
- Use browser developer tools (F12) to inspect elements
- Check the Tailwind CSS documentation for class references
- Verify all files are in the correct directory
- Test all links after making changes

Remember to always backup your files before making significant changes, and test your updates across different devices and browsers.