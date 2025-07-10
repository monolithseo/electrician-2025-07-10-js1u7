# NYC Electric Landing Page - Maintenance Guide

This guide will help you maintain and customize the NYC Electric landing page. It's written for beginners and provides detailed instructions for common updates and modifications.

## Table of Contents
- [Updating Text and Styling](#updating-text-and-styling)
- [Managing Links](#managing-links)
- [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
- [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains the company name and navigation menu. To update:

1. **Company Name:**
```html
<!-- Find this line in the header -->
<a href="#" class="text-2xl font-bold bg-gradient-to-r from-blue-500 to-purple-600 bg-clip-text text-transparent">NYC Electric</a>
```
Simply replace "NYC Electric" with your company name. The gradient styling will automatically apply.

2. **Navigation Menu Items:**
```html
<div class="hidden md:flex space-x-8">
    <a href="#services" class="text-gray-300 hover:text-white transition-colors duration-300">Services</a>
    <!-- Add or modify menu items here -->
</div>
```
Each menu item follows the same pattern. Copy and paste an existing line to add new items.

### Hero Section
The main headline and subheading are in the hero section:

```html
<h1 class="text-4xl md:text-6xl lg:text-7xl font-bold bg-gradient-to-r from-blue-500 to-purple-600 bg-clip-text text-transparent mb-6">
    Expert Electrical Services in New York
</h1>
<p class="text-xl md:text-2xl text-gray-300 mb-8">
    Professional, reliable electrical solutions available 24/7
</p>
```

To modify:
1. Replace the text between the `<h1>` tags for the main headline
2. Replace the text between the `<p>` tags for the subheading
3. Keep the existing classes to maintain responsive design

### Understanding Tailwind Classes

Key class patterns used throughout:
- Responsive prefixes: `md:` (768px), `lg:` (1024px)
- Spacing: `px-4` (padding left/right), `py-24` (padding top/bottom)
- Colors: `text-gray-300`, `bg-gray-800`
- Hover effects: `hover:scale-105`, `hover:text-white`

## Managing Links

### Navigation Menu Links
Current internal links in the navigation:
```html
<a href="#services">Services</a>
<a href="#features">Features</a>
<a href="#benefits">Benefits</a>
<a href="#faq">FAQ</a>
```

To update:
1. The `#` symbol indicates an internal link to a section ID
2. Match the `href` value to the `id` attribute of the target section
3. For external links, use the full URL: `href="https://example.com"`

### Footer Links
The footer contains multiple link sections:

```html
<ul class="space-y-2 text-gray-400">
    <li><a href="#" class="hover:text-white transition-colors duration-300">Home</a></li>
    <li><a href="#services" class="hover:text-white transition-colors duration-300">Services</a></li>
    <!-- Add more links here -->
</ul>
```

To update:
1. Replace `#` with proper page URLs
2. Maintain the class structure for consistent styling
3. Add new links by copying the existing `<li>` pattern

## Adding Privacy and Terms Pages

### Step 1: Add Footer Links
Add these lines to the footer's Quick Links section:

```html
<li><a href="privacy.html" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
```

### Step 2: Create New Pages
1. Create `privacy.html` and `terms.html` in your root directory
2. Copy the header and footer from `index.html` to maintain consistent styling
3. Add your policy content between the header and footer

Example structure for policy pages:
```html
<!-- privacy.html or terms.html -->
<!DOCTYPE html>
<html lang="en" class="scroll-smooth">
<head>
    <!-- Copy head section from index.html -->
</head>
<body class="bg-gray-900 text-gray-100 font-inter antialiased">
    <!-- Copy header section -->
    
    <main class="container mx-auto px-4 sm:px-6 lg:px-8 py-24">
        <h1 class="text-3xl font-bold mb-8">Privacy Policy</h1>
        <!-- Add your policy content here -->
    </main>

    <!-- Copy footer section -->
</body>
</html>
```

## Troubleshooting

Common issues and solutions:

1. **Broken Internal Links**
   - Ensure section IDs match exactly with href values
   - IDs are case-sensitive
   - Check for extra spaces in IDs

2. **Responsive Design Issues**
   - Don't remove `md:` or `lg:` prefixes from classes
   - Keep the viewport meta tag in the head section
   - Test on different screen sizes using browser dev tools

3. **Gradient Text Not Showing**
   - Ensure all three classes are present:
     - `bg-gradient-to-r`
     - `bg-clip-text`
     - `text-transparent`

Need help? Contact your web developer or refer to the [Tailwind CSS documentation](https://tailwindcss.com/docs).