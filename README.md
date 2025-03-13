# Morris Rental Properties Landing Page - Maintenance Guide

This guide provides detailed instructions for maintaining and customizing the Morris Rental Properties landing page. Whether you're new to web development or need a quick reference, follow these step-by-step instructions.

## Table of Contents
1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Linking Privacy and Terms Pages](#linking-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Header Section
The header contains the company name and navigation menu. To update:

1. **Company Name:**
```html
<!-- Located in header section -->
<a href="/" class="text-2xl font-bold bg-gradient-to-r from-blue-600 to-teal-400 bg-clip-text text-transparent">
    Morris Rentals  <!-- Change this text -->
</a>
```

2. **Navigation Menu Items:**
```html
<div class="hidden md:flex space-x-8">
    <!-- Update text between <a> tags -->
    <a href="#features">Features</a>
    <a href="#benefits">Benefits</a>
    <a href="#faq">FAQ</a>
    <a href="#contact">Contact</a>
</div>
```

### Hero Section
Located at the top of the page:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold leading-tight mb-8 bg-gradient-to-r from-blue-600 to-teal-400 bg-clip-text text-transparent">
    Morris Super Awesome Rental Properties In Fort Lauderdale  <!-- Update main headline -->
</h1>
<p class="text-xl text-gray-600 mb-12">
    Experience the perfect blend of luxury and comfort in our tropical paradise  <!-- Update subheading -->
</p>
```

### Understanding Tailwind Classes
Common classes used in this page:
- `text-[size]`: Controls text size (e.g., `text-xl`, `text-2xl`)
- `font-[weight]`: Controls text weight (e.g., `font-bold`, `font-semibold`)
- `bg-[color]`: Sets background color
- `px-[size]` and `py-[size]`: Sets horizontal and vertical padding
- `mb-[size]`: Sets bottom margin

Example of modifying a button:
```html
<!-- Original -->
<a href="#" class="px-6 py-3 bg-gradient-to-r from-blue-600 to-teal-400">

<!-- Modified for larger size and different colors -->
<a href="#" class="px-8 py-4 bg-gradient-to-r from-purple-600 to-pink-400">
```

## Fixing Broken Links

### Navigation Menu Links
Current internal links in the navigation:
```html
<div class="hidden md:flex space-x-8">
    <a href="#features">Features</a>  <!-- Links to features section -->
    <a href="#benefits">Benefits</a>  <!-- Links to benefits section -->
    <a href="#faq">FAQ</a>           <!-- Links to FAQ section -->
    <a href="#contact">Contact</a>    <!-- Links to contact section -->
</div>
```

To update external links:
1. Locate the booking link:
```html
<a href="https://davidmorrisproperties.com" class="hidden md:inline-block...">
    Book Now
</a>
```
2. Replace `https://davidmorrisproperties.com` with your desired URL

### Email Links
Update email addresses:
```html
<!-- In contact section -->
<a href="mailto:consultingsoftware@proton.me">Contact Us</a>

<!-- In footer -->
<li><a href="mailto:consultingsoftware@proton.me">consultingsoftware@proton.me</a></li>
```

## Linking Privacy and Terms Pages

### Footer Legal Links
Current placeholder links:
```html
<div>
    <h4 class="text-lg font-semibold mb-6">Legal</h4>
    <ul class="space-y-4">
        <li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

To add proper links:
1. Create `privacy.html` and `terms.html` in your project directory
2. Update the links:
```html
<li><a href="privacy.html" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
```

## Troubleshooting

### Common Issues

1. **Broken Internal Links**
   - Ensure section IDs match href attributes
   - Check for typos in IDs
   - Verify sections exist in the document

2. **Responsive Design Issues**
   - Check mobile display using browser dev tools
   - Verify `md:` and `lg:` classes are properly set
   - Test different screen sizes

3. **Gradient Text Not Showing**
   - Ensure all three classes are present:
     ```html
     bg-gradient-to-r from-[color] to-[color] bg-clip-text text-transparent
     ```

### Need Help?
- Review the [Tailwind CSS documentation](https://tailwindcss.com/docs)
- Use browser developer tools to inspect elements
- Test all links after making changes
- Maintain backup copies before making major changes

Remember to test all changes across different devices and browsers to ensure consistency in appearance and functionality.