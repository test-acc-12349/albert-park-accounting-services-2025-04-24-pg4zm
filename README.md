# Albert Park Landing Page - Maintenance Guide

This guide will help you maintain and customize the Albert Park accounting services landing page. Whether you're new to web development or need a quick reference, follow these detailed instructions for common updates.

## Table of Contents
1. [Updating Text and Styling](#updating-text-and-styling)
2. [Managing Links](#managing-links)
3. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains the company name and navigation menu. To update:

1. **Company Name:**
```html
<a href="/" class="text-2xl font-bold bg-gradient-to-r from-purple-400 to-pink-500 bg-clip-text text-transparent">
    Albert Park <!-- Change this text -->
</a>
```

2. **Navigation Menu Items:**
```html
<div class="hidden md:flex space-x-8">
    <a href="#features">Features</a> <!-- Update text here -->
    <a href="#benefits">Benefits</a> <!-- Update text here -->
    <a href="#contact">Contact</a> <!-- Update text here -->
</div>
```

### Hero Section
The main headline and subheading can be modified here:

```html
<h1 class="text-4xl md:text-6xl lg:text-7xl font-bold leading-tight mb-8 bg-gradient-to-r from-purple-400 to-pink-500 bg-clip-text text-transparent">
    Your financial success is our bottom line <!-- Update main headline -->
</h1>
<p class="text-xl md:text-2xl text-gray-300 mb-12">
    Expert accounting services tailored to drive your business forward <!-- Update subheading -->
</p>
```

### Understanding Tailwind Classes
Key classes explained:
- `text-4xl`: Large text size (increases with md: and lg: prefixes)
- `mb-8`: Margin bottom spacing
- `hidden md:flex`: Hidden on mobile, becomes flex on medium screens
- `bg-gray-900`: Dark background color
- `text-gray-300`: Light gray text color

## Managing Links

### Navigation Menu Links
Update these internal section links:
```html
<div class="hidden md:flex space-x-8">
    <a href="#features">Features</a> <!-- Links to features section -->
    <a href="#benefits">Benefits</a> <!-- Links to benefits section -->
    <a href="#contact">Contact</a>   <!-- Links to contact section -->
</div>
```

### Call-to-Action Buttons
Replace the placeholder URL:
```html
<a href="https://theaccountants.com" class="px-8 py-4 bg-gradient-to-r from-purple-500 to-pink-500 rounded-full">
    Get Started Today
</a>
```

### Footer Links
Update service and company links:
```html
<ul class="space-y-2 text-gray-400">
    <li><a href="#" class="hover:text-white transition-colors duration-300">Tax Optimization</a></li>
    <!-- Replace '#' with actual URLs -->
</ul>
```

## Adding Privacy and Terms Pages

1. **Update Footer Links:**
```html
<!-- Find this section in the footer -->
<div>
    <h4 class="text-lg font-semibold mb-4">Legal</h4>
    <ul class="space-y-2 text-gray-400">
        <li><a href="privacy.html" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="terms.html" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

2. **Create New Pages:**
- Create `privacy.html` and `terms.html` in the same directory as `index.html`
- Copy the header and footer from `index.html` to maintain consistent styling
- Add your privacy policy and terms content between the header and footer

## Troubleshooting

### Common Issues:

1. **Broken Internal Links**
- Ensure section IDs match href attributes
- Section IDs should not include the # symbol
- Example: `href="#features"` links to `id="features"`

2. **Responsive Design Issues**
- Check mobile display using browser dev tools
- Verify media query classes (md:, lg:) are correct
- Common classes:
  - `hidden md:flex`: Hidden on mobile, visible on medium screens
  - `text-4xl md:text-6xl`: Different text sizes for different screens

3. **Gradient Text Not Showing**
- Ensure all three classes are present:
  ```html
  bg-gradient-to-r from-purple-400 to-pink-500 bg-clip-text text-transparent
  ```

### Need Help?
- Check the [Tailwind CSS documentation](https://tailwindcss.com/docs)
- Verify HTML syntax using the [W3C Validator](https://validator.w3.org/)
- Test responsiveness at different screen sizes using browser dev tools

Remember to always test changes across different devices and browsers before deploying to production.