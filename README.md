# BrilliantPala Fullscreen Wrapper

A minimal static page that embeds https://brilliantpala.base44.app/ edge-to-edge.

## Deploy
Publish the repository root as a static site (GitHub Pages, Cloudflare Pages, Netlify, etc.). No build command is required; the entry point is `index.html`.

## Orientation behavior
- Tap **Open fullscreen** to enter fullscreen and request landscape orientation.
- Orientation locking is only available in browsers that support the Screen Orientation API and generally requires a user gesture.
- A CSS rotation fallback is applied where possible when the device remains in portrait.

## Important browser limitation
The embedded app must allow framing. If Base44 sends `X-Frame-Options` or a restrictive `Content-Security-Policy: frame-ancestors` header, the browser will block the iframe. This wrapper cannot override that server-side security policy. In that case, enable embedding in the app host settings or use the host's supported embed feature.

Camera/microphone permissions are delegated to the iframe via its `allow` attribute; the browser may still ask the user for permission.
