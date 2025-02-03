# React Router Dom v6 Catch All Route Issue

This repository demonstrates a common issue encountered when using the catch-all route (`/*`) in React Router Dom v6. The catch-all route, intended to handle unmatched paths, seems to override other defined routes, preventing them from working correctly.  The solution shows how to correctly implement it and prevent such overriding behaviors.

## Problem

The provided `App.js` shows a simple React Router setup.  Despite having specific routes defined (`/` and `/about`), the catch-all route (`/*`) always triggers, displaying the 404 page even when navigating to valid paths like `/` or `/about`.

## Solution

`AppSolution.js` provides the correct implementation. The solution is to place the catch all route as the last route. That way, React Router will match all other routes first before falling back to this catch-all route if no other route matches.