# Texas Web Design Landing Page - Maintenance Guide

This guide will help you maintain and customize the Texas Web Design landing page. It's written specifically for beginners and provides detailed instructions for common maintenance tasks.

## Table of Contents
1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Text Content Updates

#### Hero Section
The main headline and subheading are located in the hero section:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 mb-6 leading-tight tracking-tight">
    Best Websites In Texas
</h1>
<p class="text-xl md:text-2xl text-gray-600 mb-10 leading-relaxed">
    Professional web design solutions tailored for Texas businesses
</p>
```
To update:
1. Locate the text between the `<h1>` tags for the main headline
2. Locate the text between the `<p>` tags for the subheading
3. Replace the text while keeping the HTML tags intact

#### Features Section
Each feature card contains:
- Icon (using Font Awesome)
- Heading
- Description

Example of a feature card:
```html
<div class="bg-white rounded-xl shadow-lg p-8 hover:shadow-xl transition-shadow duration-300">
    <div class="text-blue-600 mb-4">
        <i class="fas fa-server text-4xl"></i>
    </div>
    <h3 class="text-xl font-semibold mb-4">Free Hosting</h3>
    <p class="text-gray-600 leading-relaxed">
        Complimentary hosting services included with every website package
    </p>
</div>
```

### Tailwind CSS Classes Explained

#### Common Class Patterns
- Spacing: `p-8` (padding), `mb-4` (margin-bottom)
- Text size: `text-xl`, `text-4xl`
- Colors: `text-blue-600`, `bg-white`
- Responsive design: `md:text-5xl` (applies at medium screens)

#### Important Responsive Classes
```html
<!-- Example of responsive classes -->
<div class="text-2xl md:text-3xl lg:text-4xl">
```
- Default: `text-2xl` (mobile)
- `md:text-3xl` (tablets)
- `lg:text-4xl` (desktop)

## Fixing Broken Links

### Navigation Menu Links
Current navigation links are:
```html
<div class="hidden md:flex space-x-8">
    <a href="#features" class="text-gray-600 hover:text-blue-600 transition-colors duration-300">Features</a>
    <a href="#benefits" class="text-gray-600 hover:text-blue-600 transition-colors duration-300">Benefits</a>
    <a href="#faq" class="text-gray-600 hover:text-blue-600 transition-colors duration-300">FAQ</a>
    <a href="#contact" class="text-gray-600 hover:text-blue-600 transition-colors duration-300">Contact</a>
</div>
```

To update:
1. Locate the `href` attribute
2. Replace the value with:
   - `#section-name` for same-page links
   - Full URL for external links (e.g., `https://example.com`)
   - Relative path for internal pages (e.g., `./about.html`)

### Social Media Links
Located in the footer:
```html
<div class="flex space-x-4">
    <a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">
        <i class="fab fa-facebook text-xl"></i>
    </a>
    <!-- Similar structure for Twitter and LinkedIn -->
</div>
```

To update:
1. Replace the `#` in `href="#"` with your social media profile URLs
2. Ensure URLs include `https://` prefix

## Adding Privacy and Terms Pages

### Step 1: Add Footer Links
Add these links to the footer's Quick Links section:
```html
<ul class="space-y-2">
    <li><a href="./privacy.html" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
    <li><a href="./terms.html" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
</ul>
```

### Step 2: Create New Pages
1. Create `privacy.html` and `terms.html` in the same directory
2. Copy the header and footer from `index.html`
3. Add your policy content between them

Example structure:
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <!-- Copy head section from index.html -->
</head>
<body>
    <!-- Copy header section -->
    
    <main class="pt-32 pb-24">
        <div class="container mx-auto px-6">
            <h1 class="text-3xl font-bold mb-8">Privacy Policy</h1>
            <!-- Add your privacy policy content here -->
        </div>
    </main>

    <!-- Copy footer section -->
</body>
</html>
```

## Troubleshooting

### Common Issues

1. **Broken Navigation Links**
   - Check that section IDs match href values
   - Ensure section IDs are unique
   - Verify file paths for external pages

2. **Responsive Design Issues**
   - Test at different screen sizes
   - Verify media query classes (md:, lg:) are correct
   - Check for missing responsive classes

3. **Icon Display Problems**
   - Verify Font Awesome CSS is loaded
   - Check icon class names against Font Awesome documentation
   - Ensure internet connection for CDN access

### Need Help?
If you encounter issues:
1. Check the browser console for errors (F12)
2. Verify all files are in the correct directory
3. Ensure all CDN links are accessible
4. Test the page in multiple browsers

Remember to always backup your files before making changes!