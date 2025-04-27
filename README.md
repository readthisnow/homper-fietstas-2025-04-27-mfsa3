# Homper Landing Page Maintenance Guide

This guide will help you maintain and customize the Homper landing page. It's written for beginners with no prior coding experience.

## Table of Contents
- [Updating Text and Styling](#updating-text-and-styling)
- [Managing Links](#managing-links)
- [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
- [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Main Sections
The landing page is divided into these key sections:

1. Header (Navigation)
2. Hero Section
3. Features
4. Benefits
5. FAQ
6. Call-to-Action
7. Footer

### How to Update Text Content

#### Updating the Hero Section
```html
<!-- Located near the top of the page -->
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 mb-6 leading-tight">
    Homper Fietstas
</h1>
```
To change the main title, simply replace "Homper Fietstas" with your desired text.

#### Updating Feature Cards
```html
<div class="bg-white rounded-xl p-8 shadow-lg hover:shadow-xl transition-shadow duration-300">
    <i class="fas fa-shield-alt text-3xl text-blue-600 mb-4"></i>
    <h3 class="text-xl font-semibold mb-4">Waterdicht Design</h3>
    <p class="text-gray-600">Bescherm je spullen tegen alle weersomstandigheden</p>
</div>
```
To modify a feature card:
1. Change the icon by updating the `fa-shield-alt` class to another FontAwesome icon
2. Update the heading text within the `<h3>` tags
3. Modify the description within the `<p>` tags

### Understanding Tailwind Classes

#### Common Class Patterns
- Text sizes: `text-sm`, `text-xl`, `text-2xl`, etc.
- Colors: `text-gray-600`, `bg-blue-600`, etc.
- Spacing: `p-8` (padding), `mb-4` (margin-bottom)
- Responsive design: `md:text-4xl` (applies at medium screens)

Example of modifying text size:
```html
<!-- Original -->
<h2 class="text-3xl md:text-4xl font-bold text-center mb-16">

<!-- Making text larger -->
<h2 class="text-4xl md:text-5xl font-bold text-center mb-16">
```

## Managing Links

### Navigation Menu Links
Current navigation links are located in the header:
```html
<div class="hidden md:flex space-x-8">
    <a href="#features">Features</a>
    <a href="#benefits">Voordelen</a>
    <a href="#faq">FAQ</a>
    <a href="#contact">Contact</a>
</div>
```

To update a link:
1. Locate the `<a>` tag
2. Modify the `href` attribute
3. Update the link text

Example:
```html
<!-- Original -->
<a href="#features">Features</a>

<!-- Updated -->
<a href="#new-section">New Section</a>
```

### Call-to-Action Links
The main CTA buttons use Amazon affiliate links:
```html
<a href="https://amzn.to/431gxKK" class="inline-block bg-blue-600 text-white px-8 py-4 rounded-full">
```

To update:
1. Replace `https://amzn.to/431gxKK` with your new link
2. Keep the existing classes to maintain styling

## Adding Privacy and Terms Pages

### Current Footer Links
```html
<ul class="space-y-2">
    <li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
    <li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">Terms & Conditions</a></li>
</ul>
```

### Steps to Add Policy Pages

1. Create new HTML files:
   - Create `privacy.html`
   - Create `terms.html`

2. Update the footer links:
```html
<li><a href="privacy.html" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="text-gray-400 hover:text-white transition-colors duration-300">Terms & Conditions</a></li>
```

3. Ensure consistent styling by copying the header and footer from `index.html` to your new pages

## Troubleshooting

### Common Issues

1. **Broken Internal Links**
   - Check that section IDs match their corresponding links
   - Example: `href="#features"` should match `id="features"`

2. **Responsive Design Issues**
   - Look for classes starting with `sm:`, `md:`, or `lg:`
   - These control how elements appear at different screen sizes

3. **Icon Not Showing**
   - Verify the FontAwesome CDN link is present in the `<head>`
   - Check that icon class names are correct (e.g., `fa-shield-alt`)

### Need Help?
- Double-check your changes against the original code
- Use browser developer tools (F12) to inspect elements
- Ensure all HTML tags are properly closed
- Verify that copied classes match exactly (Tailwind is case-sensitive)

Remember to test all changes across different screen sizes and browsers before publishing updates.