# Stomerij Wateringen Landing Page - Maintenance Guide

This guide will help you maintain and customize the Stomerij Wateringen landing page. Whether you're new to web development or need a quick reference, follow these detailed instructions for common maintenance tasks.

## Table of Contents
1. [Updating Text and Styling](#updating-text-and-styling)
2. [Managing Links](#managing-links)
3. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains the company name and navigation menu. To update:

```html
<!-- Company Name -->
<a href="/" class="text-2xl font-bold text-blue-600">Stomerij Wateringen</a>

<!-- Navigation Items -->
<div class="hidden md:flex space-x-8">
    <a href="#diensten" class="text-gray-600 hover:text-blue-600 transition duration-300">Diensten</a>
    <!-- More menu items... -->
</div>
```

To modify:
1. Change company name: Replace "Stomerij Wateringen" with your text
2. Adjust text size: Modify `text-2xl` to `text-3xl` for larger text
3. Change color: Replace `text-blue-600` with other Tailwind colors (e.g., `text-red-600`)

### Hero Section
Located at the top of the page with main headline and call-to-action:

```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-extrabold text-gray-900 mb-8">
    🌟 Stomerij Wateringen: Gratis Haal- en Brengservice! 🚚
</h1>
```

To modify:
1. Update headline: Replace text between `<h1>` tags
2. Adjust spacing: Modify `mb-8` (margin-bottom) to `mb-4` for less space
3. Change text size: Adjust `text-4xl` classes for different screen sizes

### Features Section
Contains service cards with icons and descriptions:

```html
<div class="bg-white p-8 rounded-2xl shadow-lg hover:shadow-xl transition duration-300">
    <div class="text-4xl mb-4">👕</div>
    <h3 class="text-xl font-bold mb-4">Premium Stoomservice</h3>
    <p class="text-gray-600">Professionele behandeling voor al uw delicate kleding</p>
</div>
```

To modify:
1. Change icon: Replace emoji between first `<div>` tags
2. Update title: Modify text in `<h3>` tags
3. Edit description: Update text in `<p>` tags
4. Adjust card styling: Modify `p-8` padding or `shadow-lg` shadow effect

## Managing Links

### Navigation Menu Links
Current internal links in the navigation:

```html
<a href="#diensten">Diensten</a>
<a href="#voordelen">Voordelen</a>
<a href="#faq">FAQ</a>
<a href="#contact">Contact</a>
```

To update:
1. Internal links: Keep `#` prefix for same-page sections
2. External links: Replace with full URL (e.g., `href="https://example.com"`)
3. Ensure matching IDs exist for internal links (e.g., `id="diensten"` on target section)

### Call-to-Action Links
Located in hero and CTA sections:

```html
<a href="https://wasserettewestland.nl" class="inline-block px-8 py-4 text-lg font-semibold text-white bg-blue-600 rounded-full">
    Direct Reserveren
</a>
```

To modify:
1. Update URL: Replace `https://wasserettewestland.nl` with your booking link
2. Change button text: Modify "Direct Reserveren" as needed
3. Adjust styling: Modify color (`bg-blue-600`) or padding (`px-8 py-4`)

## Adding Privacy and Terms Pages

### Footer Links Section
Located in the footer:

```html
<ul class="space-y-2">
    <li><a href="#" class="hover:text-blue-400 transition duration-300">Privacy Policy</a></li>
    <li><a href="#" class="hover:text-blue-400 transition duration-300">Algemene Voorwaarden</a></li>
</ul>
```

To add privacy and terms pages:
1. Create new HTML files:
   - Create `privacy.html` in your root directory
   - Create `terms.html` in your root directory

2. Update footer links:
```html
<li><a href="privacy.html" class="hover:text-blue-400 transition duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="hover:text-blue-400 transition duration-300">Algemene Voorwaarden</a></li>
```

## Troubleshooting

### Common Issues

1. **Broken Internal Links**
   - Check that section IDs match navigation href attributes
   - Ensure hash (#) prefix is present for internal links
   - Verify no spaces in ID names

2. **Responsive Design Issues**
   - Check responsive classes (e.g., `md:`, `lg:` prefixes)
   - Test on different screen sizes
   - Verify mobile menu functionality

3. **Style Problems**
   - Confirm Tailwind CSS CDN link is working
   - Check for typos in class names
   - Ensure classes are space-separated

### Need Help?
- Validate HTML at [W3C Validator](https://validator.w3.org/)
- Check Tailwind documentation for class references
- Test all links before deploying changes

Remember to always backup your files before making significant changes, and test thoroughly across different devices and browsers.