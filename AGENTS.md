# TeaLixir Website Agents

## Project Description

This project is a website for the TeaLixir iOS app. The website is built using the
Hugo static site generator with a modern, iOS-inspired design that showcases the app's
intelligent features and appeals to iOS and iPadOS users.

### iOS App Information

TeaLixir is an intelligent tea tracking app for iOS that helps users remember what they love,
discover new favorites, and never buy disappointing tea again. The app is designed with
privacy as a core principle and is coming soon to the App Store.

**Core Value Proposition:**
"Finally, a tea app that actually understands tea."

**Key Intelligent Features:**
- **Smart Tea Scanning**: Advanced OCR technology reads tea packaging and automatically extracts:
  - Tea name and brand
  - Origin and estate information
  - Tea type and caffeine level
  - Flush season and harvest details
  - Organic and Fair Trade certifications
  - Brewing instructions and tasting notes
- **Intelligent Tea Matching**: Understands tea relationships (e.g., "Ceylon" means Sri Lanka), recognizes estate names, and matches teas to existing brands
- **Personal Tea Intelligence**: Analyzes taste patterns and provides personalized recommendations
- **Smart Purchase Tracking**: Track purchase history, mark teas as purchased, sort by recent purchases
- **Seamless iCloud Sync**: Automatic sync across iPhone, iPad, and other Apple devices

**Comprehensive Tea Data Tracking:**
- Tea type (black, green, herbal, oolong, etc.)
- Caffeine levels and brewing instructions
- Tasting notes and personal ratings
- Origin, estate, harvest season details
- Organic and Fair Trade certifications
- Brand and seller information
- Photos of tea packages
- Purchase history and frequency

**Privacy-First Design:**
- All data stored securely in user's personal Apple iCloud account
- No external servers or data collection
- User maintains complete ownership and control of their data
- On-device image processing with Apple Core ML
- No analytics, tracking, or third-party data sharing

**Target Users:**
- **New to Tea**: Simple scanning and rating to build confidence
- **Tea Enthusiasts**: Detailed tracking and comprehensive tasting notes
- **Serious Collectors**: Extensive photo documentation and collection management

## Website Features

**Enhanced Content Structure:**
- **Hero Banner**: Compelling headline with gradient background and download button
- **Problem-Solution Section**: Addresses user pain points and positions TeaLixir as the solution
- **Smart Features Showcase**: Detailed explanation of intelligent app capabilities
- **User Personas**: Tailored content for different types of tea drinkers
- **Key Features Grid**: Comprehensive feature overview in organized cards
- **Why Choose TeaLixir**: Five compelling reasons with enhanced messaging
- **Download CTA**: Strong call-to-action with "coming soon" status

**Design Principles:**
- **iOS-Inspired Design**: Clean, modern styling that appeals to iOS users
- **Mobile-First**: Optimized for iPhone and iPad viewing
- **Accessibility**: Good contrast ratios and readable typography
- **Performance**: Lightweight CSS with efficient layouts
- **Modular Architecture**: Hugo shortcodes for easy content management

**Hugo Shortcodes System:**
The website uses a comprehensive shortcode system for modular content:
- `hero-banner` - Enhanced hero with download button
- `problem-solution` - Problem/solution messaging
- `smart-features-section` & `smart-feature` - Intelligent features showcase
- `user-personas` & `persona-card` - User persona sections
- `key-features-grid` & `key-feature` - Feature grid layout
- `download-cta` - Call-to-action section
- `why-section` & `why-card` - Why choose cards

**Privacy Policy:**
Comprehensive privacy policy with detailed information about:
- iCloud data storage and encryption
- Apple's privacy infrastructure
- User data rights and control
- Security measures and best practices
- No third-party data sharing or analytics

## Website Tech Stack

- **Hugo** (version: v0.128.0+extended) - Static site generator
- **CSS3** - Modern styling with Grid, Flexbox, and advanced features
- **Hugo Shortcodes** - Modular content management system
- **Responsive Design** - Mobile-first approach for all devices

## Key Files and Structure

**Content Management:**
- `content/_index.md` - Homepage content using shortcodes
- `content/privacy-policy/_index.md` - Comprehensive privacy policy with iCloud details
- `content/contact/_index.md` - Contact page

**Templates and Layouts:**
- `layouts/index.html` - Simplified homepage template
- `layouts/shortcodes/` - 13 shortcode components for modular content
- `layouts/partials/` - Reusable template components

**Styling:**
- `static/css/main.css` - Comprehensive CSS with iOS-inspired design
- Responsive breakpoints for mobile, tablet, and desktop
- CSS custom properties for consistent theming

**Configuration:**
- `hugo.toml` - Site configuration with metadata and build settings
- Updated title: "TeaLixir - Your Personal Tea Journey Companion"

## Development Workflow

**Local Development:**
```bash
hugo server --buildDrafts --buildFuture
```

**Production Build:**
```bash
hugo
```

**Content Updates:**
- Modify content in `content/` directory using Markdown and shortcodes
- Shortcodes provide separation between content and presentation
- No HTML/CSS knowledge required for content updates

**App Store Integration:**
- `download-cta` shortcode supports easy transition from "coming soon" to live App Store links
- Simply change `status="coming-soon"` to `status="available"` and add `app_id="1234567890"`
- No code changes required - just content parameter updates
- See `APP_STORE_SETUP.md` for detailed instructions

**Design Updates:**
- CSS modifications in `static/css/main.css`
- Shortcode template updates in `layouts/shortcodes/`
- Responsive design considerations for all changes
