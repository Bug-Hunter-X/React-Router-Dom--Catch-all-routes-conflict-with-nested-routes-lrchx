# React Router Dom: Catch-all Route Conflict

This repository demonstrates a common issue with React Router's catch-all routes (`/*`) when used in conjunction with nested routes. The catch-all route, intended to handle all unmatched paths, can unintentionally override more specific nested routes, preventing them from being accessed.

## Problem
The provided `App.js` contains a catch-all route (`/*`) that is defined before a nested route, and as a result, the nested route will never be matched.

## Solution
The solution (`AppSolution.js`) places the catch-all route after all other routes.  This ensures that only paths that do not match any other route will be handled by the catch-all.