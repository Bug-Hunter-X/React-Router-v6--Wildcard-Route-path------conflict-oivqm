# React Router v6 Wildcard Route Conflict

This repository demonstrates a common issue encountered when using wildcard routes ("*" or path="/*") in React Router v6.  The problem arises when a wildcard route is placed after more specific routes. Even when navigating to valid routes, the wildcard route may still be matched, resulting in an unexpected 404 page.

## Problem Description
The wildcard route `/` catches every path, and it is always matched before other routes. This makes other routes not be matched.

## Solution
The solution involves reordering the routes, placing the wildcard route at the end of the `Routes` component, after any other more specific routes.

## How to Reproduce
1. Clone the repository
2. Run `npm install`
3. Run `npm start`
4. Observe that even when navigating to `/about`, the `/` route will match. 