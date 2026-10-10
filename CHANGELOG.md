# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [2.0.2] - 2026-10-09

### Changed
- Updated academic references and project information.
- Updated repository links and documentation.
- Updated the product demonstration video.
- Improved overall content consistency.

## [2.0.1] - 2026-10-09

### Changed
- **Academic References:**
  - Updated course references to Aplicaciones Web.
  - Updated repository links to the `dymbia-aplicaciones-web` GitHub organization.
- **Project Documentation:**
  - Updated project information for the Aplicaciones Web course.

## [2.0.0] - 2026-10-09

### Added
- **Team Presentation:**
  - Dedicated About the Team video section with descriptive content.
  - Internationalization support for the team presentation section.
- **Internationalization:**
  - Modular English and Spanish translation dictionaries.
  - Spanish translations for legal pages.
  - Support for multiple language toggle buttons.
- **Application Initialization:**
  - Modular `initApp` function for initializing navigation, pricing, and language selection.
- **Legal Page Assets:**
  - Icons for privacy policy and terms of service pages.
- **Project Documentation:**
  - Landing page documentation in `README.md`.
  - `CHANGELOG.md` documenting project changes.
  - `LICENSE.md` with project licensing information.

### Changed
- **Project Structure:**
  - Reorganized assets under `public/assets/`.
  - Reorganized legal pages under `public/sections/`.
- **Product Demonstration:**
  - Replaced the local video player with an embedded YouTube iframe.
  - Updated styles for the product demonstration section.
- **Project Documentation:**
  - Updated README layout and project structure information.

### Fixed
- **Metadata and Content:**
  - Corrected landing page title, meta description, and keywords.
  - Updated header, hero, and About Us content.
  - Corrected team section content and positioning.
  - Updated audience, solutions, demonstration, and pricing text.
  - Corrected impact, testimonials, and call-to-action content.
- **Internationalization and Pricing:**
  - Corrected language switcher logic and billing period labels.
  - Fixed monthly and annual billing toggle behavior.
  - Corrected translated content and internationalization logic for legal pages.
- **Asset References:**
  - Corrected asset and translation paths after directory reorganization.

### Removed
- Unused SVG icons and obsolete image assets.
- Previous local product demonstration video player.

## [1.1.0]

### Added
- **Legal Pages:**
  - Privacy Policy (`public/sections/policy.html`) describing information collection,
    data usage, protection, and contact details.
  - Terms of Service (`public/sections/service.html`) covering service acceptance,
    user accounts, intellectual property, and liability.
  - Cookie Policy (`public/sections/cookie.html`) describing cookie categories
    and browser management options.
  - Shared branding, footer navigation, and language controls across legal pages.
- **Internationalization:**
  - English and Spanish language switching through `data-i18n` attributes.
  - Language dictionaries in `public/assets/js/i18n/`.
  - Language preference persistence using `localStorage`.
  - Dynamic updates to the document language and language button accessibility labels.
  - Billing period translations when changing languages.
- **Interactive Navigation:**
  - Mobile navigation toggle with dynamic `aria-expanded` states.
  - Automatic menu closure when selecting a navigation link or clicking outside the menu.
- **Interactive Pricing:**
  - Monthly and annual billing selection with dynamic price updates.
  - Annual billing selection through the savings badge.
  - Enter and Space keyboard support for the savings badge.
- **Product Demonstration:**
  - HTML5 video player referencing
    `public/assets/images/Recording-20261009_092557.webm`.

## [1.0.0]

### Added
- **Landing Page:**
  - Hero section presenting SumaqAgro and its precision agriculture value proposition.
  - About Us section describing the platform and its focus on Peruvian potato
    and coffee growers.
  - Audience cards for independent farmers, cooperative leaders, and technical advisors.
  - Solutions section presenting satellite monitoring, cost accounting,
    digital harvest quality certification, and agronomic alerts.
  - Pricing cards for Seed Plan, Cooperative Pro, and Technical Advisor Plan,
    with monthly and annual price data.
  - Impact section with agricultural metrics and user testimonials.
  - Team section with member profiles, photographs, and responsibilities.
  - About the Team video placeholder.
  - Registration calls to action and links to `/app/login` and `/app/register`.
- **Page Structure and Navigation:**
  - Header with brand identity, section navigation, and account access links.
  - Footer with product, company, support, social media, and legal navigation areas.
  - Asset organization including CSS, fonts, images, and JavaScript directories.
- **Metadata and Accessibility:**
  - Page title, description, keywords, author metadata, and Open Graph tags.
  - Favicon reference and viewport configuration.
  - Semantic HTML sections and descriptive image alternative text.
  - Skip-to-content navigation.
  - Accessible labels for navigation and interactive controls.