# Snow Removal Landing Page - Maintenance Guide

## Table of Contents
- [Updating Text and Styling](#updating-text-and-styling)
- [Managing Links](#managing-links)
- [Adding Policy Pages](#adding-policy-pages)
- [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains your main navigation and company name. To update:

1. Company Name:
```html
<!-- Find this line in the header -->
<h1 class="text-2xl font-bold text-blue-600">Snow Removal Calgary</h1>
```
Simply replace "Snow Removal Calgary" with your company name.

### Hero Section
Located at the top of the page with the main headline:
```html
<h2 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 mb-8 tracking-tight">Professional Snow Removal Services in Calgary</h2>
```
- Update the text between the `<h2>` tags
- The classes explain the styling:
  - `text-4xl`: Large text on mobile
  - `md:text-5xl`: Larger text on medium screens
  - `lg:text-6xl`: Largest text on large screens

### Service Cards
Each service card follows this structure:
```html
<div class="bg-white p-8 rounded-xl shadow-lg hover:shadow-xl transition duration-300">
    <div class="text-blue-600 mb-4">
        <i class="fas fa-bolt text-3xl"></i>
    </div>
    <h3 class="text-xl font-bold text-gray-900 mb-4">Speedy Service</h3>
    <p class="text-gray-600 leading-relaxed">Quick response times...</p>
</div>
```
To modify:
1. Change the icon by updating the `fa-bolt` class to any [Font Awesome](https://fontawesome.com/icons) icon
2. Update the heading text in the `<h3>` tag
3. Modify the description in the `<p>` tag

### Tailwind CSS Tips for Beginners
- Colors: Replace `blue-600` with other colors like `red-600` or `green-600`
- Spacing: Numbers in classes like `p-8` (padding) or `mb-4` (margin-bottom) can be adjusted (0-16)
- Example: Change button color
```html
<!-- Original -->
<a href="#" class="bg-blue-600 text-white">Contact Us</a>
<!-- Modified -->
<a href="#" class="bg-green-600 text-white">Contact Us</a>
```

## Managing Links

### Navigation Menu Links
Current navigation links are:
```html
<a href="#services">Services</a>
<a href="#benefits">Benefits</a>
<a href="#faq">FAQ</a>
<a href="#contact">Contact Us</a>
```

To update:
1. Internal links (same page):
   - Keep the `#` followed by the section ID
   - Example: `href="#services"` jumps to `<section id="services">`

2. External links:
   - Replace `#` with full URL
   - Example: `href="https://your-website.com/services"`

### Call-to-Action Button
Located in the hero section:
```html
<a href="https://snowremoval.com" class="inline-block bg-blue-600">Get Started Today</a>
```
Replace `https://snowremoval.com` with your desired URL.

### Email Link
In the CTA section:
```html
<a href="mailto:iainhmunro@gmail.com">Contact Us Now</a>
```
Replace `iainhmunro@gmail.com` with your business email.

## Adding Policy Pages

### Step 1: Add Footer Links
Add these lines to the Quick Links section in the footer:
```html
<ul class="space-y-2">
    <!-- Existing links -->
    <li><a href="privacy.html" class="text-gray-400 hover:text-white transition duration-300">Privacy Policy</a></li>
    <li><a href="terms.html" class="text-gray-400 hover:text-white transition duration-300">Terms of Service</a></li>
</ul>
```

### Step 2: Create Policy Pages
1. Create two new files:
   - `privacy.html`
   - `terms.html`
2. Use the same header and footer as `index.html`
3. Add your policy content in the main section

Example structure for policy pages:
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <!-- Copy head section from index.html -->
</head>
<body class="font-sans antialiased bg-gray-50">
    <!-- Copy header from index.html -->
    
    <main class="pt-32 pb-24">
        <div class="container mx-auto px-4">
            <h1 class="text-3xl font-bold mb-8">Privacy Policy</h1>
            <!-- Add your policy content here -->
        </div>
    </main>

    <!-- Copy footer from index.html -->
</body>
</html>
```

## Troubleshooting

Common Issues:
1. **Broken Internal Links**
   - Ensure section IDs match exactly with href attributes
   - IDs are case-sensitive

2. **Responsive Design Issues**
   - Check that you've maintained the responsive classes (md: and lg: prefixes)
   - Test on different screen sizes using browser dev tools

3. **Icon Not Showing**
   - Verify Font Awesome CSS is properly loaded
   - Check icon class names against Font Awesome documentation

4. **Styling Not Applied**
   - Confirm Tailwind CSS is properly loaded
   - Check for typos in class names

Need help? Contact your web developer or refer to the [Tailwind CSS documentation](https://tailwindcss.com/docs).