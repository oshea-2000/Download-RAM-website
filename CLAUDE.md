# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

RAMDirect is a satirical parody website based on the classic internet joke "download more RAM." It presents a fake SaaS-style landing page with psychological dark patterns commonly used by real SaaS sites, all offering free downloads of RAM, CPU cores, storage, and bundle packages.

## Running the Project

Open `index.html` directly in a browser. No build step, server, or dependencies required.

## Architecture

Single self-contained HTML file (~1700 lines) with:
- **Embedded CSS**: CSS custom properties for theming, responsive layouts, tabs, modals, toasts
- **HTML structure**: Nav, hero with urgency timer, tabbed product categories, how-it-works, testimonials, FAQ, footer, modals
- **Embedded JavaScript**: Tab switching, subscription toggle, download simulation, activity notifications, exit-intent popup

## Product Categories (Tabbed Interface)

| Tab | Products | Price Range |
|-----|----------|-------------|
| RAM | 5 tiers (8GB-128GB) | $49-$499 |
| CPU Cores | 4 tiers (2-16 cores) | $29-$199 |
| Storage | 4 tiers (256GB-10TB) | $29-$299 |
| Bundles | 4 packages | $177-$997 |

All products marked as "Free" with struck-through retail prices.

## Psychological Dark Patterns (Satirical)

- **Urgency timer**: 15-minute localStorage-persisted countdown
- **Activity notifications**: Random toast popups ("Sarah from Austin just downloaded 32GB RAM")
- **Price anchors**: Struck-through "retail" prices above Free
- **Micro-commitment checkboxes**: Required before download button enables
- **Exit-intent popup**: Triggers when mouse leaves toward browser chrome
- **Subscription toggle**: Free vs Premium (both $0/mo - the joke)

## Styling Notes

CSS custom properties in `:root`:
- `--primary`: #0a2540 (dark blue)
- `--accent`: #00d4aa (teal/green)
- `--surface`: #f6f9fc (light background)
