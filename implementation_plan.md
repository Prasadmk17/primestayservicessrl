# Implementation Plan - Prime Stay Services SRL

## 1. Project Structure
The project will consist of a simple static structure to ensure fast load times and ease of hosting on platforms like GitHub Pages, Vercel, or Netlify.

```
/
├── index.html        # Acasă (Home Page)
├── services.html     # Servicii (Services Page)
├── about.html        # Despre Noi (About Us Page)
├── contact.html      # Contact & Estimare Preț (Contact Page)
├── css/
│   └── styles.css    # Custom CSS (Micro-animations, Tailwind overrides, glassmorphism)
├── js/
│   └── main.js       # Interactive logic (Mobile menu, language toggle, estimators)
├── assets/           # Images, logos, and icons (if needed)
└── README.md         # Documentation for hosting and editing
```

## 2. Design System
- **Framework:** HTML5 + Tailwind CSS (via CDN for simplicity and immediate setup).
- **Typography:** 
  - Headings: 'Outfit', sans-serif (Modern, clean, bold).
  - Body: 'Inter', sans-serif (Highly readable, neutral).
- **Color Palette:**
  - Primary: Clean Blue (`sky-600` / `#0284C7`)
  - Accent: Emerald Green (`emerald-600` / `#059669`)
  - Background: Soft Gray (`gray-50` / `#F9FAFB`) to crisp White (`#FFFFFF`)
  - Text: Dark Slate (`slate-800` / `#1E293B`)
- **Aesthetics:** 
  - Subtle drop shadows for cards (`shadow-lg`, `shadow-xl`).
  - Glassmorphism for floating elements (navbars, widgets).
  - Hover micro-animations on interactive elements (buttons, cards, links).

## 3. Component Breakdown
### Shared Components
- **Navbar:** Sticky glassmorphic header, Logo, Nav Links, Language Switcher (RO/EN), "Cere Ofertă" CTA button, Hamburger menu for mobile.
- **Footer:** Dark background (`slate-900`), Legal Details (SRL, CUI, Reg. Com.), Contact Links, Copyright.
- **Floating WhatsApp Widget:** Fixed bottom-right corner button with pulse animation for direct contact.

### Page-Specific Components
- **Home (`index.html`):**
  - **Hero Section:** High-impact headline, dynamic background image (or gradient), two CTA buttons.
  - **Why Choose Us:** Grid layout with icons (Guarantee, Staff, Eco-friendly, Fast).
  - **Price Estimator:** Interactive card with drop-downs for Property Type and Service Type, calculating base price via JS.
  - **Testimonials:** 3-column grid highlighting reviews.
  - **Bottom CTA:** Banner prompting action.
- **Services (`services.html`):**
  - **Service Cards:** Detailed grid for Airbnb, Residential, Deep Clean, and Office cleaning.
  - **Comparison Table:** What's included checklist table.
- **About Us (`about.html`):**
  - **Story Section:** Two-column layout (Text + Image) for the company story.
  - **Values & Badges:** Grid layout highlighting trust factors.
- **Contact (`contact.html`):**
  - **Contact Info:** Cards for Phone, Email, Hours, Locations.
  - **Quote Form:** Responsive form grid, date picker, submit button with JS success state simulation.

## 4. Implementation Steps
1. Scaffold directories and initial files.
2. Build the shared Navbar and Footer inside each HTML page.
3. Construct `index.html` with Hero and Price Estimator.
4. Construct `services.html`, `about.html`, and `contact.html`.
5. Add custom CSS in `styles.css` for animations and fonts.
6. Write JavaScript in `main.js` to handle interactivity (menu, estimator, language toggle structure).
7. Final polish and README generation.
