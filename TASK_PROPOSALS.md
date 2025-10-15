# Proposed Maintenance Tasks

## Typo Fix
- **Location:** `index.html`, "Areas of Interest" card for cloud computing.
- **Issue:** "Azure Solutions Architecure" is misspelled; should be "Azure Solutions Architecture".
- **Suggested Fix:** Correct the spelling to improve professionalism and search indexing.

## Bug Fix
- **Location:** `assets/js/main.js`, scrolly initialization.
- **Issue:** The code references `$navbar.outerHeight()` without defining `$navbar`, which throws a `ReferenceError` and breaks the smooth scrolling offset.
- **Suggested Fix:** Define `$navbar` (e.g., `var $navbar = $('.custom-navbar');`) before use or replace the expression with the actual selector to ensure the scrolly plugin receives a valid offset value.

## Documentation/Comment Discrepancy
- **Location:** `portfolio.html`, section comment before the project grid.
- **Issue:** The section is labeled "blog section" even though it displays portfolio project cards, causing confusion for maintainers.
- **Suggested Fix:** Update the comment (and `id` if appropriate) to reflect that the content is a portfolio/projects section.

## Test Improvement
- **Scope:** Overall site navigation behavior.
- **Issue:** The repository lacks automated coverage ensuring that key interactive behavior (e.g., nav toggle, smooth scroll) works after changes.
- **Suggested Fix:** Introduce a lightweight end-to-end test (for example, using Playwright or Cypress in CI) that loads `index.html`, toggles the hamburger menu, and confirms navigation links scroll to the correct section. This will guard against regressions like the undefined `$navbar` reference.
