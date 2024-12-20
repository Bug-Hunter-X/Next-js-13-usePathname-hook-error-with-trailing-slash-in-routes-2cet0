# Next.js 13 usePathname Hook Error with Trailing Slash in Routes

This repository demonstrates a potential issue with the `usePathname` hook in Next.js 13 when a route is defined with a trailing slash. The issue arises from a breaking change introduced in Next.js 13, where routes defined with trailing slashes may behave unexpectedly.

## Problem

When using the `usePathname` hook in a page defined with a trailing slash, the path returned by `usePathname` might not be what's expected. This can lead to unexpected behavior in the application. For instance, a route defined as `/about/` might return `/about` instead.

## Solution

The most straightforward solution is to ensure that your routes are defined without trailing slashes. Alternatively, if the trailing slash is necessary, consider handling the potential discrepancy in the returned pathname using conditional logic within the component.

## Reproduction

1. Clone the repository.
2. Run `npm install` to install dependencies.
3. Run `npm run dev` to start the development server.
4. Navigate to `/about`. Observe the pathname displayed on the About page. The pathname returned will be `/about`, not `/about/`. This is the discrepancy the issue addresses.

## Additional Notes

This issue is specific to Next.js 13 and its handling of trailing slashes. It does not affect earlier versions of Next.js.

