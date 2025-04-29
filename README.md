# Melbourne Web Design Landing Page - Maintenance Guide

This guide will help you maintain and customize the Melbourne Web Design landing page. It's written for beginners and provides step-by-step instructions for common updates.

## Table of Contents
- [Updating Text and Styling](#updating-text-and-styling)
- [Managing Links](#managing-links)
- [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
- [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains the company logo and navigation menu. To update:

1. **Company Logo**
```html
<a href="/" class="text-2xl font-bold text-blue-600">TWD</a>
```
- Replace "TWD" with your company name
- Adjust text size by changing `text-2xl` to `text-xl` (smaller) or `text-3xl` (larger)

2. **Navigation Menu Items**
```html
<div class="hidden md:flex space-x-8">
    <a href="#features" class="text-gray-600 hover:text-blue-600">Features</a>
    <!-- Other menu items -->
</div>
```
- Update text between `<a>` tags
- Keep the `hidden md:flex` class to maintain mobile responsiveness

### Hero Section
Located at the top of the page:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold">
    Melbourne Web Design
</h1>
<p class="text-xl md:text-2xl text-gray-600">
    Best Websites In Melbourne - Crafting Premium Digital Experiences
</p>
```
- Update heading and subheading text
- Maintain responsive text sizes (`text-4xl`, `md:text-5xl`, `lg:text-6xl`)

### Features Cards
Each feature card follows this structure:
```html
<div class="bg-white p-8 rounded-2xl shadow-lg">
    <h3 class="text-xl font-semibold mb-4">Free Hosting</h3>
    <p class="text-gray-600">Premium hosting included...</p>
</div>
```
To modify:
1. Update the heading text in `<h3>` tags
2. Change description text in `<p>` tags
3. Keep the styling classes for consistent design

## Managing Links

### Navigation Links
Current internal links:
```html
<a href="#features">Features</a>
<a href="#benefits">Benefits</a>
<a href="#faq">FAQ</a>
<a href="#contact">Contact</a>
```
To update:
1. Change the `href` value to match your section IDs
2. Ensure section IDs exist in the HTML (e.g., `id="features"`)

### Call-to-Action Buttons
Update these placeholder links:
```html
<a href="https://twd.com" class="inline-block bg-blue-600">
    Start Your Project
</a>
```
Replace `https://twd.com` with your actual URL

### Email Contact
Located in the footer:
```html
<p class="text-gray-400">admin@twd.com</p>
```
Replace with your contact email

## Adding Privacy and Terms Pages

### Step 1: Create New Pages
Create two new files in your project folder:
- `privacy.html`
- `terms.html`

### Step 2: Update Footer Links
Replace these placeholder links:
```html
<div>
    <h4 class="text-lg font-semibold text-white mb-4">Legal</h4>
    <ul class="space-y-2">
        <li><a href="privacy.html" class="hover:text-white">Privacy Policy</a></li>
        <li><a href="terms.html" class="hover:text-white">Terms of Service</a></li>
    </ul>
</div>
```

### Step 3: Maintain Consistent Styling
Copy these classes to maintain consistent link styling:
```html
class="hover:text-white transition-colors duration-300"
```

## Troubleshooting

### Common Issues

1. **Broken Links**
- Check that all `href` attributes point to valid pages or sections
- Verify that section IDs match their corresponding links
- Test all external links (like `https://twd.com`)

2. **Responsive Design Issues**
- Don't remove `md:` or `lg:` prefixes from classes
- Keep the `hidden md:flex` class on the navigation menu
- Maintain responsive text sizes (e.g., `text-4xl md:text-5xl lg:text-6xl`)

3. **Styling Problems**
- Ensure Tailwind CSS CDN is properly loaded
- Keep the font import for 'Inter' in the head section
- Maintain the structure of utility classes in elements

### Need Help?
- Check the [Tailwind CSS documentation](https://tailwindcss.com/docs)
- Verify HTML syntax using the [W3C Validator](https://validator.w3.org/)
- Test responsive design using browser developer tools

Remember to always test your changes across different devices and screen sizes before publishing updates.