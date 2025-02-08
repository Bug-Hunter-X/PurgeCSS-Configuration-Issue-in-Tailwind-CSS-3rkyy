# PurgeCSS Configuration Issue in Tailwind CSS

This repository demonstrates an uncommon bug related to PurgeCSS configuration in Tailwind CSS. The issue stems from an incorrect configuration that leads to missing styles in the production build, impacting layout and functionality.

## Problem

The `tailwind.config.js` file contains an incomplete PurgeCSS configuration. This results in inconsistencies with the styles applied, sometimes missing or including unexpected classes.   This is specifically a problem when using the `content` array for specifying files. The issue is subtle and is difficult to track down if the project is larger. This example isolates the core of the problem.

## Solution

The `tailwind.config.fixed.js` file provides the corrected configuration.  The key is ensuring that `content` array correctly points to all the template files where Tailwind CSS classes are used.  Using globbing patterns helps to accommodate multiple files within subdirectories. 

## How to Reproduce

1. Clone the repository
2. Run `npm install`
3. Observe the missing styles in the original configuration file.  
4. Replace the `tailwind.config.js` with `tailwind.config.fixed.js` and see the corrected output.