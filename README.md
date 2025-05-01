# Landing Page Maintenance Guide

This guide will help you maintain and customize the WebAgency landing page. Follow these detailed instructions to make common updates while preserving the design and functionality.

## Table of Contents
1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Header Section
The header contains your company name and navigation menu. To update:

1. Change company name:
```html
<!-- Find this line in the header section -->
<a href="#" class="text-2xl font-bold text-white hover:text-blue-400 transition duration-300">
    WebAgency  <!-- Replace this text -->
</a>
```

2. Modify navigation items:
```html
<div class="hidden md:flex space-x-8">
    <!-- Each link can be updated here -->
    <a href="#features" class="text-gray-300 hover:text-white transition duration-300">Features</a>
</div>
```

### Hero Section
Update the main headline and subheading:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-extrabold tracking-tight text-white mb-8">
    Best Web Agency In Sydney  <!-- Replace main headline -->
</h1>
<p class="text-xl md:text-2xl text-gray-300 mb-12">
    Grow your business with clicks  <!-- Replace subheading -->
</p>
```

### Understanding Tailwind Classes
Common classes used in this template:
- `text-{size}`: Controls text size (e.g., `text-xl`, `text-2xl`)
- `bg-{color}-{shade}`: Sets background color (e.g., `bg-gray-900`)
- `p-{number}`: Sets padding (e.g., `p-8`)
- `m-{number}`: Sets margin (e.g., `mb-8` for margin-bottom)
- `md:`: Applies styles at medium screen sizes
- `hover:`: Applies styles on mouse hover

## Fixing Broken Links

### Current Link Inventory
1. Navigation Menu Links:
```html
<a href="#features">Features</a>
<a href="#benefits">Benefits</a>
<a href="#faq">FAQ</a>
<a href="#contact">Contact</a>
```

2. Call-to-Action Links:
```html
<!-- Update this URL for all CTA buttons -->
<a href="https://fixrr.online" class="inline-flex items-center...">
```

### Updating Links
1. For internal section links:
- Ensure the `href` matches the section's `id` attribute
- Example: `<a href="#features">` should match `<section id="features">`

2. For external links:
```html
<!-- Replace placeholder URLs -->
<a href="https://your-actual-website.com" class="...">
```

## Adding Privacy and Terms Pages

### Footer Modification
Add privacy and terms links in the Quick Links section:
```html
<div>
    <h4 class="text-lg font-semibold mb-4">Quick Links</h4>
    <ul class="space-y-2">
        <!-- Add these new lines -->
        <li><a href="privacy.html" class="text-gray-400 hover:text-white transition duration-300">Privacy Policy</a></li>
        <li><a href="terms.html" class="text-gray-400 hover:text-white transition duration-300">Terms of Service</a></li>
        <!-- Existing links -->
        <li><a href="#features" class="text-gray-400 hover:text-white transition duration-300">Features</a></li>
    </ul>
</div>
```

## Troubleshooting

### Common Issues and Solutions

1. **Broken Section Links**
- Verify that section IDs match exactly with href attributes
- Check for typos in both the link and section ID
```html
<!-- These must match exactly -->
<a href="#features">
<section id="features">
```

2. **Responsive Design Issues**
- Don't remove `md:` or `lg:` prefixes from classes
- Keep the existing responsive structure:
```html
class="text-4xl md:text-5xl lg:text-6xl"
```

3. **Animation Problems**
- Ensure AOS script is loaded:
```html
<script src="https://unpkg.com/aos@2.3.1/dist/aos.css"></script>
```
- Verify data-aos attributes are present:
```html
data-aos="fade-up"
```

### Best Practices
- Always test changes across different screen sizes
- Maintain consistent spacing using Tailwind's utility classes
- Keep the color scheme consistent using existing color classes
- Preserve the responsive design patterns
- Test all links after making changes

Need more help? Contact your web development team or refer to the [Tailwind CSS documentation](https://tailwindcss.com/docs).