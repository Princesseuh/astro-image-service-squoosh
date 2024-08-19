# astro-image-service-squoosh

Squoosh image service for Astro, extracted from the previously built-in image service in Astro 4.x.

Note that libsquoosh, the underlying image processing library that powers this image service is deprecated, unmaintained etc etc. Use at your own risk.

This is extracted for convenience for people migrating, I do not intend on maintaining this myself.

## What are those .wasm.ts files? Are they a backdoor?

Including WASM files in SSR bundles is impossibly hard, so we do the worst hack possible of converting them to base64 and inlining them in the source code. If you want to, you can convert the base64 strings back to binary and verify that they are indeed the WASM files you expect (or compare against the commit history of Astro before 5.x).
