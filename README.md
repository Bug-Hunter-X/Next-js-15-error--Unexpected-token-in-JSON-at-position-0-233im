# Next.js 15 Unexpected Token Error in JSON

This repository demonstrates a bug in Next.js 15 where using server components with dynamic routes containing wildcards in the file system path causes an unexpected token error during JSON parsing.  The issue occurs specifically when there's a mismatch between how the client-side route is handled and how the server component attempts to access it.

## Steps to Reproduce

1. Clone this repository.
2. Install dependencies: `npm install`
3. Run the development server: `npm run dev`
4. Navigate to a route that triggers the wildcard.  You will encounter the error.  Refer to `index.js` for more detail on the setup.

## Workaround

A solution involves adjusting the path resolution within the server component to correctly handle the dynamic route.  The solution implementation is shown in `index.solution.js`

## Expected Behavior

The application should render correctly without throwing an error, regardless of the dynamic route segment containing wildcards.