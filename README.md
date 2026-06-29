# HopeCare Hospital Website

## Overview
HopeCare Hospital is a responsive web-based presentation platform for Uganda's leading National Youth Referral Hospital. The website showcases the hospital's services, news, mission, vision, and key personnel information.

## Features

### 1. **Responsive Header Navigation**
- Logo and hospital branding
- Navigation menu with links to:
  - Home
  - Departments
  - Directorates
  - Gallery
  - About Us
- Mobile-friendly design

### 2. **Interactive Carousel**
- Displays 5 medical staff images
- Auto-rotates every 3 seconds
- Manual navigation with previous/next buttons (❮ ❯)
- Dot indicators for slide navigation
- Smooth fade and slide transitions (4s duration)

### 3. **Executive Director's Message**
- Features the Executive Director's photo
- Includes welcome message and hospital overview
- Highlights diagnostic and emergency services

### 4. **News & Publications Section**
- Grid layout displaying 3 news cards
- Cards include:
  - News images
  - Article headlines
  - Brief descriptions
- Hover effects for interactivity

### 5. **Vision, Mission & Values Section**
- Mission statement
- Vision statement
- Goals and core values
- Professional formatting with Bootstrap styling

### 6. **Footer**
- Hospital information and description
- Quick links navigation
- Services listing
- Contact information:
  - Address: Rubaga Hill, Kampala, Uganda
  - Phone: +256 768 709 563
  - Email: info@hopecare.go.ug
  - Website: www.hopecarehospital.go.ug
- Copyright information

---

## Technical Details

### **Technologies Used**
- **HTML5** - Page structure and semantic markup
- **CSS3** - Styling, animations, and responsive design
- **JavaScript** - Carousel functionality and interactivity
- **Bootstrap 5.3.0** - Additional responsive styling components

### **Key Components**

#### CSS Classes
- `.carousel` - Main carousel container
- `.slide` - Individual slide elements with fade/transform animations
- `.news-card` - News article cards with hover effects
- `.footer-grid` - Responsive footer layout
- `.director-message` - Executive message section

#### JavaScript Functions
| Function | Purpose |
|----------|---------|
| `showSlide(newIndex)` | Updates carousel display and dot indicators |
| `prevBtn.onclick()` | Navigate to previous slide |
| `nextBtn.onclick()` | Navigate to next slide |
| `dot.onclick()` | Jump to specific slide via dot indicator |
| `setInterval()` | Auto-advance carousel every 3 seconds |

### **Responsive Breakpoints**
- **≤ 980px**: Single column grid layout
- **≤ 720px**: Optimized padding and full-width cards

---

## File Structure
