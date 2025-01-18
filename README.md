# React Router v6 Catch-all Route Issue

This repository demonstrates a subtle issue with catch-all routes (`/*`) in React Router v6.  The catch-all route unexpectedly intercepts routes that should be handled by other, more specific routes.

## Problem

The `/*` route, intended to handle 404 errors, is overriding other defined routes.  This is particularly problematic when routes are defined with parameters or are nested.

## Solution

The solution involves carefully ordering routes, ensuring that more specific routes are placed *before* the catch-all route. This forces React Router to evaluate more specific matches first.