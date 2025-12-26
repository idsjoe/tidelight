# Tide/Light Project Structure

```
tidelight/
├── index.html                      # Landing page with Tide/Light logo and three blog cards
├── styles.css                      # Main styles for landing page with Tide/Light theme switching
├── vercel.json                     # Vercel deployment configuration
├── README.md                       # Project README
├── NAVIGATION.md                   # Navigation guidelines and patterns
├── DEPLOYMENT.md                   # Vercel deployment instructions
├── PROJECT_STRUCTURE.md            # This file - project structure documentation
│
├── pages/                          # Blog listing pages + about page
│   ├── sunrise-lyra.html          # The Sunrise Lyra - Daily music blog listing
│   ├── highnoon-parchment.html    # The Highnoon Parchment - Weekly book blog listing
│   ├── moonlit-senet.html         # The Moonlit Senet - Monthly game blog listing
│   └── about.html                 # Glide in! - Under construction login page
│
├── blogs/                          # Individual blog posts organized by blog type
│   ├── sunrise-lyra/              # Daily music blog posts
│   │   ├── 001-hotel-california.html  # #001 - Hotel California by The Eagles (Dec 25)
│   │   └── 002-running-up-that-hill.html # #002 - Running Up That Hill by Kate Bush (Dec 26)
│   ├── highnoon-parchment/        # Weekly book blog posts
│   │   └── coming-soon.html       # Placeholder post
│   └── moonlit-senet/             # Monthly game blog posts
│       └── coming-soon.html       # Placeholder post
│
├── assets/                         # Shared resources
│   ├── pages-styles.css           # Shared styles for blog listing pages
│   ├── blog-post-styles.css       # Styles for individual blog posts
│   ├── sunrise-lyra-theme.css     # Sunrise-specific color theme (warm sunrise feel)
│   ├── highnoon-parchment-theme.css # Parchment-specific color theme (mid-day feel)
│   ├── moonlit-senet-theme.css    # Senet-specific color theme (moonlit night feel)
│   └── under-construction.css     # Styles for about.html page
│
└── BlogFormat/                     # Markdown drafts and content source files
    ├── TheSunriseLyra/            # Sunrise Lyra markdown drafts
    │   ├── #001-hotel-california.md    # Source content for Hotel California post
    │   └── #002-running-up-that-hill.md # Source content for Running Up That Hill post
    ├── TheHighnoonParchment/      # Highnoon Parchment markdown drafts
    └── TheMoonlitSenet/           # Moonlit Senet markdown drafts
```

## File Descriptions

### Root Files
- **index.html** - Main landing page featuring Tide/Light branding and three clickable blog cards (Sunrise Lyra, Highnoon Parchment, Moonlit Senet). Includes Open Graph meta tags for social media previews.
- **styles.css** - Complete styling for the landing page including time-based theme switching (Tide/Light modes)
- **vercel.json** - Vercel deployment configuration for clean URLs
- **README.md** - Project documentation
- **NAVIGATION.md** - Navigation pattern documentation for consistent site navigation
- **DEPLOYMENT.md** - Complete guide for deploying to Vercel

### pages/
Contains blog listing pages that show all posts for each blog category, plus the about page.
- **sunrise-lyra.html** - Daily music blog listing with featured latest post and grid of past posts (sunrise theme). Currently showing 2 posts with "Previous Posts" section.
- **highnoon-parchment.html** - Weekly book blog listing with featured latest post (parchment/mid-day theme)
- **moonlit-senet.html** - Monthly game blog listing with featured latest post (moonlit night theme)
- **about.html** - "Glide in!" under-construction login page (forced light mode, half-built UI elements)

### blogs/
Contains individual blog post files, organized by blog type into subdirectories.
- **sunrise-lyra/** - Daily music blog posts
  - 001-hotel-california.html - #001: Hotel California by The Eagles (Dec 25, 2025)
  - 002-running-up-that-hill.html - #002: Running Up That Hill by Kate Bush (Dec 26, 2025)
- **highnoon-parchment/** - Weekly book blog posts
  - coming-soon.html - Placeholder post
- **moonlit-senet/** - Monthly game blog posts
  - coming-soon.html - Placeholder post

### assets/
Shared CSS files used across multiple pages.
- **pages-styles.css** - Shared styling for all blog listing pages
- **blog-post-styles.css** - Styling for individual blog post pages
- **sunrise-lyra-theme.css** - Warm sunrise color palette (coral accents, cream background)
- **highnoon-parchment-theme.css** - Aged parchment color palette (leather-tan accents)
- **moonlit-senet-theme.css** - Dark moonlit color palette (ultraviolet accents, obsidian background)
- **under-construction.css** - Styling for about.html with construction-themed UI elements

### BlogFormat/
Markdown source files for blog content (drafts and content organization).
- **TheSunriseLyra/** - Source markdown files for Sunrise Lyra posts
- **TheHighnoonParchment/** - Source markdown files for Highnoon Parchment posts
- **TheMoonlitSenet/** - Source markdown files for Moonlit Senet posts

## Theme Notes
- **Landing page (index.html):** Time-based theme switching between Tide (dark) and Light (bright) modes
- **Blog listing pages:** Each has a fixed custom theme (no switching)
  - Sunrise Lyra: Warm sunrise palette
  - Highnoon Parchment: Mid-day parchment palette
  - Moonlit Senet: Dark moonlit palette
- **About page:** Fixed light mode only
- All pages maintain consistent navigation with back button (top left) and "Glide in!" button (top right)

## Deployment
Ready for Vercel deployment with clean URLs configured via vercel.json
