# Tide/Light Landing Page - Escape Package

Beautiful landing page extracted from the Astro project for use in Webflow or any other platform.

## Files Included

- **index.html** - Complete standalone HTML
- **styles.css** - All styles including theme switching
- **README.md** - This file

## Features

### ✨ Time-Based Theming
- **Light Mode** (6 AM - 6 PM): Daylight Sunset palette
- **Tide Mode** (6 PM - 6 AM): Obsidian Void palette with radial gradient
- Click "Tide" or "Light" in the logo to manually switch themes
- Theme preference is saved to localStorage

### 🎨 Three Beautiful Cards
1. **The Sunrise Lyra** - Music blog with Gorditas font
2. **The Highnoon Parchment** - Books blog with UnifrakturMaguntia font
3. **The Moonlit Senet** - Games blog with Metal Mania font

### 🎯 Design Highlights
- 16:9 aspect ratio cards with background images
- Gradient overlays and color tinting per card
- Gradient text effect on "Light" with glow
- Radial gradient background in Tide mode
- Smooth transitions and hover effects
- Fully responsive design

## Customization

### Change Card Images
Edit the `:root` CSS variables in `styles.css`:
```css
:root {
	--sunrise-img: url('your-image-url');
	--parchment-img: url('your-image-url');
	--senet-img: url('your-image-url');
}
```

### Change Colors
Modify the theme variables in `styles.css`:
- `body.light-mode` for light theme colors
- `body.tide-mode` for dark theme colors

### Change Fonts
The page uses three Google Fonts (already linked in HTML):
- Gorditas (Sunrise)
- UnifrakturMaguntia (Highnoon)
- Metal Mania (Moonlit)

### Update Links
In `index.html`, change the href attributes:
- Top-right button: `/about`
- Sunrise Lyra: `/sunrise-lyra`
- Highnoon Parchment: `/highnoon-parchment`
- Moonlit Senet: `/moonlit-senet`

## Webflow Integration Tips

1. **Custom Code**: Paste the entire `index.html` body into a custom code embed
2. **CSS**: Add `styles.css` to Project Settings → Custom Code → Head Code wrapped in `<style>` tags
3. **Fonts**: Google Fonts are already linked in the HTML head
4. **Images**: Upload your images to Webflow assets and update URLs in CSS
5. **Theme Script**: The JavaScript is included inline in the HTML and will work automatically

## Technical Details

- Pure HTML/CSS/JS - no framework dependencies
- localStorage for theme persistence
- CSS custom properties for theming
- Mobile-responsive grid layout
- Accessibility features (focus states, smooth scroll)

## Author
- idhant <3

Crafted with love in VS Code, ready for Webflow ✨
