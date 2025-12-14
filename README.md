# TeaLixir Website

This is the official website for the TeaLixir iOS app - an intelligent tea tracking app that helps users discover, track, and enjoy their perfect cup of tea.

## About TeaLixir

TeaLixir is an intelligent tea tracking app for iOS that helps you remember what you love, discover new favorites, and never buy disappointing tea again. Key features include:

- **Smart Tea Scanning**: Advanced OCR technology reads tea packaging and automatically extracts tea information
- **Intelligent Tea Matching**: Understands tea relationships and recognizes estate names and origins
- **Personal Tea Intelligence**: Analyzes your taste patterns and provides personalized recommendations
- **Smart Purchase Tracking**: Track purchase history and never forget a great tea again
- **Seamless iCloud Sync**: Your tea collection syncs automatically across all your Apple devices
- **Privacy-First Design**: All data stored securely in your personal iCloud account

## Website Features

- **Enhanced Landing Page**: iOS-inspired design with comprehensive app feature showcase
- **Problem-Solution Messaging**: Addresses user pain points and positions TeaLixir as the solution
- **User Personas**: Tailored content for different types of tea drinkers
- **Smart Features Showcase**: Detailed explanation of intelligent app capabilities
- **Privacy Policy**: Comprehensive privacy policy with detailed iCloud information
- **Contact Page**: Contact information and support
- **Mobile Responsive**: Optimized for iPhone and iPad viewing
- **App Store Ready**: Professional design meeting Apple's standards

## Development

This website is built with [Hugo](https://gohugo.io/) static site generator.

### Local Development

1. Install Hugo (v0.128.0+extended or later)
2. Clone this repository
3. Run the development server:
   ```bash
   hugo server
   ```
4. Visit `http://localhost:1313`

### Building for Production

```bash
hugo
```

The generated site will be in the `public/` directory.

### Project Structure

```
├── content/           # Page content
│   ├── _index.md     # Homepage content (uses shortcodes)
│   ├── contact/      # Contact page
│   └── privacy-policy/ # Privacy policy
├── layouts/          # HTML templates
│   ├── index.html    # Homepage template (simplified structure)
│   ├── _default/     # Default page templates
│   ├── partials/     # Reusable template components
│   │   ├── head.html # HTML head with meta tags and CSS
│   │   └── footer.html
│   └── shortcodes/   # Reusable content components
│       ├── hero-banner.html        # Enhanced hero with download button
│       ├── problem-solution.html   # Problem/solution messaging
│       ├── smart-feature.html      # Individual smart feature
│       ├── smart-features-section.html # Smart features container
│       ├── persona-card.html       # User persona card
│       ├── user-personas.html      # User personas container
│       ├── key-feature.html        # Key feature item
│       ├── key-features-grid.html  # Key features container
│       ├── download-cta.html       # Download call-to-action
│       ├── feature-card.html       # Legacy feature card
│       ├── hero-intro.html         # Legacy hero intro
│       ├── features-section.html   # Legacy features section
│       ├── why-card.html           # Why choose card
│       └── why-section.html        # Why choose container
├── static/           # Static assets (images, CSS, etc.)
│   ├── css/
│   │   └── main.css  # Main stylesheet
│   └── logo.png
└── hugo.toml         # Hugo configuration
```

### Configuration

Site configuration is managed in `hugo.toml`:

- **Site metadata**: Title, description, author
- **Footer settings**: Copyright year and footer links
- **Build settings**: Markup configuration and disabled features

### Styling

The site uses an iOS-inspired, modern CSS architecture:

- **External stylesheet**: All styles are in `static/css/main.css`
- **iOS Design Language**: Clean, modern styling with rounded corners and gradients
- **Responsive design**: Mobile-first approach optimized for iPhone and iPad
- **Modern CSS**: Uses CSS Grid, Flexbox, and advanced CSS features
- **Performance optimized**: Single CSS file, minimal HTTP requests
- **Accessibility**: Good contrast ratios and readable typography
- **Interactive Elements**: Hover effects and smooth transitions

### Shortcodes

The homepage uses Hugo shortcodes for modular content management and better content/presentation separation:

#### Primary Content Shortcodes
- `{{< hero-banner >}}` - Enhanced hero section with gradient background and download button
- `{{< problem-solution >}}` - Problem/solution messaging section
- `{{< smart-features-section >}}` - Container for intelligent app features
- `{{< smart-feature >}}` - Individual smart feature with icon, title, highlight, and description
- `{{< user-personas >}}` - Container for user persona cards
- `{{< persona-card >}}` - Individual user persona with icon and content
- `{{< key-features-grid >}}` - Grid layout for key features
- `{{< key-feature >}}` - Individual key feature item
- `{{< download-cta >}}` - Call-to-action section with App Store download button
- `{{< why-section >}}` - Container for "why choose" cards
- `{{< why-card >}}` - Individual reason card

#### Legacy Shortcodes (maintained for compatibility)
- `{{< hero-intro >}}` - Original hero section
- `{{< features-section >}}` - Original feature cards container
- `{{< feature-card >}}` - Original feature card

#### Shortcode Features
- **Flexible Parameters**: Most shortcodes accept customizable titles, icons, and content
- **Responsive Design**: All shortcodes are mobile-optimized
- **Consistent Styling**: Unified design language across all components
- **Easy Maintenance**: Content updates don't require HTML/CSS knowledge

#### App Store Integration
The `download-cta` shortcode supports easy switching from "coming soon" to live App Store links:

**Coming Soon Mode (current):**
```markdown
{{< download-cta title="Download TeaLixir Today" status="coming-soon" >}}
Available now on the App Store for iPhone and iPad.
{{< /download-cta >}}
```

**Live App Store Mode (when published):**
```markdown
{{< download-cta title="Download TeaLixir Today" status="available" app_id="1234567890" >}}
Available now on the App Store for iPhone and iPad.
{{< /download-cta >}}
```

**Alternative with full URL:**
```markdown
{{< download-cta title="Download TeaLixir Today" status="available" app_store_url="https://apps.apple.com/app/tealixir/id1234567890" >}}
Available now on the App Store for iPhone and iPad.
{{< /download-cta >}}
```

**Parameters:**
- `status`: "coming-soon" (default) or "available"
- `app_id`: App Store ID number (generates standard App Store URL)
- `app_store_url`: Full App Store URL (alternative to app_id)
- `title`: Section title
- `subtitle`: Optional subtitle text
