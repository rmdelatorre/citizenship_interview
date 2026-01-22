# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

A U.S. Citizenship Test interview simulator - a standalone HTML file that runs entirely in the browser with no build step. Deployed via GitHub Pages at https://rmdelatorre.github.io/citizenship_interview/

## Architecture

Single-file React application (`index.html`) using CDN-loaded dependencies:
- React 18 (via unpkg CDN)
- Babel standalone for JSX transformation in-browser
- Tailwind CSS (via CDN)
- Lucide icons (inline SVG components)

All code, styles, and data are contained in one file. No npm, no build process, no server required.

## Key Components

- `QUESTIONS` array (lines 60-161): Contains all 100 official USCIS civics questions with accepted answers
- `CitizenshipTest` component: Main app with three states - intro, testing, results
- `checkAnswer()`: Fuzzy answer matching that handles number normalization, plurals, and multi-answer questions

## Development

Open `index.html` directly in a browser or use any local server. Changes are visible on page refresh.

## State-Specific Questions

Questions 20, 23, 80, 83, 100, 103, 104, 106, 107 contain state-specific answers (currently set for New York). These may need updating for other states or when officials change.
