# LoanCalc Landing Page - Maintenance Guide

This guide provides detailed instructions for maintaining and customizing the LoanCalc landing page. Whether you're new to web development or need a quick reference, you'll find step-by-step guidance for common updates.

## Table of Contents
- [Updating Text and Styling](#updating-text-and-styling)
- [Managing Navigation Links](#managing-navigation-links)
- [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
- [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains the logo and navigation menu. To update:

1. **Logo Text**: Locate this section in the header:
```html
<div class="text-2xl font-bold bg-gradient-to-r from-blue-600 to-indigo-600 bg-clip-text text-transparent">
    LoanCalc
</div>
```
Simply replace "LoanCalc" with your desired text.

2. **Navigation Menu Items**: Find the navigation div:
```html
<div class="hidden md:flex space-x-8">
    <a href="#features" class="text-gray-600 hover:text-blue-600 transition-colors duration-300">Features</a>
    <a href="#benefits" class="text-gray-600 hover:text-blue-600 transition-colors duration-300">Benefits</a>
    <a href="#contact" class="text-gray-600 hover:text-blue-600 transition-colors duration-300">Contact</a>
</div>
```
To add or modify menu items, copy an existing `<a>` tag and update the `href` and text content.

### Hero Section
Located at the top of the page, modify the main headline and subtext:

```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold leading-tight mb-8 bg-gradient-to-r from-blue-600 to-indigo-600 bg-clip-text text-transparent">
    Commercial Business Loans Calculator - Leverage Advanced Growth Forecasting
</h1>
<p class="text-xl md:text-2xl text-gray-600 mb-12">
    Harness the power of our Commercial Business Loan Calculator
</p>
```

### Tailwind CSS Classes Explained
- `text-4xl`: Sets font size (increases with `md:` and `lg:` prefixes for different screen sizes)
- `font-bold`: Makes text bold
- `mb-8`: Adds margin bottom (spacing)
- `bg-gradient-to-r`: Creates right-flowing gradient
- `text-transparent`: Makes text transparent to show gradient background

## Managing Navigation Links

### Internal Links
The page uses anchor links to navigate sections. Update these in two places:

1. **Navigation Menu**:
```html
<a href="#features">Features</a>
<a href="#benefits">Benefits</a>
<a href="#contact">Contact</a>
```

2. **Corresponding Sections**:
Ensure section IDs match the href values:
```html
<section id="features" class="py-24 bg-white">
<section id="benefits" class="py-24 bg-gradient-to-b from-gray-50 to-white">
```

### Email Links
Current email links use mailto:
```html
<a href="mailto:briansavic@me.com">Contact Us Now</a>
```
Replace `briansavic@me.com` with your email address wherever it appears.

## Adding Privacy and Terms Pages

### Step 1: Create New Pages
Create two new files in your project directory:
- `privacy.html`
- `terms.html`

### Step 2: Update Footer Links
Locate the legal section in the footer:
```html
<div>
    <h4 class="text-lg font-semibold text-white mb-4">Legal</h4>
    <ul class="space-y-2">
        <li><a href="#" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="#" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

Replace the `#` placeholder with proper paths:
```html
<li><a href="privacy.html" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
```

## Troubleshooting

### Common Issues and Solutions

1. **Broken Links**
   - Check that all `href` attributes point to valid files or sections
   - Ensure section IDs exist and match exactly (case-sensitive)
   - Test all links after updating

2. **Styling Issues**
   - Verify Tailwind CSS is properly loaded
   - Check for typos in class names
   - Maintain responsive design classes (`md:`, `lg:` prefixes)

3. **Layout Problems**
   - Keep the container structure intact:
```html
<div class="container mx-auto px-6">
    <!-- Content here -->
</div>
```
   - Maintain the grid system in features and benefits sections

### Need Help?
- Double-check the Tailwind CSS version (currently using 2.2.19)
- Verify Alpine.js is loading correctly
- Ensure all sections have proper opening and closing tags
- Keep the responsive design intact by not removing media query classes

Remember to test all changes across different screen sizes using your browser's developer tools.