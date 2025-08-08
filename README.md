# Landing Page Maintenance Guide

This guide will help you maintain and customize the Beaumont Castration Services landing page. Whether you're new to web development or need a quick reference, follow these detailed instructions for common updates.

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
<a href="/" class="text-xl font-bold text-blue-900">Beaumont Castration</a>
```
- Replace "Beaumont Castration" with your company name
- Keep the existing classes to maintain styling

2. **Navigation Menu Items:**
```html
<div class="hidden md:flex space-x-8">
    <a href="#services" class="text-gray-700 hover:text-blue-900 transition-colors duration-300">Services</a>
    <!-- Additional menu items -->
</div>
```
- Update text between `>` and `</a>` tags
- Maintain the `href` attributes for proper section linking

### Hero Section
Located at the top of the page:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-blue-900 leading-tight mb-6">
    Trusted Livestock Castration for Southeast Texas Ranchers
</h1>
```
- Update the heading text while keeping the classes
- The `text-4xl md:text-5xl lg:text-6xl` classes control text size across different screen sizes

### Understanding Tailwind Classes
Common classes used in this page:
- `container mx-auto`: Centers content and sets max-width
- `px-6`: Adds horizontal padding
- `py-24`: Adds vertical padding
- `text-gray-600`: Sets text color
- `bg-white`: Sets background color
- `rounded-2xl`: Adds rounded corners
- `shadow-lg`: Adds box shadow

## Managing Links

### Navigation Menu Links
Current internal links:
```html
<a href="#services">Services</a>
<a href="#benefits">Benefits</a>
<a href="#faq">FAQ</a>
<a href="#contact">Contact Us</a>
```
To update:
1. The `#` symbol links to sections within the page
2. Ensure section IDs match these links (e.g., `id="services"`)
3. For external links, replace with full URL:
```html
<a href="https://your-website.com/services">Services</a>
```

### Contact Button
Update the email link:
```html
<a href="mailto:heydud@dudehey.com" class="inline-block px-8 py-4 bg-white text-blue-900 rounded-full">
    Email Us
</a>
```
- Replace `heydud@dudehey.com` with your email address
- Keep all classes to maintain button styling

## Adding Privacy and Terms Pages

### Current Footer Links
```html
<div>
    <h4 class="text-lg font-semibold mb-4">Legal</h4>
    <ul class="space-y-2">
        <li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

To link privacy and terms pages:

1. Create new HTML files:
   - `privacy.html`
   - `terms.html`

2. Update the footer links:
```html
<li><a href="privacy.html" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
```

3. Ensure consistent styling by copying these classes to new page links:
   - `text-gray-400`: Default text color
   - `hover:text-white`: Text color on hover
   - `transition-colors duration-300`: Smooth color transition

## Troubleshooting

### Common Issues and Solutions

1. **Broken Internal Links**
   - Check that section IDs match navigation links exactly
   - Example: `href="#services"` must match `id="services"`

2. **Responsive Design Issues**
   - Look for classes starting with `md:` or `lg:`
   - These control appearance at different screen sizes
   - Example: `text-4xl md:text-5xl lg:text-6xl`

3. **Styling Inconsistencies**
   - Copy existing classes when adding new elements
   - Use browser inspector to view applied styles
   - Maintain the same color scheme:
     - Primary blue: `text-blue-900`
     - Gray text: `text-gray-600`
     - White backgrounds: `bg-white`

### Need Help?
- Use browser developer tools (F12) to inspect elements
- Check Tailwind CSS documentation for class references
- Ensure all HTML tags are properly closed
- Maintain proper indentation for readability

Remember to test all changes across different screen sizes and browsers before publishing updates.