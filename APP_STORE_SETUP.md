# App Store Setup Guide

This guide explains how to update the TeaLixir website when the app goes live on the App Store.

## Current Status: Coming Soon

The website currently shows "Coming Soon to the App Store" using this configuration in `content/_index.md`:

```markdown
{{< download-cta title="Download TeaLixir Today" subtitle="Stop buying tea you don't like. Start building a collection you love." status="coming-soon" >}}
Available now on the App Store for iPhone and iPad.

*TeaLixir - Because every cup should be perfect.*
{{< /download-cta >}}
```

## When App Goes Live: Update Instructions

### Option 1: Using App Store ID (Recommended)

Once you have your App Store ID (e.g., 1234567890), update the shortcode in `content/_index.md`:

```markdown
{{< download-cta title="Download TeaLixir Today" subtitle="Stop buying tea you don't like. Start building a collection you love." status="available" app_id="1234567890" >}}
Available now on the App Store for iPhone and iPad.

*TeaLixir - Because every cup should be perfect.*
{{< /download-cta >}}
```

This will automatically generate the URL: `https://apps.apple.com/app/id1234567890`

### Option 2: Using Full App Store URL

If you prefer to use the complete URL:

```markdown
{{< download-cta title="Download TeaLixir Today" subtitle="Stop buying tea you don't like. Start building a collection you love." status="available" app_store_url="https://apps.apple.com/app/tealixir/id1234567890" >}}
Available now on the App Store for iPhone and iPad.

*TeaLixir - Because every cup should be perfect.*
{{< /download-cta >}}
```

## Finding Your App Store ID

1. Go to App Store Connect
2. Navigate to your app
3. The App Store ID is shown in the app information section
4. It's also visible in the App Store URL once your app is live

## Testing

After making changes:

1. Run `hugo` to build the site
2. Check that the download button links to the correct App Store page
3. Verify the button opens in a new tab and has proper accessibility attributes

## Deployment

1. Update the content file as shown above
2. Build the site: `hugo`
3. Deploy the `public/` directory to your hosting platform

The change is immediate - no code changes required, just content updates!
