# BrilliantPala iframe

A minimal static page that displays https://brilliantpala.base44.app/ in a full-page iframe.

## Deploy

Publish the repository root as a static site. No build command is required; the entry point is `index.html`.

## Note

The embedded site must allow iframe embedding. If its server sends restrictive `X-Frame-Options` or `Content-Security-Policy: frame-ancestors` headers, the browser will block it.
