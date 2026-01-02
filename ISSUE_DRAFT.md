# Optimization: Implement debouncing for search input

**Labels:** `performance`, `enhancement`, `javascript`

## Description
Implemented debouncing for the live search input in `script.js`.

The search functionality was previously triggered on every `input` event, which meant running fuzzy matching logic and DOM updates for every character typed. This is inefficient, especially for faster typists or on lower-end devices.

## Solution
I added a `debounce` utility function with a 300ms delay. The `showLiveSuggestions` function is now only called after the user stops typing for 300ms.

## Impact
This change reduces the computational load and layout thrashing without negatively impacting the user experience.

## Verification
- Verified that rapid typing no longer triggers immediate search calculations.
- Confirmed that search still functions correctly after the 300ms delay.
