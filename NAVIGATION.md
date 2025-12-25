# Tide/Light Navigation Guidelines

## Top Navigation Pattern

Every page in the Tide/Light project must follow this consistent navigation pattern:

### Top Left Button
- **Position:** Fixed, top left corner
- **Function:** Back/navigation button
- **Examples:**
  - Landing page: N/A (homepage has no back button)
  - Blog listing pages: `← Tide/Light` (back to homepage)
  - Individual blog posts: `← The Sunrise Lyra` (back to blog listing)
  
### Top Right Button
- **Position:** Fixed, top right corner
- **Function:** "Glide in!" link (quasi-login page)
- **URL:** `/about`
- **Style:** Identical to the left button
- **Text:** Always "Glide in!"

### Styling Requirements
Both buttons must have:
- Same border style (1px solid)
- Same padding (0.5rem 1rem)
- Same border-radius (4px)
- Same font size (0.9rem)
- Same hover effects (color and border transition to accent color)
- Same text color (--text-secondary)

### CSS Implementation
```css
.top-nav {
	position: fixed;
	top: 0;
	left: 0;
	right: 0;
	z-index: 1000;
	display: flex;
	justify-content: space-between;
	align-items: center;
	padding: 1.5rem 2rem;
	background: linear-gradient(180deg, var(--bg-primary) 0%, transparent 100%);
}

.top-nav a {
	color: var(--text-secondary);
	text-decoration: none;
	font-size: 0.9rem;
	padding: 0.5rem 1rem;
	border: 1px solid var(--text-secondary);
	border-radius: 4px;
	transition: all 0.2s ease;
}

.top-nav a:hover {
	color: var(--accent);
	border-color: var(--accent);
}
```

### Page-Specific Navigation

#### Landing Page (index.html)
- Top Right: `Glide in!` → `/about`

#### Blog Listing Pages (pages/sunrise-lyra.html, etc.)
- Top Left: `← Tide/Light` → `../index.html`
- Top Right: `Glide in!` → `/about`

#### Individual Blog Posts (blogs/*.html)
- Top Left: `← The Sunrise Lyra` → `../pages/sunrise-lyra.html`
- Top Right: `Glide in!` → `/about`

## Consistency is Key
This navigation pattern ensures users always know:
1. How to go back (top left)
2. How to access the login/about page (top right)
3. Where they are in the site hierarchy

**Never deviate from this pattern without updating this document.**
