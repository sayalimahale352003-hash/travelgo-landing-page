# Accessibility Audit Report – AdventureX

## 1. Project Information

**Website:** AdventureX Landing Page  
**Live Website:** https://sayalimahale352003-hash.github.io/travelgo-landing-page/  
**Accessibility Tool:** WAVE Web Accessibility Evaluation Tool  
**Target Standard:** WCAG 2.1 AA

---

## 2. Objective

The objective of this accessibility audit was to identify and fix accessibility issues in the AdventureX landing page so that the website is more usable for people who use screen readers, keyboard-only navigation, and users with visual impairments.

The website was tested using the WAVE accessibility evaluation tool and manual keyboard navigation.

---

## 3. Before Accessibility Audit

The initial WAVE audit identified the following issues:

| Issue | Before |
|---|---:|
| Errors | 5 |
| Contrast Errors | 13 |
| Alerts | 1 |
| Features | 14 |
| Structure | 31 |
| AIM Score | 5.2/10 |

### Issues Identified

#### 1. Empty Button
The mobile navigation button did not have an accessible name.

**Fix:** Added an accessible label and ARIA state:

```html
<button class="menu-btn"
        aria-label="Open navigation menu"
        aria-expanded="false">
    <i class="fa-solid fa-bars" aria-hidden="true"></i>
</button>

#### 2. Empty Links

The social media links contained icons but did not have accessible names for screen reader users.

**Fix:** Added descriptive aria-label attributes and marked the decorative icons as hidden from screen readers:

<div class="social-links">
    <a href="#" aria-label="Facebook">
        <i class="fab fa-facebook-f" aria-hidden="true"></i>
    </a>

    <a href="#" aria-label="Instagram">
        <i class="fab fa-instagram" aria-hidden="true"></i>
    </a>

    <a href="#" aria-label="Twitter">
        <i class="fab fa-twitter" aria-hidden="true"></i>
    </a>

    <a href="#" aria-label="LinkedIn">
        <i class="fab fa-linkedin-in" aria-hidden="true"></i>
    </a>
</div>
