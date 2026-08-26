# Portfolio Hardening Review

## Purpose

I tested my portfolio beyond the normal happy path to find broken links,
form issues, browser problems, duplicate submissions, and discoverability
issues before launch.

## 1. Where It Breaks — Findings

| Test | Result | Status | Action |
|---|---|---|---|
| Submit contact form empty | Browser validation prevents submission | Fixed | Kept required-field validation |
| Submit invalid email | Invalid email is rejected | Fixed | Added email validation |
| Submit form twice quickly | Duplicate submissions can occur | Known limitation | Needs server-side duplicate protection |
| Open portfolio on desktop browser | Works correctly | Fixed | No action needed |
| Open portfolio on mobile browser | Layout works, some spacing is tighter | Known limitation | Can improve in future |
| Click navigation links | Sections open correctly | Fixed | No action needed |
| Click GitHub links | Links open correctly | Fixed | No action needed |
| Click CV link | CV opens/downloads correctly | Fixed | No action needed |
| Submit contact form with valid data | Submission works | Fixed | No action needed |
| Open portfolio with JavaScript disabled | Some interactive behavior may be limited | Known limitation | Not required for current version |

## 2. Fix-Now Issues

The following issues were considered important enough to fix before launch:

### Invalid form input

The contact form now validates required fields and email format before
submission.

### Navigation and links

I tested the navigation, project links, GitHub link, CV link, and contact
links and fixed broken or incorrect destinations.

### SEO metadata

Basic metadata was added:

- Page title
- Meta description
- Open Graph title
- Open Graph description
- Open Graph image
- Canonical URL

## 3. Known Limitations

These issues do not block launch but are documented honestly:

1. Rapid duplicate form submissions may still require additional
   server-side protection.
2. Some mobile spacing can be improved further.
3. The portfolio currently uses a simple static structure rather than a
   full content management system.

## 4. SEO

The portfolio includes basic SEO metadata so search engines and social
platforms can understand the site.

Example:

```html
<title>Rafia Jahangir — AI & ML Engineer</title>

<meta
  name="description"
  content="Rafia Jahangir — AI & ML Engineer specializing in AI, machine learning, computer vision, NLP and software development."
/>

<meta property="og:title" content="Rafia Jahangir — AI & ML Engineer" />

<meta
  property="og:description"
  content="Portfolio of Rafia Jahangir, an AI & ML Engineer."
/>

<meta property="og:type" content="website" />
