# LuxuryBath Landing Page Maintenance Guide

This guide provides detailed instructions for maintaining and customizing the LuxuryBath landing page. Whether you're new to web development or need a quick reference, follow these step-by-step instructions.

## Table of Contents
1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Text Content Updates

#### Company Name and Branding
```html
<!-- Located in the header -->
<div class="text-2xl font-bold text-gray-800">LuxuryBath</div>

<!-- Located in the footer -->
<h3 class="text-xl font-bold mb-4">LuxuryBath</h3>
```
To update, simply replace "LuxuryBath" with your company name.

#### Hero Section
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 mb-6">
    Bathroom Remodeling Contractors In Florin, CA
</h1>
<p class="text-xl md:text-2xl text-gray-600 mb-10">
    Transform Your Space with Premium Renovation Service
</p>
```
Update location and tagline by modifying the text within these tags.

#### Phone Number
Search for all instances of `8775596432` and replace with your business phone number:
```html
<a href="tel:8775596432">Call (877) 559-6432 Today!</a>
```

### Tailwind CSS Modifications

#### Understanding Responsive Classes
- `md:` prefix = applies on medium screens and up
- `lg:` prefix = applies on large screens and up
- Example:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl">
<!-- text-4xl (mobile) → text-5xl (tablet) → text-6xl (desktop) -->
```

#### Common Tailwind Classes Used
- Text sizes: `text-xl`, `text-2xl`, etc.
- Colors: `text-gray-900`, `bg-blue-600`
- Spacing: `px-6`, `py-4`, `mb-4`
- Flex: `flex`, `items-center`, `justify-between`

## Fixing Broken Links

### Navigation Menu Links
Current internal links in the navigation:
```html
<div class="hidden md:flex space-x-8">
    <a href="#features">Features</a>
    <a href="#benefits">Benefits</a>
    <a href="#faq">FAQ</a>
    <a href="#contact">Contact</a>
</div>
```

To update:
1. For internal sections, keep the `#` prefix
2. Ensure the href matches the section's ID exactly
3. Example: `<a href="#new-section">New Section</a>`

### Social Media Links
Located in the footer:
```html
<div class="flex space-x-4">
    <a href="#" class="text-gray-400 hover:text-white">
        <i class="fab fa-facebook text-2xl"></i>
    </a>
    <!-- Similar for Instagram and Twitter -->
</div>
```

To update:
1. Replace `#` with your social media profile URLs
2. Example: `<a href="https://facebook.com/yourbusiness">`

## Adding Privacy and Terms Pages

### Footer Modification
Add these links to the footer's "Links" section:
```html
<div>
    <h3 class="text-xl font-bold mb-4">Links</h3>
    <ul class="space-y-2">
        <!-- Existing links -->
        <li><a href="privacy.html" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="terms.html" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

### Creating New Pages
1. Create `privacy.html` and `terms.html` in the same directory
2. Copy the header and footer from `index.html`
3. Add your policy content between them
4. Maintain consistent styling using the same Tailwind classes

## Troubleshooting

### Common Issues

1. **Broken Layout**
   - Check for missing closing tags
   - Verify Tailwind CDN link is working
   - Ensure responsive classes are properly ordered

2. **Missing Icons**
   - Verify Font Awesome CDN link is working
   - Check icon class names against [Font Awesome documentation](https://fontawesome.com/icons)

3. **Non-Working Links**
   - Confirm file paths are correct
   - Check for typos in href attributes
   - Verify section IDs match their corresponding links

### Getting Help
- Consult the [Tailwind CSS documentation](https://tailwindcss.com/docs)
- Use browser developer tools (F12) to inspect elements
- Check for console errors

Remember to always test your changes across different screen sizes and browsers before deploying to production.