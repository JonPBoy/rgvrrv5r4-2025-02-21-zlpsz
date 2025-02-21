# Landing Page Maintenance Guide

This guide will help you maintain and customize the Claude AI landing page. Whether you're new to web development or need a quick reference, follow these instructions to make common updates safely and effectively.

## Table of Contents
- [Updating Text and Styling](#updating-text-and-styling)
- [Managing Links](#managing-links)
- [Adding Policy Pages](#adding-policy-pages)
- [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Hero Section
The main headline and subtitle are located in the first `<section>` after `<main>`:

```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold tracking-tight mb-8">
    rgvrrv5r4  <!-- Replace this text -->
</h1>
<p class="text-xl md:text-2xl text-gray-400 max-w-3xl mx-auto mb-12">
    efefef  <!-- Replace this text -->
</p>
```

To update:
1. Locate the placeholder text (`rgvrrv5r4` and `efefef`)
2. Replace with your desired content
3. Keep the surrounding HTML tags intact

### Understanding Tailwind Classes
The page uses Tailwind CSS for styling. Common class patterns:

- Size classes: `text-4xl` (large text), `text-xl` (medium text)
- Colors: `text-gray-400` (text color), `bg-purple-600` (background color)
- Spacing: `mb-8` (margin bottom), `px-6` (padding left/right)
- Responsive prefixes: `md:` (medium screens), `lg:` (large screens)

Example of modifying button color:
```html
<!-- Original -->
<a href="#contact" class="bg-purple-600 hover:bg-purple-700">

<!-- Changed to blue -->
<a href="#contact" class="bg-blue-600 hover:bg-blue-700">
```

### Benefits Section
To add or modify benefit cards:

```html
<div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
    <div class="p-8 bg-gray-800 rounded-2xl hover:bg-gray-700 transition-colors">
        <h3 class="text-xl font-semibold mb-4">c4t4f4f4x</h3>
        <p class="text-gray-400">Transform your workflow...</p>
    </div>
    <!-- Copy and paste this div to add more benefit cards -->
</div>
```

## Managing Links

### Navigation Menu Links
Current navigation links are in the header:

```html
<div class="hidden md:flex items-center space-x-8">
    <a href="#features" class="hover:text-purple-400 transition-colors">Features</a>
    <a href="#benefits" class="hover:text-purple-400 transition-colors">Benefits</a>
    <a href="#contact" class="hover:text-purple-400 transition-colors">Contact</a>
</div>
```

To update links:
1. Locate the `href` attribute
2. For same-page sections, use `#section-id`
3. For external links, use full URL: `https://example.com`
4. For internal pages, use relative path: `./about.html`

### Email Links
Update email addresses in two locations:

```html
<!-- Contact section -->
<p class="text-xl text-gray-400 mb-8">Contact us at: jojo@zdd.com</p>
<a href="mailto:jojo@zdd.com">Send Email</a>

<!-- Footer -->
<div>
    <h4 class="font-semibold mb-4">Contact</h4>
    <p class="text-gray-400">jojo@zdd.com</p>
</div>
```

## Adding Policy Pages

### Footer Policy Links
Current placeholder links:

```html
<div>
    <h4 class="font-semibold mb-4">Legal</h4>
    <ul class="space-y-2 text-gray-400">
        <li><a href="#" class="hover:text-purple-400 transition-colors">Privacy Policy</a></li>
        <li><a href="#" class="hover:text-purple-400 transition-colors">Terms of Service</a></li>
    </ul>
</div>
```

To link to policy pages:
1. Create `privacy.html` and `terms.html` in your project folder
2. Update the href attributes:

```html
<li><a href="./privacy.html" class="hover:text-purple-400 transition-colors">Privacy Policy</a></li>
<li><a href="./terms.html" class="hover:text-purple-400 transition-colors">Terms of Service</a></li>
```

## Troubleshooting

Common issues and solutions:

1. **Broken Layout**
   - Check that you haven't removed any closing tags
   - Verify Tailwind CSS is loading (check network tab in browser dev tools)
   - Ensure responsive classes (`md:`, `lg:`) remain intact

2. **Links Not Working**
   - For section links (#features), ensure the ID exists in the HTML
   - Check for typos in href attributes
   - Verify file paths for internal pages are correct

3. **Styles Not Applying**
   - Confirm Tailwind CSS link in head section is working
   - Check for typos in class names
   - Make sure classes are space-separated

Need help? Contact your development team or refer to the [Tailwind CSS documentation](https://tailwindcss.com/docs).