# Texas Web Design Landing Page - Maintenance Guide

This guide will help you maintain and customize the Texas Web Design landing page. It's written for beginners with no prior coding experience.

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
3. Features Section
4. Benefits Section
5. FAQ Section
6. Call to Action
7. Footer

### Updating Text Content

#### Header Text
To update the logo text:
```html
<!-- Find this line in the header section -->
<a href="/" class="text-2xl font-bold text-blue-600">TWD</a>
```
Simply replace "TWD" with your desired text.

#### Hero Section Text
Locate the hero section and modify these lines:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 mb-6">Texas Web Design</h1>
<p class="text-xl md:text-2xl text-gray-600 mb-12">Best Websites In Texas</p>
```
Replace "Texas Web Design" and "Best Websites In Texas" with your desired content.

### Modifying Tailwind CSS Classes

#### Understanding Responsive Classes
In this code, responsive classes use these prefixes:
- `md:` - applies to medium screens (768px and up)
- `lg:` - applies to large screens (1024px and up)

Example:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl">
```
This means:
- Mobile: text-4xl (2.25rem)
- Tablet: text-5xl (3rem)
- Desktop: text-6xl (3.75rem)

#### Common Tailwind Classes Used
- Text Colors: `text-gray-900`, `text-blue-600`, `text-white`
- Background Colors: `bg-white`, `bg-blue-600`, `bg-gray-50`
- Spacing: `px-4`, `py-24`, `mb-6`, `mt-12`
- Flex Layout: `flex`, `items-center`, `justify-between`
- Grid Layout: `grid`, `grid-cols-1`, `md:grid-cols-3`

## Managing Links

### Navigation Menu Links
Current navigation links are:
```html
<div class="hidden md:flex items-center space-x-8">
    <a href="#features">Features</a>
    <a href="#benefits">Benefits</a>
    <a href="#faq">FAQ</a>
    <a href="https://twd.com">Get Started</a>
</div>
```

To update links:
1. For internal sections, use `#section-name`
2. For external links, use the full URL
3. Replace `https://twd.com` with your actual website URL

### Call-to-Action Links
Locate these buttons and update their `href` attributes:
```html
<!-- Hero section button -->
<a href="https://twd.com" class="inline-block bg-blue-600...">Start Your Project</a>

<!-- Bottom CTA button -->
<a href="https://twd.com" class="inline-block bg-white...">Contact Us Today</a>
```

## Adding Privacy and Terms Pages

### Step 1: Create New Pages
Create two new files in your website directory:
- `privacy.html`
- `terms.html`

### Step 2: Update Footer Links
Locate this section in the footer:
```html
<div>
    <h4 class="text-lg font-semibold mb-4">Legal</h4>
    <ul class="space-y-2">
        <li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

Replace the `#` placeholders:
```html
<li><a href="privacy.html" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
```

## Troubleshooting

### Common Issues and Solutions

1. **Links Not Working**
   - Check for typos in `href` attributes
   - Ensure file names match exactly (case-sensitive)
   - Verify file locations are correct

2. **Styling Issues**
   - Make sure Tailwind CSS CDN link is present in the head section
   - Check for missing or mistyped class names
   - Verify responsive classes are properly prefixed (`md:`, `lg:`)

3. **Layout Problems**
   - Check for unclosed div tags
   - Verify grid column settings
   - Ensure responsive classes are correctly applied

### Need Help?
- Double-check the original HTML structure
- Use browser developer tools (F12) to inspect elements
- Maintain consistent indentation for better readability
- Test all changes across different screen sizes

Remember to always backup your code before making significant changes!