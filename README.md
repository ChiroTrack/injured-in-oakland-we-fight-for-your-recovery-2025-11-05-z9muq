# Pre Chiropractic Landing Page - Maintenance & Customization Guide

Welcome! This comprehensive guide will help you maintain and customize your Pre Chiropractic landing page. Whether you're updating text, fixing links, or adding new pages, we'll walk you through each step with clear, beginner-friendly instructions.

---

## Table of Contents

1. [Understanding the Page Structure](#understanding-the-page-structure)
2. [Updating Text Content](#updating-text-content)
3. [Modifying Tailwind CSS Classes](#modifying-tailwind-css-classes)
4. [Fixing and Managing Links](#fixing-and-managing-links)
5. [Linking Privacy and Terms Pages](#linking-privacy-and-terms-pages)
6. [Troubleshooting Common Issues](#troubleshooting-common-issues)
7. [Best Practices](#best-practices)

---

## Understanding the Page Structure

Before making changes, let's understand how your landing page is organized:

### Main Sections

Your `index.html` file contains these key sections:

| Section | Purpose | Starts With |
|---------|---------|------------|
| **Header Navigation** | Sticky menu at top | `<header>` tag |
| **Hero Section** | Main banner with headline | `id="features"` reference area |
| **Features Section** | Three service cards | `id="features"` |
| **Benefits Section** | Why choose us | `id="benefits"` |
| **CTA Section** | Call-to-action banner | Background image section |
| **Testimonials** | Client reviews | `id="testimonials"` |
| **About Us** | Company information | `id="about"` |
| **FAQ Section** | Frequently asked questions | `id="faq"` |
| **Final CTA** | Last call-to-action | Gradient background |
| **Footer** | Contact & links | `<footer>` tag |

### File Organization Recommendation

Create this folder structure for your website:

```
your-website/
├── index.html (main landing page)
├── privacy.html (privacy policy)
├── terms.html (terms of service)
├── blog.html (blog page)
├── css/
│   └── custom.css (optional custom styles)
├── js/
│   └── custom.js (optional custom scripts)
└── images/
    └── (your images here)
```

---

## Updating Text Content

### 1. Changing the Company Name

Your company name appears in multiple locations. Here's how to update each one:

#### Location 1: Header Logo Text
**Find this code in the `<header>` section (line ~50):**

```html
<span class="text-2xl font-bold gradient-text">Pre Chiropractic</span>
```

**To change it:**
- Replace `Pre Chiropractic` with your company name
- Example: `<span class="text-2xl font-bold gradient-text">Recovery Plus Legal</span>`

#### Location 2: Footer Logo Text
**Find this code in the `<footer>` section (line ~650):**

```html
<span class="text-xl font-bold gradient-text">Pre Chiropractic</span>
```

**To change it:**
- Replace `Pre Chiropractic` with your company name
- Keep the `gradient-text` class to maintain the purple-to-pink color effect

#### Location 3: Page Title (Browser Tab)
**Find this code in the `<head>` section (line ~10):**

```html
<title>Injured in Oakland? We Fight For Your Recovery | Pre Chiropractic</title>
```

**To change it:**
- Replace the entire text with your desired title
- Example: `<title>Personal Injury Lawyer Oakland | Recovery Plus Legal</title>`
- Keep it under 60 characters for best display in search results

#### Location 4: Meta Description
**Find this code in the `<head>` section (line ~8):**

```html
<meta name="description" content="Oakland personal injury lawyer specializing in car accidents and rehabilitation. Maximized compensation with no upfront costs.">
```

**To change it:**
- Update the `content=""` attribute with your description
- Keep it between 150-160 characters for optimal search engine display
- Example: `content="Expert personal injury attorney in Oakland. Free consultation, no upfront costs. Specializing in car accidents and rehabilitation."`

#### Location 5: Meta Author
**Find this code in the `<head>` section (line ~11):**

```html
<meta name="author" content="Pre Chiropractic">
```

**To change it:**
- Replace `Pre Chiropractic` with your company name

### 2. Updating Hero Section Headlines

#### Main Headline
**Find this code (line ~115):**

```html
<h1 class="text-5xl md:text-6xl lg:text-7xl font-black leading-tight tracking-tight">
    Injured in Oakland? <span class="gradient-text">We Fight For Your Recovery.</span>
</h1>
```

**To change it:**
- Replace the text before `<span>` with your main headline
- Replace the text inside `<span class="gradient-text">...</span>` with the highlighted portion
- The text in the `<span>` will appear in the purple-to-pink gradient color
- Example:
```html
<h1 class="text-5xl md:text-6xl lg:text-7xl font-black leading-tight tracking-tight">
    Hurt in an accident? <span class="gradient-text">Get the compensation you deserve.</span>
</h1>
```

#### Hero Subheadline
**Find this code (line ~120):**

```html
<p class="text-xl md:text-2xl text-gray-300 leading-relaxed font-light">
    Don't let a car accident define your future. We provide comprehensive legal support and advanced rehabilitation services to maximize your compensation and restore your quality of life.
</p>
```

**To change it:**
- Replace the paragraph text with your message
- Keep the classes (`text-xl md:text-2xl text-gray-300 leading-relaxed font-light`) for proper styling
- Example:
```html
<p class="text-xl md:text-2xl text-gray-300 leading-relaxed font-light">
    From initial consultation to full recovery, we handle every detail of your case. Our integrated approach combines expert legal representation with cutting-edge rehabilitation.
</p>
```

### 3. Updating Feature Cards (Services Section)

Your page has three feature cards. Here's how to update each one:

#### Feature Card 1: Legal Referral Network
**Find this section (line ~175):**

```html
<div class="card-hover bg-gradient-to-br from-gray-700 to-gray-800 p-8 rounded-xl border border-gray-600 hover:border-purple-500">
    <div class="w-16 h-16 bg-gradient-to-r from-purple-600 to-pink-600 rounded-lg flex items-center justify-center mb-6">
        <i class="fas fa-gavel text-2xl text-white"></i>
    </div>
    <h3 class="text-2xl font-bold mb-4">Legal Referral Network</h3>
    <p class="text-gray-300 leading-relaxed mb-6">
        Connect with experienced personal injury attorneys...
    </p>
```

**To change the icon:**
- Replace `fas fa-gavel` with a different Font Awesome icon
- Common options: `fas fa-scale-balanced`, `fas fa-briefcase`, `fas fa-handshake`
- Visit [fontawesome.com](https://fontawesome.com/icons) to find more icons

**To change the title:**
- Replace `Legal Referral Network` with your title
- Example: `Expert Attorney Connections`

**To change the description:**
- Replace the paragraph text while keeping the classes
- Example:
```html
<p class="text-gray-300 leading-relaxed mb-6">
    We connect you with the region's top personal injury attorneys who understand California law and insurance tactics. Our partners have recovered over $50 million for injured clients.
</p>
```

**To update the bullet points:**
**Find this section in the same card (line ~190):**

```html
<ul class="space-y-3">
    <li class="flex items-center text-gray-200">
        <i class="fas fa-check text-green-500 mr-3"></i>
        Expert accident attorneys
    </li>
    <li class="flex items-center text-gray-200">
        <i class="fas fa-check text-green-500 mr-3"></i>
        Proven track record
    </li>
    <li class="flex items-center text-gray-200">
        <i class="fas fa-check text-green-500 mr-3"></i>
        Full case coordination
    </li>
</ul>
```

**To change bullet points:**
- Replace the text after each `<i>` tag with your bullet point
- Keep the `<i class="fas fa-check text-green-500 mr-3"></i>` for the checkmark
- Example:
```html
<ul class="space-y-3">
    <li class="flex items-center text-gray-200">
        <i class="fas fa-check text-green-500 mr-3"></i>
        25+ years combined experience
    </li>
    <li class="flex items-center text-gray-200">
        <i class="fas fa-check text-green-500 mr-3"></i>
        98% settlement success rate
    </li>
    <li class="flex items-center text-gray-200">
        <i class="fas fa-check text-green-500 mr-3"></i>
        Bilingual representation available
    </li>
</ul>
```

#### Feature Cards 2 & 3
Follow the same process for the other two cards:
- **Feature 2** starts around line ~205 (Advanced Rehabilitation)
- **Feature 3** starts around line ~235 (No Upfront Costs)

### 4. Updating Benefits Section

**Find the section heading (line ~265):**

```html
<h2 class="text-4xl md:text-5xl font-black mb-4 tracking-tight">
    Why Choose <span class="gradient-text">Pre Chiropractic?</span>
</h2>
```

**To change it:**
- Replace text before `<span>` with your heading
- Replace text inside `<span class="gradient-text">...</span>` with highlighted portion
- Example:
```html
<h2 class="text-4xl md:text-5xl font-black mb-4 tracking-tight">
    The <span class="gradient-text">Complete Recovery Solution</span>
</h2>
```

**Update benefit descriptions (lines ~290-310):**

Each benefit has an icon, title, and description. To update:

```html
<div class="text-center">
    <div class="inline-flex items-center justify-center w-20 h-20 bg-gradient-to-r from-purple-600 to-pink-600 rounded-full mb-6">
        <i class="fas fa-chart-line text-3xl text-white"></i>
    </div>
    <h3 class="text-2xl font-bold mb-4">Maximized Compensation</h3>
    <p class="text-gray-300 leading-relaxed">
        Our legal partners work tirelessly...
    </p>
</div>
```

- Change the icon (e.g., `fas fa-chart-line`)
- Change the title (e.g., `Maximized Compensation`)
- Change the description paragraph

### 5. Updating Testimonials

**Find testimonials section (line ~370):**

Each testimonial card contains:

```html
<div class="card-hover bg-gradient-to-br from-gray-700 to-gray-800 p-6 rounded-xl border border-gray-600">
    <div class="flex items-center mb-4">
        <i class="fas fa-star text-yellow-400"></i>
        <i class="fas fa-star text-yellow-400"></i>
        <i class="fas fa-star text-yellow-400"></i>
        <i class="fas fa-star text-yellow-400"></i>
        <i class="fas fa-star text-yellow-400"></i>
    </div>
    <p class="text-gray-300 mb-4 leading-relaxed">
        "After my car accident, I was overwhelmed..."
    </p>
    <div class="border-t border-gray-600 pt-4">
        <p class="font-bold text-white">Maria Rodriguez</p>
        <p class="text-sm text-gray-400">Oakland, CA</p>
    </div>
</div>
```

**To update a testimonial:**

1. **Change the star rating** (1-5 stars):
   - Add or remove `<i class="fas fa-star text-yellow-400"></i>` lines
   - 5 lines = 5-star review, 4 lines = 4-star review, etc.

2. **Change the testimonial text:**
   - Replace the quoted text with your client's review
   - Keep the quotation marks

3. **Change the client name:**
   - Replace `Maria Rodriguez` with the actual name

4. **Change the location:**
   - Replace `Oakland, CA` with the client's location

**Example of a complete updated testimonial:**

```html
<div class="card-hover bg-gradient-to-br from-gray-700 to-gray-800 p-6 rounded-xl border border-gray-600">
    <div class="flex items-center mb-4">
        <i class="fas fa-star text-yellow-400"></i>
        <i class="fas fa-star text-yellow-400"></i>
        <i class="fas fa-star text-yellow-400"></i>
        <i class="fas fa-star text-yellow-400"></i>
        <i class="fas fa-star text-yellow-400"></i>
    </div>
    <p class="text-gray-300 mb-4 leading-relaxed">
        "The team handled everything professionally. My case was resolved quickly and I received fair compensation. Highly recommended!"
    </p>
    <div class="border-t border-gray-600 pt-4">
        <p class="font-bold text-white">John Smith</p>
        <p class="text-sm text-gray-400">Oakland, CA</p>
    </div>
</div>
```

### 6. Updating About Section

**Find the About heading (line ~440):**

```html
<h2 class="text-4xl md:text-5xl font-black mb-4 tracking-tight">
    About <span class="gradient-text">Pre Chiropractic</span>
</h2>
```

**To change it:**
- Replace `Pre Chiropractic` with your company name
- Example:
```html
<h2 class="text-4xl md:text-5xl font-black mb-4 tracking-tight">
    About <span class="gradient-text">Recovery Plus Legal</span>
</h2>
```

**Update the company story (lines ~450-465):**

```html
<p>
    Founded in 2015, Pre Chiropractic was born from a simple mission...
</p>
```

**To change it:**
- Replace the entire paragraph with your company's story
- Keep the same structure (2-3 paragraphs work best)
- Example:
```html
<p>
    Founded in 2012, Recovery Plus Legal emerged from a simple vision: to provide injured individuals with seamless access to expert legal representation and advanced rehabilitation services. Our founder, Attorney Michael Torres, recognized that most injury victims faced a fragmented system where lawyers and doctors worked independently. He created an integrated model that revolutionized how people recover after accidents.
</p>

<p>
    Today, we've helped over 3,000 clients recover fully and receive fair compensation. Our commitment to excellence, integrity, and client satisfaction has made us the trusted choice for personal injury recovery in the Bay Area. We believe every injured person deserves compassionate care, expert representation, and financial security during their recovery journey.
</p>
```

**Update the statistics (lines ~475-485):**

```html
<div class="grid grid-cols-1 md:grid-cols-3 gap-8 mt-16 pt-16 border-t border-gray-700">
    <div class="text-center">
        <div class="text-4xl font-black gradient-text mb-2">5000+</div>
        <p class="text-gray-300">Clients Successfully Recovered</p>
    </div>
    <div class="text-center">
        <div class="text-4xl font-black gradient-text mb-2">$50M+</div>
        <p class="text-gray-300">In Settlements Recovered</p>
    </div>
    <div class="text-center">
        <div class="text-4xl font-black gradient-text mb-2">98%</div>
        <p class="text-gray-300">Client Satisfaction Rate</p>
    </div>
</div>
```

**To update statistics:**
- Replace the number (e.g., `5000+`) with your actual number
- Replace the description (e.g., `Clients Successfully Recovered`) with your metric
- Example:
```html
<div class="text-center">
    <div class="text-4xl font-black gradient-text mb-2">3000+</div>
    <p class="text-gray-300">Cases Successfully Resolved</p>
</div>
```

### 7. Updating FAQ Section

**Find the FAQ heading (line ~500):**

```html
<h2 class="text-4xl md:text-5xl font-black mb-4 tracking-tight">
    Frequently Asked <span class="gradient-text">Questions</span>
</h2>
```

**To update individual FAQ items (starting line ~520):**

Each FAQ item has this structure:

```html
<div class="faq-item bg-gradient-to-br from-gray-700 to-gray-800 rounded-xl border border-gray-600 overflow-hidden">
    <button class="faq-question w-full px-6 py-6 flex items-center justify-between hover:bg-gray-700 hover:bg-opacity-50 transition-all duration-300 cursor-pointer text-left">
        <span class="text-lg font-bold">How much does your service cost?</span>
        <i class="faq-icon fas fa-chevron-down text-purple-400 transition-transform duration-300"></i>
    </button>
    <div class="faq-answer hidden px-6 pb-6">
        <p class="text-gray-300 leading-relaxed">
            Pre Chiropractic operates on a completely free consultation basis...
        </p>
    </div>
</div>
```

**To update a question:**
- Replace the text inside `<span class="text-lg font-bold">...</span>`
- Example: `<span class="text-lg font-bold">What qualifications do your attorneys have?</span>`

**To update an answer:**
- Replace the text inside `<p class="text-gray-300 leading-relaxed">...</p>`
- You can use multiple paragraphs if needed
- Example:
```html
<div class="faq-answer hidden px-6 pb-6">
    <p class="text-gray-300 leading-relaxed mb-4">
        All our attorneys are licensed in California and have a minimum of 10 years experience in personal injury law.
    </p>
    <p class="text-gray-300 leading-relaxed">
        Many are members of the State Bar Association and have received awards for their legal work.
    </p>
</div>
```

### 8. Updating Contact Information

**Find contact info in the footer (lines ~650-680):**

```html
<li class="flex items-start space-x-3">
    <i class="fas fa-envelope text-purple-500 mt-1"></i>
    <div>
        <p class="text-sm text-gray-400">Email</p>
        <a href="mailto:prechiropractic@gmail.com" class="text-white hover:text-purple-400 transition-colors duration-300">prechiropractic@gmail.com</a>
    </div>
</li>
```

**To update email:**
- Replace `prechiropractic@gmail.com` in BOTH places (the href and the displayed text)
- Example:
```html
<a href="mailto:contact@recoveryplus.com" class="text-white hover:text-purple-400 transition-colors duration-300">contact@recoveryplus.com</a>
```

**To update location:**
- Find and replace `Oakland, California` with your city
- Example: `San Francisco, California`

**To update business hours:**
- Find this code:
```html
<li class="flex items-start space-x-3">
    <i class="fas fa-clock text-purple-500 mt-1"></i>
    <div>
        <p class="text-sm text-gray-400">Hours</p>
        <p class="text-white">Mon-Fri: 9AM-6PM</p>
    </div>
</li>
```

- Replace `Mon-Fri: 9AM-6PM` with your actual hours
- Example: `Mon-Fri: 8AM-7PM, Sat: 10AM-4PM`

---

## Modifying Tailwind CSS Classes

Tailwind CSS is a utility-first framework that uses classes to style elements. This landing page uses Tailwind extensively. Here's how to modify styling while maintaining responsive design.

### Understanding Tailwind Classes

Tailwind classes follow this pattern: `property-value-breakpoint`

**Example:** `text-2xl md:text-3xl lg:text-4xl`

- `text-2xl` = text size on mobile (all screens)
- `md:text-3xl` = text size on medium screens and up (768px+)
- `lg:text-4xl` = text size on large screens and up (1024px+)

### Common Tailwind Classes Used in This Page

#### Text Sizes
```
text-sm    = Small text (14px)
text-base  = Normal text (16px)
text-lg    = Large text (18px)
text-xl    = Extra large (20px)
text-2xl   = 2x large (24px)
text-4xl   = 4x large (36px)
text-5xl   = 5x large (48px)
text-6xl   = 6x large (60px)
text-7xl   = 7x large (80px)
```

#### Text Colors
```
text-white      = White text
text-gray-300   = Light gray text
text-gray-400   = Medium-light gray
text-gray-500   = Medium gray
text-gray-900   = Dark gray/black
text-purple-400 = Light purple
text-green-500  = Green
text-yellow-400 = Yellow
```

#### Background Colors
```
bg-gray-900     = Very dark gray background
bg-gray-800     = Dark gray background
bg-gray-700     = Medium-dark gray
bg-purple-600   = Purple background
bg-pink-600     = Pink background
bg-white        = White background
```

#### Spacing (Padding & Margin)
```
p-4   = 16px padding on all sides
px-8  = 32px padding left and right
py-4  = 16px padding top and bottom
m-4   = 16px margin on all sides
mb-4  = 16px margin bottom
mt-1  = 4px margin top
space-y-3 = 12px space between vertical elements
```

#### Font Styling
```
font-light  = Thin/light weight
font-bold   = Bold text
font-black  = Extra bold text
leading-relaxed = Increased line spacing
tracking-tight  = Reduced letter spacing
```

#### Borders
```
border          = 1px border
border-2        = 2px border
border-gray-600 = Gray border color
rounded-lg      = Rounded corners (medium)
rounded-xl      = Rounded corners (large)
rounded-full    = Completely rounded (circle)
```

### How to Change Colors

#### Example 1: Change Hero Section Background

**Find this code (line ~100):**

```html
<section class="relative overflow-hidden bg-gradient-to-br from-gray-900 via-gray-800 to-gray-900 pt-20 pb-32 md:pt-32 md:pb-48">
```

**Current gradient:** `bg-gradient-to-br from-gray-900 via-gray-800 to-gray-900` (dark gray gradient)

**To change to a blue gradient:**

```html
<section class="relative overflow-hidden bg-gradient-to-br from-blue-900 via-blue-800 to-blue-900 pt-20 pb-32 md:pt-32 md:pb-48">
```

**To change to a green gradient:**

```html
<section class="relative overflow-hidden bg-gradient-to-br from-green-900 via-green-800 to-green-900 pt-20 pb-32 md:pt-32 md:pb-48">
```

**Color options:**
- `gray-900`, `blue-900`, `purple-900`, `pink-900`, `red-900`, `green-900`, `indigo-900`, `yellow-900`

#### Example 2: Change Button Colors

**Find the primary button class (lines ~30-32):**

```css
.btn-primary {
    @apply px-8 py-4 bg-gradient-to-r from-purple-600 to-pink-600 text-white font-bold rounded-lg hover:shadow-lg hover:scale-105 transition-all duration-300 cursor-pointer;
}
```

**To change to a blue-to-cyan gradient:**

```css
.btn-primary {
    @apply px-8 py-4 bg-gradient-to-r from-blue-600 to-cyan-600 text-white font-bold rounded-lg hover:shadow-lg hover:scale-105 transition-all duration-300 cursor-pointer;
}
```

**To change to a solid green:**

```css
.btn-primary {
    @apply px-8 py-4 bg-green-600 text-white font-bold rounded-lg hover:shadow-lg hover:scale-105 transition-all duration-300 cursor-pointer;
}
```

### How to Change Text Size

#### Example: Make Hero Headline Larger

**Find this code (line ~115):**

```html
<h1 class="text-5xl md:text-6xl lg:text-7xl font-black leading-tight tracking-tight">
```

**Current sizes:**
- Mobile: `text-5xl` (48px)
- Tablet (768px+): `md:text-6xl` (60px)
- Desktop (1024px+): `lg:text-7xl` (80px)

**To make it even larger:**

```html
<h1 class="text-6xl md:text-7xl lg:text-8xl font-black leading-tight tracking-tight">
```

**To make it smaller:**

```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-black leading-tight tracking-tight">
```

### How to Change Spacing

#### Example: Increase Padding in Feature Cards

**Find this code (line ~175):**

```html
<div class="card-hover bg-gradient-to-br from-gray-700 to-gray-800 p-8 rounded-xl border border-gray-600 hover:border-purple-500">
```

**Current padding:** `p-8` (32px on all sides)

**To increase padding:**

```html
<div class="card-hover bg-gradient-to-br from-gray-700 to-gray-800 p-12 rounded-xl border border-gray-600 hover:border-purple-500">
```

**To decrease padding:**

```html
<div class="card-hover bg-gradient-to-br from-gray-700 to-gray-800 p-6 rounded-xl border border-gray-600 hover:border-purple-500">
```

**Padding values:** `p-2`, `p-4`, `p-6`, `p-8`, `p-10`, `p-12`, `p-16`

### How to Change Responsive Behavior

#### Example: Stack on Different Screen Sizes

**Find this code (line ~111):**

```html
<div class="grid grid-cols-1 lg:grid-cols-2 gap-12 items-center">
```

**Current behavior:**
- Mobile (all screens): `grid-cols-1` (1 column)
- Large screens (1024px+): `lg:grid-cols-2` (2 columns)

**To change to 3 columns on large screens:**

```html
<div class="grid grid-cols-1 lg:grid-cols-3 gap-12 items-center">
```

**To add a tablet breakpoint (2 columns on tablet):**

```html
<div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-12 items-center">
```

**Breakpoints:**
- No prefix = mobile (all screens)
- `sm:` = small screens (640px+)
- `md:` = medium screens (768px+)
- `lg:` = large screens (1024px+)
- `xl:` = extra large (1280px+)
- `2xl:` = 2x extra large (1536px+)

### How to Change Border Radius (Rounded Corners)

#### Example: Make Cards More Rounded

**Find this code (line ~175):**

```html
<div class="card-hover bg-gradient-to-br from-gray-700 to-gray-800 p-8 rounded-xl border border-gray-600 hover:border-purple-500">
```

**Current border radius:** `rounded-xl` (medium-large rounded corners)

**To make corners less rounded:**

```html
<div class="card-hover bg-gradient-to-br from-gray-700 to-gray-800 p-8 rounded-lg border border-gray-600 hover:border-purple-500">
```

**To make corners more rounded:**

```html
<div class="card-hover bg-gradient-to-br from-gray-700 to-gray-800 p-8 rounded-2xl border border-gray-600 hover:border-purple-500">
```

**Border radius options:**
- `rounded-none` = no rounding
- `rounded-sm` = slight rounding
- `rounded` = standard rounding
- `rounded-lg` = large rounding
- `rounded-xl` = extra large rounding
- `rounded-2xl` = 2x extra large
- `rounded-3xl` = 3x extra large
- `rounded-full` = completely rounded (circle/pill shape)

### Creating Custom Styles

If you need styling that Tailwind doesn't provide, use the `<style>` section in the `<head>` (lines ~25-45).

#### Example: Add a Custom Animation

**Add this to the `<style>` section:**

```css
@keyframes slideInFromLeft {
    from {
        opacity: 0;
        transform: translateX(-100px);
    }
    to {
        opacity: 1;
        transform: translateX(0);
    }
}

.slide-in {
    animation: slideInFromLeft 0.6s ease-out;
}
```

**Then use it in your HTML:**

```html
<h1 class="slide-in text-5xl md:text-6xl lg:text-7xl font-black leading-tight tracking-tight">
    Your Headline Here
</h1>
```

---

## Fixing and Managing Links

Links are crucial for navigation and user engagement. Let's cover all the links in your page and how to manage them.

### Types of Links in Your Page

1. **Navigation Links** - Links in the header menu
2. **Internal Links** - Links to sections within the same page (using #)
3. **External Links** - Links to other websites
4. **Email Links** - Links that open email client
5. **CTA Links** - Call-to-action buttons
6. **Footer Links** - Links in the footer section

### Understanding Link Structure

A basic link looks like this:

```html
<a href="destination" target="_blank" class="styling">Link Text</a>
```

- `href=""` = where the link goes
- `target="_blank"` = opens in new tab (optional)
- `class=""` = styling
- `Link Text` = what the user sees

### Current Links in Your Page

#### Navigation Links (Header Menu)

**Find these in the desktop menu (lines ~55-63):**

```html
<a href="#features" class="text-gray-300 hover:text-white transition-colors duration-300">Services</a>
<a href="#benefits" class="text-gray-300 hover:text-white transition-colors duration-300">Benefits</a>
<a href="#testimonials" class="text-gray-300 hover:text-white transition-colors duration-300">Testimonials</a>
<a href="#faq" class="text-gray-300 hover:text-white transition-colors duration-300">FAQ</a>
<a href="#about" class="text-gray-300 hover:text-white transition-colors duration-300">About</a>
<a href="https://app.acuityscheduling.com/schedule.php?owner=13033735" target="_blank" class="btn-primary">Schedule Now</a>
```

**These links are:**
- `#features` = jumps to Features section
- `#benefits` = jumps to Benefits section
- `#testimonials` = jumps to Testimonials section
- `#faq` = jumps to FAQ section
- `#about` = jumps to About section
- Acuity Scheduling link = external booking system

#### Mobile Menu Links

**Find these in the mobile menu (lines ~70-77):**

Same links as desktop menu - keep them synchronized.

#### CTA Button Links

**Find in hero section (line ~126):**

```html
<a href="https://app.acuityscheduling.com/schedule.php?owner=13033735" target="_blank" class="btn-primary text-center">
    <i class="fas fa-calendar-check mr-2"></i>Schedule Your Free Consultation
</a>
```

**This is your main booking link** - appears multiple times throughout the page.

#### Footer Links

**Find in footer (lines ~630-645):**

```html
<a href="#features" class="text-gray-400 hover:text-white transition-colors duration-300">Our Services</a>
<a href="#benefits" class="text-gray-400 hover:text-white transition-colors duration-300">Benefits</a>
<a href="#testimonials" class="text-gray-400 hover:text-white transition-colors duration-300">Testimonials</a>
<a href="#faq" class="text-gray-400 hover:text-white transition-colors duration-300">FAQ</a>
<a href="#about" class="text-gray-400 hover:text-white transition-colors duration-300">About Us</a>
```

**Policy links (lines ~650-653):**

```html
<a href="privacy.html" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a>
<a href="terms.html" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a>
<a href="blog.html" class="text-gray-400 hover:text-white transition-colors duration-300">Blog</a>
<a href="https://app.acuityscheduling.com/schedule.php?owner=13033735" target="_blank" class="text-gray-400 hover:text-white transition-colors duration-300">Schedule Appointment</a>
```

#### Contact Links

**Email link (line ~668):**

```html
<a href="mailto:prechiropractic@gmail.com" class="text-white hover:text-purple-400 transition-colors duration-300">prechiropractic@gmail.com</a>
```

**Social media links (lines ~625-640):**

```html
<a href="#" class="w-10 h-10 bg-gray-800 rounded-lg flex items-center justify-center text-gray-400 hover:text-white hover:bg-purple-600 transition-all duration-300">
    <i class="fab fa-facebook-f"></i>
</a>
```

### How to Update Links

#### Step 1: Update Your Booking Link

Your Acuity Scheduling link appears in **5 locations**:

1. **Header desktop menu** (line ~62)
2. **Header mobile menu** (line ~76)
3. **Hero section button** (line ~126)
4. **CTA section** (line ~335)
5. **Footer** (line ~654)
6. **Final CTA section** (line ~700)

**To update all at once:**

1. Open your `index.html` file
2. Use Find & Replace (Ctrl+H or Cmd+H)
3. Find: `https://app.acuityscheduling.com/schedule.php?owner=13033735`
4. Replace with: `YOUR_NEW_BOOKING_LINK`
5. Click "Replace All"

**Where to get your booking link:**

- If using Acuity Scheduling: Log in, go to Settings → Embed, copy your scheduling link
- If using Calendly: Go to Settings → Share, copy your booking link
- If using another service: Copy the link from your service

#### Step 2: Update Email Links

**Find the email link (line ~668):**

```html
<a href="mailto:prechiropractic@gmail.com" class="text-white hover:text-purple-400 transition-colors duration-300">prechiropractic@gmail.com</a>
```

**To change it:**

1. Replace `prechiropractic@gmail.com` in the `href` attribute
2. Replace `prechiropractic@gmail.com` in the visible text
3. Example:
```html
<a href="mailto:contact@mycompany.com" class="text-white hover:text-purple-400 transition-colors duration-300">contact@mycompany.com</a>
```

**Also update the email in the final CTA section (line ~700):**

```html
<a href="mailto:prechiropractic@gmail.com" class="btn-secondary">
    <i class="fas fa-envelope mr-2"></i>Email Us
</a>
```

#### Step 3: Update Social Media Links

**Find social media links in footer (lines ~625-640):**

```html
<a href="#" class="w-10 h-10 bg-gray-800 rounded-lg flex items-center justify-center text-gray-400 hover:text-white hover:bg-purple-600 transition-all duration-300">
    <i class="fab fa-facebook-f"></i>
</a>
```

**To add your Facebook page:**

```html
<a href="https://facebook.com/your-page-name" target="_blank" class="w-10 h-10 bg-gray-800 rounded-lg flex items-center justify-center text-gray-400 hover:text-white hover:bg-purple-600 transition-all duration-300">
    <i class="fab fa-facebook-f"></i>
</a>
```

**To add your Twitter:**

```html
<a href="https://twitter.com/your-handle" target="_blank" class="w-10 h-10 bg-gray-800 rounded-lg flex items-center justify-center text-gray-400 hover:text-white hover:bg-purple-600 transition-all duration-300">
    <i class="fab fa-twitter"></i>
</a>
```

**To add your LinkedIn:**

```html
<a href="https://linkedin.com/company/your-company" target="_blank" class="w-10 h-10 bg-gray-800 rounded-lg flex items-center justify-center text-gray-400 hover:text-white hover:bg-purple-600 transition-all duration-300">
    <i class="fab fa-linkedin-in"></i>
</a>
```

**To add your Instagram:**

```html
<a href="https://instagram.com/your-handle" target="_blank" class="w-10 h-10 bg-gray-800 rounded-lg flex items-center justify-center text-gray-400 hover:text-white hover:bg-purple-600 transition-all duration-300">
    <i class="fab fa-instagram"></i>
</a>
```

**Key points:**
- Add `target="_blank"` to open in new tab
- Replace `#` with your actual social media URL
- Keep the Font Awesome icon class matching the social platform

#### Step 4: Verify Internal Links Work

Your internal links use the `#` symbol to jump to sections:

- `#features` → jumps to Features section
- `#benefits` → jumps to Benefits section
- `#testimonials` → jumps to Testimonials section
- `#faq` → jumps to FAQ section
- `#about` → jumps to About section

**These work because each section has a matching `id` attribute:**

```html
<section id="features" class="...">
<section id="benefits" class="...">
<section id="testimonials" class="...">
<section id="faq" class="...">
<section id="about" class="...">
```

**If a link isn't working:**

1. Check that the section has the correct `id`
2. Check that the link uses the exact same name as the `id`
3. Example: Link `href="#services"` must match `id="services"`

### Testing Links

After updating links:

1. **Open your page in a browser**
2. **Test each link:**
   - Click navigation links - they should scroll to each section
   - Click "Schedule Now" - should open booking page in new tab
   - Click email link - should open your email client
   - Click social media icons - should open in new tab
   - Click footer links - should work correctly

---

## Linking Privacy and Terms Pages

Your landing page references privacy and terms pages that don't exist yet. Let's create them and link them properly.

### Step 1: Create the Privacy Policy Page

**Create a new file called `privacy.html` in your website folder:**

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Privacy Policy for Pre Chiropractic">
    <meta name="author" content="Pre Chiropractic">
    <title>Privacy Policy | Pre Chiropractic</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        html {
            scroll-behavior: smooth;
        }
        
        .gradient-text {
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }
    </style>
</head>
<body class="bg-gray-900 text-white">
    <!-- Header Navigation (Same as index.html) -->
    <header class="sticky top-0 z-50 bg-gray-900 bg-opacity-95 backdrop-blur-md border-b border-gray-800">
        <nav class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-4 flex items-center justify-between">
            <div class="flex items-center space-x-2">
                <div class="w-10 h-10 bg-gradient-to-r from-purple-600 to-pink-600 rounded-lg flex items-center justify-center">
                    <i class="fas fa-heartbeat text-white text-xl"></i>
                </div>
                <a href="index.html" class="text-2xl font-bold gradient-text">Pre Chiropractic</a>
            </div>
            
            <div class="hidden md:flex items-center space-x-8">
                <a href="index.html#features" class="text-gray-300 hover:text-white transition-colors duration-300">Services</a>
                <a href="index.html#benefits" class="text-gray-300 hover:text-white transition-colors duration-300">Benefits</a>
                <a href="index.html#testimonials" class="text-gray-300 hover:text-white transition-colors duration-300">Testimonials</a>
                <a href="index.html#faq" class="text-gray-300 hover:text-white transition-colors duration-300">FAQ</a>
                <a href="index.html#about" class="text-gray-300 hover:text-white transition-colors duration-300">About</a>
            </div>
        </nav>
    </header>

    <!-- Main Content -->
    <section class="py-24 bg-gray-900">
        <div class="max-w-4xl mx-auto px-4 sm:px-6 lg:px-8">
            <h1 class="text-5xl md:text-6xl font-black mb-12 tracking-tight">
                <span class="gradient-text">Privacy Policy</span>
            </h1>
            
            <div class="prose prose-invert max-w-none space-y-8 text-gray-300">
                <div>
                    <h2 class="text-3xl font-bold text-white mb-4">1. Information We Collect</h2>
                    <p>
                        Pre Chiropractic collects information you provide directly to us, such as when you:
                    </p>
                    <ul class="list-disc list-inside space-y-2 ml-4">
                        <li>Schedule a consultation</li>
                        <li>Contact us via email or phone</li>
                        <li>Fill out forms on our website</li>
                        <li>Receive our services</li>
                    </ul>
                    <p class="mt-4">
                        This information may include your name, email address, phone number, address, medical history, and insurance information.
                    </p>
                </div>

                <div>
                    <h2 class="text-3xl font-bold text-white mb-4">2. How We Use Your Information</h2>
                    <p>
                        We use the information we collect to:
                    </p>
                    <ul class="list-disc list-inside space-y-2 ml-4">
                        <li>Provide and improve our services</li>
                        <li>Process your appointments and consultations</li>
                        <li>Communicate with you about your care</li>
                        <li>Comply with legal obligations</li>
                        <li>Protect against fraud and abuse</li>
                    </ul>
                </div>

                <div>
                    <h2 class="text-3xl font-bold text-white mb-4">3. Information Sharing</h2>
                    <p>
                        We may share your information with:
                    </p>
                    <ul class="list-disc list-inside space-y-2 ml-4">
                        <li>Legal partners in our referral network</li>
                        <li>Insurance providers for billing purposes</li>
                        <li>Healthcare providers involved in your treatment</li>
                        <li>Law enforcement when required by law</li>
                    </ul>
                    <p class="mt-4">
                        We do not sell your personal information to third parties.
                    </p>
                </div>

                <div>
                    <h2 class="text-3xl font-bold text-white mb-4">4. Data Security</h2>
                    <p>
                        We implement appropriate technical and organizational measures to protect your personal information against unauthorized access, alteration, disclosure, or destruction. However, no method of transmission over the Internet is 100% secure.
                    </p>
                </div>

                <div>
                    <h2 class="text-3xl font-bold text-white mb-4">5. Your Rights</h2>
                    <p>
                        You have the right to:
                    </p>
                    <ul class="list-disc list-inside space-y-2 ml-4">
                        <li>Access your personal information</li>
                        <li>Correct inaccurate information</li>
                        <li>Request deletion of your information</li>
                        <li>Opt-out of certain communications</li>
                    </ul>
                    <p class="mt-4">
                        To exercise these rights, please contact us at prechiropractic@gmail.com.
                    </p>
                </div>

                <div>
                    <h2 class="text-3xl font-bold text-white mb-4">6. Contact Us</h2>
                    <p>
                        If you have questions about this Privacy Policy, please contact us at:
                    </p>
                    <p class="mt-4">
                        <strong>Pre Chiropractic</strong><br>
                        Email: prechiropractic@gmail.com<br>
                        Location: Oakland, California
                    </p>
                </div>

                <div class="bg-gray-800 p-6 rounded-lg border border-gray-700">
                    <p class="text-sm">
                        <strong>Last Updated:</strong> January 2025<br>
                        This Privacy Policy may be updated from time to time. We will notify you of any changes by posting the new Privacy Policy on this page.
                    </p>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer (Same as index.html) -->
    <footer class="bg-gray-900 border-t border-gray-800 py-16">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="border-t border-gray-800 pt-8">
                <p class="text-gray-400 text-sm text-center">
                    &copy; 2025 Pre Chiropractic. All rights reserved.
                </p>
            </div>
        </div>
    </footer>
</body>
</html>
```

### Step 2: Create the Terms of Service Page

**Create a new file called `terms.html` in your website folder:**

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Terms of Service for Pre Chiropractic">
    <meta name="author" content="Pre Chiropractic">
    <title>Terms of Service | Pre Chiropractic</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        html {
            scroll-behavior: smooth;
        }
        
        .gradient-text {
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }
    </style>
</head>
<body class="bg-gray-900 text-white">
    <!-- Header Navigation -->
    <header class="sticky top-0 z-50 bg-gray-900 bg-opacity-95 backdrop-blur-md border-b border-gray-800">
        <nav class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-4 flex items-center justify-between">
            <div class="flex items-center space-x-2">
                <div class="w-10 h-10 bg-gradient-to-r from-purple-600 to-pink-600 rounded-lg flex items-center justify-center">
                    <i class="fas fa-heartbeat text-white text-xl"></i>
                </div>
                <a href="index.html" class="text-2xl font-bold gradient-text">Pre Chiropractic</a>
            </div>
            
            <div class="hidden md:flex items-center space-x-8">
                <a href="index.html#features" class="text-gray-300 hover:text-white transition-colors duration-300">Services</a>
                <a href="index.html#benefits" class="text-gray-300 hover:text-white transition-colors duration-300">Benefits</a>
                <a href="index.html#testimonials" class="text-gray-300 hover:text-white transition-colors duration-300">Testimonials</a>
                <a href="index.html#faq" class="text-gray-300 hover:text-white transition-colors duration-300">FAQ</a>
                <a href="index.html#about" class="text-gray-300 hover:text-white transition-colors duration-300">About</a>
            </div>
        </nav>
    </header>

    <!-- Main Content -->
    <section class="py-24 bg-gray-900">
        <div class="max-w-4xl mx-auto px-4 sm:px-6 lg:px-8">
            <h1 class="text-5xl md:text-6xl font-black mb-12 tracking-tight">
                <span class="gradient-text">Terms of Service</span>
            </h1>
            
            <div class="prose prose-invert max-w-none space-y-8 text-gray-300">
                <div>
                    <h2 class="text-3xl font-bold text-white mb-4">1. Acceptance of Terms</h2>
                    <p>
                        By accessing and using this website and our services, you accept and agree to be bound by the terms and provision of this agreement. If you do not agree to abide by the above, please do not use this service.
                    </p>
                </div>

                <div>
                    <h2 class="text-3xl font-bold text-white mb-4">2. Use License</h2>
                    <p>
                        Permission is granted to temporarily download one copy of the materials (information or software) on Pre Chiropractic's website for personal, non-commercial transitory viewing only. This is the grant of a license, not a transfer of title, and under this license you may not:
                    </p>
                    <ul class="list-disc list-inside space-y-2 ml-4">
                        <li>Modify or copy the materials</li>
                        <li>Use the materials for any commercial purpose or for any public display</li>
                        <li>Attempt to reverse engineer any software contained on the website</li>
                        <li>Remove any copyright or other proprietary notations from the materials</li>
                        <li>Transfer the materials to another person or "mirror" the materials on any other server</li>
                    </ul>
                </div>

                <div>
                    <h2 class="text-3xl font-bold text-white mb-4">3. Disclaimer</h2>
                    <p>
                        The materials on Pre Chiropractic's website are provided on an 'as is' basis. Pre Chiropractic makes no warranties, expressed or implied, and hereby disclaims and negates all other warranties including, without limitation, implied warranties or conditions of merchantability, fitness for a particular purpose, or non-infringement of intellectual property or other violation of rights.
                    </p>
                </div>

                <div>
                    <h2 class="text-3xl font-bold text-white mb-4">4. Limitations</h2>
                    <p>
                        In no event shall Pre Chiropractic or its suppliers be liable for any damages (including, without limitation, damages for loss of data or profit, or due to business interruption) arising out of the use or inability to use the materials on Pre Chiropractic's website.
                    </p>
                </div>

                <div>
                    <h2 class="text-3xl font-bold text-white mb-4">5. Accuracy of Materials</h2>
                    <p>
                        The materials appearing on Pre Chiropractic's website could include technical, typographical, or photographic errors. Pre Chiropractic does not warrant that any of the materials on its website are accurate, complete, or current. Pre Chiropractic may make changes to the materials contained on its website at any time without notice.
                    </p>
                </div>

                <div>
                    <h2 class="text-3xl font-bold text-white mb-4">6. Links</h2>
                    <p>
                        Pre Chiropractic has not reviewed all of the sites linked to its website and is not responsible for the contents of any such linked site. The inclusion of any link does not imply endorsement by Pre Chiropractic of the site. Use of any such linked website is at the user's own risk.
                    </p>
                </div>

                <div>
                    <h2 class="text-3xl font-bold text-white mb-4">7. Modifications</h2>
                    <p>
                        Pre Chiropractic may revise these terms of service for its website at any time without notice. By using this website, you are agreeing to be bound by the then current version of these terms of service.
                    </p>
                </div>

                <div>
                    <h2 class="text-3xl font-bold text-white mb-4">8. Governing Law</h2>
                    <p>
                        These terms and conditions are governed by and construed in accordance with the laws of the State of California, and you irrevocably submit to the exclusive jurisdiction of the courts in that location.
                    </p>
                </div>

                <div class="bg-gray-800 p-6 rounded-lg border border-gray-700">
                    <p class="text-sm">
                        <strong>Last Updated:</strong> January 2025<br>
                        These Terms of Service may be updated from time to time. We will notify you of any changes by posting the new Terms on this page.
                    </p>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer class="bg-gray-900 border-t border-gray-800 py-16">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="border-t border-gray-800 pt-8">
                <p class="text-gray-400 text-sm text-center">
                    &copy; 2025 Pre Chiropractic. All rights reserved.
                </p>
            </div>
        </div>
    </footer>
</body>
</html>
```

### Step 3: Verify Links in Your Main Page

The links to these pages are already in your `index.html`:

**In the footer (lines ~650-653):**

```html
<a href="privacy.html" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a>
<a href="terms.html" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a>
```

These links are **already correct** and will work once you create the `privacy.html` and `terms.html` files.

### Step 4: Test the Links

1. **Save both new files** (`privacy.html` and `terms.html`) in the same folder as your `index.html`
2. **Open your `index.html`** in a browser
3. **Scroll to the footer**
4. **Click "Privacy Policy"** - should open the privacy page
5. **Click "Terms of Service"** - should open the terms page
6. **Click the company logo** on the policy pages - should return to home

### Step 5: Customize the Policy Pages

The policy pages I provided are templates. You should customize them with your actual information:

#### In both `privacy.html` and `terms.html`:

**Replace this:**
```html
<meta name="author" content="Pre Chiropractic">
<title>Privacy Policy | Pre Chiropractic</title>
```

**With your company info:**
```html
<meta name="author" content="Your Company Name">
<title>Privacy Policy | Your Company Name</title>
```

**Replace all instances of:**
- `Pre Chiropractic` → Your company name
- `prechiropractic@gmail.com` → Your email
- `Oakland, California` → Your location

**Update the "Last Updated" date:**
```html
<strong>Last Updated:</strong> January 2025
```

**Add your specific terms and policies** - the content I provided is a template and may not accurately reflect your actual business practices. Consider consulting with a lawyer to ensure your policies comply with California law.

---

## Troubleshooting Common Issues

### Issue 1: Links Not Working

**Problem:** When I click a link, nothing happens or it goes to the wrong place.

**Solution:**

1. **For internal links (starting with #):**
   - Check that the section has the matching `id`
   - Example: Link `href="#faq"` must match a section with `id="faq"`
   - Make sure there are no typos

2. **For external links:**
   - Make sure the URL is complete (starts with `https://` or `http://`)
   - Test the URL directly in your browser first
   - Check that `target="_blank"` is included if you want it to open in a new tab

3. **For email links:**
   - Make sure it starts with `mailto:`
   - Example: `href="mailto:your-email@example.com"`
   - Test by clicking and checking your email client opens

4. **For relative links (like `privacy.html`):**
   - Make sure the file exists in the same folder as `index.html`
   - Make sure the filename is spelled exactly the same
   - Check for case sensitivity (some servers are case-sensitive)

### Issue 2: Text Not Displaying Correctly

**Problem:** My text is cut off, overlapping, or not visible.

**Solution:**

1. **Text is cut off:**
   - Check the container width classes
   - Look for `max-w-` classes that might be limiting width
   - Try increasing the width or removing the `max-w-` class

2. **Text overlapping:**
   - Check padding and margin values
   - Increase `p-` values (padding)
   - Add `mb-` values (margin-bottom) to create space

3. **Text not visible:**
   - Check text color (`text-white`, `text-gray-300`, etc.)
   - Check background color - text color must contrast with background
   - Try `text-white` if text isn't showing
   - Check that text isn't hidden behind other elements (z-index issue)

### Issue 3: Styling Changes Not Showing

**Problem:** I changed the CSS but the page looks the same.

**Solution:**

1. **Hard refresh your browser:**
   - Windows: Press `Ctrl + Shift + R`
   - Mac: Press `Cmd + Shift + R`
   - This clears the browser cache

2. **Check that you saved the file:**
   - Make sure you saved your changes (Ctrl+S or Cmd+S)
   - Check that you're editing the right file

3. **Check for syntax errors:**
   - Look for missing closing tags or quotes
   - Check that all `{` have matching `}`
   - Look for red underlines in your code editor

4. **For Tailwind classes:**
   - Make sure the class is spelled correctly
   - Tailwind classes are case-sensitive
   - Try using a class you know works, then modify it

### Issue 4: Mobile Menu Not Working

**Problem:** The mobile menu button doesn't open/close the menu.

**Solution:**

1. **Check the JavaScript:**
   - Look at the JavaScript section at the bottom of the file (lines ~710-750)
   - Make sure it's not commented out
   - Check that there are no syntax errors

2. **Check the HTML structure:**
   - Make sure the `.mobile-menu-button` class exists
   - Make sure the `.mobile-menu` class exists
   - Check that the button and menu are in the same `<header>` section

3. **Test in browser console:**
   - Right-click → Inspect
   - Go to Console tab
   - Look for any red error messages
   - These errors might tell you what's wrong

### Issue 5: Images Not Loading

**Problem:** I see broken image icons instead of images.

**Solution:**

1. **Check the image URL:**
   - Look for `src=""` attributes
   - Make sure the URL is complete and correct
   - Test the URL in your browser

2. **For external images (from Unsplash, etc.):**
   - The URL should start with `https://`
   - Make sure the website is still online
   - Try copying the image URL directly into your browser

3. **For local images:**
   - Make sure the image file exists
   - Make sure the filename is spelled correctly (case-sensitive)
   - Use relative paths: `src="images/my-image.jpg"`
   - Make sure the image is in the correct folder

### Issue 6: Page Layout Breaking on Mobile

**Problem:** The page looks good on desktop but is broken on mobile.

**Solution:**

1. **Check responsive classes:**
   - Look for `md:` and `lg:` prefixes
   - These control how the page looks on different screen sizes
   - Make sure mobile-first classes exist (without prefix)

2. **Test on actual mobile:**
   - Open DevTools (F12)
   - Click the mobile icon (usually top-left of DevTools)
   - Resize to different screen sizes

3. **Check common issues:**
   - Text too large: Reduce `text-` sizes
   - Content too wide: Check `max-w-` classes
   - Buttons overlapping: Check padding and spacing

### Issue 7: Colors Not Matching

**Problem:** My gradient or button colors don't look right.

**Solution:**

1. **Check color names:**
   - Tailwind uses specific color names: `purple-600`, `pink-600`, etc.
   - Check that you're using correct names
   - Visit [tailwindcss.com/docs/customization/colors](https://tailwindcss.com/docs/customization/colors) for full list

2. **Check color numbers:**
   - `600` is darker than `400`
   - `900` is very dark
   - `100` is very light
   - Adjust the number to get the shade you want

3. **For gradients:**
   - Format: `from-COLOR-NUMBER to-COLOR-NUMBER`
   - Example: `from-purple-600 to-pink-600`
   - Make sure both colors are specified

### Issue 8: FAQ Accordion Not Working

**Problem:** FAQ items don't expand/collapse when clicked.

**Solution:**

1. **Check the JavaScript:**
   - Look at the FAQ JavaScript (lines ~730-745)
   - Make sure it's not commented out
   - Check for syntax errors

2. **Check the HTML structure:**
   - Make sure each FAQ item has class `faq-item`
   - Make sure each question has class `faq-question`
   - Make sure each answer has class `faq-answer`
   - Make sure the icon has class `faq-icon`

3. **Test in browser:**
   - Right-click → Inspect
   - Look at the HTML to verify structure
   - Check Console tab for JavaScript errors

---

## Best Practices

### 1. Keep Backups

Before making major changes:

```
1. Copy your index.html to index-backup.html
2. Make your changes
3. Test thoroughly
4. If something breaks, you can restore from backup
```

### 2. Test Changes

After any update:

1. **Refresh the page** (Ctrl+Shift+R or Cmd+Shift+R)
2. **Test on desktop** - use your main browser
3. **Test on mobile** - use DevTools or actual phone
4. **Test all links** - click every link
5. **Test all interactive elements** - buttons, menu, FAQ

### 3. Use Version Control (Optional but Recommended)

If you use GitHub or similar:

```
1. Create a new branch for your changes
2. Make your changes
3. Test thoroughly
4. Merge to main when satisfied
5. You can always revert if needed
```

### 4. Update Consistently

When making changes:

- Update text in ALL locations (header, footer, multiple sections)
- Use Find & Replace to ensure consistency
- Keep the same style and tone throughout
- Don't mix old and new information

### 5. Keep SEO in Mind

When updating content:

- Keep your main keyword in the title
- Update meta description (160 characters max)
- Use clear, descriptive headings
- Include relevant keywords naturally
- Keep your company name consistent

### 6. Mobile-First Approach

When adding new content:

1. Design for mobile first
2. Then add classes for larger screens
3. Test on mobile, tablet, and desktop
4. Example: `text-lg md:text-xl lg:text-2xl`

### 7. Color Consistency

Keep your brand colors consistent:

- Primary: Purple-to-pink gradient (`from-purple-600 to-pink-600`)
- Text: White on dark (`text-white`), Gray on light (`text-gray-300`)
- Accents: Green for success (`text-green-500`), Yellow for stars (`text-yellow-400`)
- Don't change colors randomly - maintain your brand identity

### 8. Font and Typography

Keep typography consistent:

- Headings: Use `font-black` for impact
- Body text: Use `font-light` or default weight
- Descriptions: Use `text-gray-300` for secondary text
- Consistency creates professionalism

### 9. Spacing and Layout

Maintain consistent spacing:

- Use `mb-` classes for vertical spacing
- Use `space-y-` for spacing between elements
- Keep padding consistent (`p-6`, `p-8`, etc.)
- Align items with `flex` and `grid` classes

### 10. Performance Tips

Keep your page fast:

- Compress images before uploading
- Use external images (CDN) when possible
- Minimize JavaScript code
- Remove unused CSS classes
- Test page speed with Google PageSpeed Insights

### 11. Accessibility

Make your site usable for everyone:

- Use semantic HTML (`<header>`, `<section>`, `<footer>`)
- Add `alt` text to images
- Use sufficient color contrast
- Make buttons keyboard-accessible
- Include descriptive link text (not "click here")

### 12. Documentation

Keep notes about your changes:

```
2025-01-15: Updated company name to "Recovery Plus Legal"
2025-01-15: Changed primary button color from purple to blue
2025-01-14: Added new testimonial from John Smith
```

This helps you remember what you changed and why.

---

## Quick Reference Guide

### File Locations for Common Updates

| What to Change | File Location | Line Number |
|---|---|---|
| Company Name | `index.html` | 50, 650 |
| Page Title | `index.html` | 10 |
| Hero Headline | `index.html` | 115 |
| Feature Cards | `index.html` | 175-250 |
| Testimonials | `index.html` | 370-430 |
| About Section | `index.html` | 440-485 |
| FAQ Items | `index.html` | 500-620 |
| Email Address | `index.html` | 668, 700 |
| Booking Link | `index.html` | 62, 76, 126, 335, 654, 700 |
| Social Links | `index.html` | 625-640 |

### Common Tailwind Classes Reference

```
Text Sizes: text-sm, text-lg, text-xl, text-2xl, text-4xl, text-5xl, text-6xl
Colors: text-white, text-gray-300, text-purple-600, text-pink-600, text-green-500
Spacing: p-4, px-8, py-4, mb-4, mt-1, space-y-3
Fonts: font-bold, font-black, font-light
Responsive: md:text-2xl, lg:text-3xl
Borders: border, rounded-lg, rounded-xl, rounded-full
```

### Keyboard Shortcuts

```
Ctrl/Cmd + H = Find & Replace
Ctrl/Cmd + S = Save file
Ctrl/Cmd + Z = Undo
Ctrl/Cmd + Shift + R = Hard refresh browser
F12 = Open Developer Tools
```

---

## Getting Help

### Common Resources

- **Tailwind CSS Docs:** https://tailwindcss.com/docs
- **Font Awesome Icons:** https://fontawesome.com/icons
- **HTML Reference:** https://developer.mozilla.org/en-US/docs/Web/HTML
- **CSS Reference:** https://developer.mozilla.org/en-US/docs/Web/CSS

### When Something Goes Wrong

1. **Check the Console:** F12 → Console tab → Look for red errors
2. **Validate HTML:** https://validator.w3.org/
3. **Test CSS:** https://jigsaw.w3.org/css-validator/
4. **Ask for help:** Share your code and error message with a developer

---

## Conclusion

You now have a comprehensive guide for maintaining and customizing your Pre Chiropractic landing page. Remember:

- **Start small** - make one change at a time
- **Test frequently** - refresh and check after each change
- **Keep backups** - save copies before major changes
- **Be consistent** - maintain your brand style
- **Ask for help** - don't hesitate to reach out if stuck

Good luck with your landing page! Your business will benefit from a professional, well-maintained web presence.