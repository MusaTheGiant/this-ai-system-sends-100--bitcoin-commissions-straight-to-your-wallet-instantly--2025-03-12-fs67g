# AI Bitcoin Landing Page - Maintenance Guide

This guide will help you maintain and customize the AI Bitcoin landing page. It's written for beginners with no prior coding experience.

## Table of Contents
- [Updating Text and Styling](#updating-text-and-styling)
- [Managing Links](#managing-links)
- [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
- [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains the logo and navigation menu. To modify:

1. **Logo Text**: Find this line and change "AI Bitcoin":
```html
<div class="text-2xl font-bold text-blue-600">AI Bitcoin</div>
```

2. **Navigation Links**: Located in the header section:
```html
<div class="hidden md:flex space-x-8">
    <a href="#features">Features</a>
    <a href="#benefits">Benefits</a>
    <a href="#faq">FAQ</a>
</div>
```

### Hero Section
Update the main headline and subheading:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 leading-tight mb-6">
    This AI System Sends 100% Bitcoin Commissions Straight to Your Wallet-Instantly
</h1>
<p class="text-xl md:text-2xl text-gray-600 mb-12">
    The Easiest and Fastest Way to Accumulate Bitcoin daily!
</p>
```

### Tailwind CSS Classes Explained
Common classes used throughout:
- `text-[size]`: Controls text size (xl, 2xl, 3xl, etc.)
- `mb-[size]`: Adds margin bottom (4, 6, 8, etc.)
- `py-[size]`: Adds padding top and bottom
- `bg-[color]`: Sets background color
- `text-[color]`: Sets text color

Example: To make text larger and blue:
```html
<p class="text-2xl text-blue-600">Your text here</p>
```

## Managing Links

### Current Link Structure
The page contains these link types:
1. Navigation links (internal):
```html
<a href="#features">Features</a>
<a href="#benefits">Benefits</a>
<a href="#faq">FAQ</a>
```

2. Call-to-action links (external):
```html
<a href="https://go.e1ulife.com/ai-takeover?affid=realmtg">Get Started</a>
```

### Updating Links
To update any link:
1. Locate the `<a>` tag
2. Modify the `href` attribute
3. Update the text between the tags

Example:
```html
<!-- Before -->
<a href="#features">Features</a>

<!-- After -->
<a href="#new-section">New Section</a>
```

### Social Media Links
Located in the footer:
```html
<div class="flex space-x-4">
    <a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">
        <i class="fab fa-twitter"></i>
    </a>
    <!-- Add your social media URLs here -->
</div>
```

## Adding Privacy and Terms Pages

### Step 1: Create New Files
Create two new files in your project:
- `privacy.html`
- `terms.html`

### Step 2: Update Footer Links
Locate these lines in the footer:
```html
<ul class="space-y-2">
    <li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
    <li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
</ul>
```

Replace with:
```html
<ul class="space-y-2">
    <li><a href="privacy.html" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
    <li><a href="terms.html" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
</ul>
```

## Troubleshooting

### Common Issues

1. **Broken Links**
   - Check for typos in `href` attributes
   - Ensure file names match exactly
   - Verify file locations/paths

2. **Styling Problems**
   - Make sure Tailwind CSS is properly loaded
   - Check for missing or mistyped class names
   - Verify responsive classes (md:, lg:) are correct

3. **Layout Issues**
   - Inspect container widths (`container mx-auto`)
   - Check padding classes (`px-6`, `py-4`)
   - Verify grid classes (`grid-cols-1 md:grid-cols-3`)

### Need Help?
If you encounter issues:
1. Check the browser's developer tools (F12)
2. Verify all CDN links are working
3. Double-check class names against Tailwind documentation
4. Contact support at the email provided in the footer

Remember to always test changes across different screen sizes using your browser's responsive design mode.