# Prime Stay Services SRL - Website

This is a modern, responsive, and fast static website built for Prime Stay Services SRL, a professional cleaning business in Romania.

## Tech Stack
- **HTML5**: Semantic and accessible markup.
- **Tailwind CSS (via CDN)**: Utility-first CSS framework for rapid UI development without a build step.
- **Vanilla JavaScript**: Lightweight interactivity for mobile menus, language toggles, price estimators, and form simulation.
- **Phosphor Icons**: Beautiful, clean icon set included via CDN.
- **Google Fonts**: 'Outfit' for headings and 'Inter' for body text.

## Project Structure
```
/
├── index.html        # Home Page (Hero, Why Us, Price Estimator, Testimonials)
├── services.html     # Services Page (Detailed service cards, Comparison table)
├── about.html        # About Us Page (Story, Values, Trust badges)
├── contact.html      # Contact Page (Info, Interactive Quote Form)
├── css/
│   └── styles.css    # Custom CSS for micro-animations and specific design touches
├── js/
│   └── main.js       # Core interactivity (Estimator logic, mobile menu, language toggle)
└── README.md         # This documentation file
```

## How to Edit the Website

### 1. Editing Text and Content
Open any `.html` file in a text editor (like VS Code, Notepad, or Sublime Text). Look for the text you want to change inside the HTML tags (e.g., `<h1>`, `<p>`, `<span>`). Save the file and refresh your browser to see the changes.

### 2. Changing Colors
The main brand colors are defined in the Tailwind configuration script within the `<head>` of every HTML file:
```javascript
tailwind.config = {
    theme: {
        extend: {
            colors: {
                primary: '#0284C7', // Main Blue
                accent: '#059669',  // Emerald Green
            }
        }
    }
}
```
Change these hex codes to update the brand colors across the entire site instantly.

### 3. Updating the WhatsApp Number
In every HTML file, there is a floating WhatsApp widget near the bottom (before the `<script>` tags). Change the `href` attribute:
```html
<a href="https://wa.me/40700000000" ...>
```
Replace `40700000000` with your actual phone number, including the country code (40 for Romania), without any spaces or plus signs.

### 4. Updating the Price Estimator
The logic for the price estimator is in `js/main.js`. You can adjust the base prices and multipliers directly in the `calculateEstimate` function.

## How to Host the Website

Because this is a completely static website (no backend server or build process required), you can host it for free or very cheaply on almost any provider.

### Option 1: Vercel or Netlify (Recommended - Free)
1. Create a free account on [Vercel](https://vercel.com/) or [Netlify](https://www.netlify.com/).
2. Drag and drop this entire project folder into their dashboard (Deploy manually).
3. They will provide a live URL instantly. You can then attach a custom domain (e.g., `primestayservices.ro`).

### Option 2: GitHub Pages (Free)
1. Create a GitHub repository and upload these files.
2. Go to Settings -> Pages.
3. Select the `main` branch as the source and click Save.

### Option 3: Traditional cPanel Hosting
1. Purchase hosting and a domain name (e.g., from Hostico, Romarg, RoHost).
2. Open the File Manager in cPanel or connect via FTP.
3. Upload all files (`index.html`, `css/`, `js/`, etc.) directly into the `public_html` folder.

## Forms Notice
Currently, the contact form on the `contact.html` page is a visual simulation handled by JavaScript (it shows a success message but does not send an email). 
To make it functional on static hosting, you can integrate a service like [Formspree](https://formspree.io/) or [Netlify Forms](https://docs.netlify.com/forms/setup/). Simply change the `<form>` tag's `action` attribute to the endpoint they provide.
