# React Router v6 Catch-all Route Issue

This repository demonstrates a common issue encountered when using catch-all routes (`/*`) in React Router v6.  The catch-all route unintentionally overrides other route matches, preventing the correct component from rendering.  The solution shows how to correctly prioritize routes to resolve this problem.

## Problem

The provided `App.js` demonstrates a simple React Router setup.  However, the catch-all route `/*` always matches, regardless of the URL, preventing the `/about` route from rendering correctly.  This is because `/*` is a broad match that matches any path.

## Solution

`AppSolution.js` provides a solution by placing the catch-all route at the end of the routes array. This ensures that it only matches paths that haven't already matched any other routes.