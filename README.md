# TeaLixir Website

This is the official website for the TeaLixir iOS app - an intelligent tea tracking app that helps users discover, track, and enjoy their perfect cup of tea.

## About TeaLixir

TeaLixir is a comprehensive tea tracking app for iOS that features:
- Comprehensive tea tracking with photos and detailed information
- Recommendations based on user preferences
- Simplified data entry with photo recognition
- Secure iCloud sync across devices

## Website Features

- **Landing Page**: Clean, modern design showcasing app features
- **Privacy Policy**: Comprehensive privacy policy covering both app and website
- **Contact Page**: Contact information and FAQ
- **Mobile Responsive**: Optimized for all device sizes
- **App Store Ready**: Designed to meet Apple App Store submission requirements

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
│   ├── index.html    # Homepage template
│   ├── _default/     # Default page templates
│   ├── partials/     # Reusable template components
│   │   ├── head.html # HTML head with meta tags and CSS
│   │   └── footer.html
│   └── shortcodes/   # Reusable content components
│       ├── feature-card.html
│       ├── hero-intro.html
│       ├── features-section.html
│       └── why-section.html
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

The site uses a clean, modern CSS architecture:

- **External stylesheet**: All styles are in `static/css/main.css`
- **No inline CSS**: Clean separation of content and presentation
- **Responsive design**: Mobile-first approach with media queries
- **Modern CSS**: Uses CSS Grid, Flexbox, and CSS custom properties
- **Performance optimized**: Single CSS file, minimal HTTP requests

### Shortcodes

The homepage uses Hugo shortcodes for better content/presentation separation:

- `{{< hero-intro >}}` - Hero section with title, subtitle, and description
- `{{< features-section >}}` - Container for feature cards
- `{{< feature-card >}}` - Individual feature with icon, title, and bullet points
- `{{< why-section >}}` - Container for "why" cards
- `{{< why-card >}}` - Individual reason card
