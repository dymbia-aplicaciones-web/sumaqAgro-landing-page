# Contributing to SumaqAgro Landing Page

Thank you for contributing to the SumaqAgro landing page!

This project is developed by Dymbia for the Aplicaciones Web course at Universidad Peruana de Ciencias Aplicadas (UPC).

This document defines the project structure, coding conventions, Git workflow, and review process for maintaining a consistent and accessible website.

---

## Table of Contents

1. [Project Structure](#project-structure)
2. [Development Setup](#development-setup)
3. [Git Workflow](#git-workflow)
4. [Conventional Commits](#conventional-commits)
5. [Coding Guidelines](#coding-guidelines)
6. [Internationalization](#internationalization)
7. [Accessibility and Responsive Design](#accessibility-and-responsive-design)
8. [Assets and Legal Pages](#assets-and-legal-pages)
9. [Semantic Versioning](#semantic-versioning)
10. [Quality Assurance](#quality-assurance)
11. [Pull Request Process](#pull-request-process)

---

## Project Structure

The landing page uses HTML5, CSS3, and JavaScript vanilla.

```text
sumaqAgro-landing-page/
├── public/
│   ├── assets/
│   │   ├── css/
│   │   │   └── styles.css
│   │   ├── fonts/
│   │   ├── images/
│   │   └── js/
│   │       ├── i18n/
│   │       │   ├── en.js
│   │       │   └── es.js
│   │       └── script.js
│   └── sections/
│       ├── cookie.html
│       ├── policy.html
│       └── service.html
├── .gitignore
├── CHANGELOG.md
├── CONTRIBUTING.md
├── index.html
├── LICENSE.md
├── package.json
└── README.md
```

### Responsibilities

- `index.html`: Main landing page content and structure.
- `styles.css`: Shared styles, layouts, and responsive rules.
- `script.js`: Navigation, language selection, pricing, and application initialization.
- `i18n/en.js` and `i18n/es.js`: English and Spanish translation dictionaries.
- `public/sections/`: Privacy Policy, Terms of Service, and Cookie Policy pages.
- `public/assets/images/`: Images and video assets.

---

## Development Setup

### Prerequisites

- Git.
- A code editor.
- A modern web browser.
- A local static web server.

### Clone the Repository

```bash
git clone https://github.com/dymbia-aplicaciones-web/sumaqAgro-landing-page.git
cd sumaqAgro-landing-page
```

Serve the repository root using a local static server, such as the Live Server extension for Visual Studio Code.

Alternatively, with Python installed:

```bash
python -m http.server 8080
```

Open:

```text
http://localhost:8080
```

Serving the repository root makes `index.html` and the `public/` directory available together.

### Available Scripts

Check `package.json` before running project commands.

Only use development, build, lint, or test commands when their corresponding scripts are defined.

A placeholder test script must not be treated as an automated test suite.

---

## Git Workflow

Use the following branches:

- `main`: Stable release branch.
- `develop`: Integration branch.
- `feature/<short-description>`: Features, enhancements, and documentation.
- `bugfix/<short-description>`: Non-urgent corrections.
- `release/v<version>`: Release preparation.
- `hotfix/<short-description>`: Urgent corrections to the stable version.

Create feature and bugfix branches from `develop`. Submit their pull requests to `develop`.

### Branch Examples

```text
feature/repository-documentation
feature/landing-page-fixes
feature/team-video
bugfix/language-switcher
bugfix/mobile-navigation
```

### Starting a Contribution

Commit or stash existing local changes before switching branches.

```bash
git switch develop
git pull origin develop
git switch -c feature/short-description
```

Keep each branch focused on a related set of changes.

---

## Conventional Commits

Use the following format:

```text
<type>: <short description>
```

A scope is optional:

```text
<type>(<scope>): <short description>
```

Write concise descriptions in English using the imperative mood. General messages are acceptable when they clearly describe the change.

### Commit Types

| Type | Purpose |
|---|---|
| `feat` | Add functionality. |
| `fix` | Correct a defect. |
| `docs` | Update documentation. |
| `style` | Change code formatting without changing behavior. |
| `refactor` | Restructure code without changing functionality. |
| `perf` | Improve performance. |
| `test` | Add or update tests. |
| `build` | Update dependencies or build configuration. |
| `ci` | Update continuous integration configuration. |
| `chore` | Perform maintenance tasks. |

### Examples

```text
feat: add new sections
fix: correct navigation behavior
docs: update project documentation
refactor: organize application code
chore: clean up unused assets
```

Use `docs` for documentation-only changes.

---

## Coding Guidelines

### HTML

- Use semantic elements such as `header`, `nav`, `main`, `section`, and `footer`.
- Maintain a logical heading hierarchy.
- Keep IDs unique and consistent with navigation links.
- Use buttons for actions and links for navigation.
- Keep asset paths correct relative to each HTML file.
- Preserve translation attributes when editing localized content.

### CSS

- Maintain shared styles in `public/assets/css/styles.css`.
- Follow existing class naming conventions.
- Reuse existing colors, typography, spacing, and component styles.
- Prefer reusable classes over repeated inline styles.
- Check that changes do not unintentionally affect other sections or legal pages.
- Ensure layouts remain usable on desktop and mobile screens.

### JavaScript

- Maintain website interactions in `public/assets/js/script.js`.
- Use `const` by default and `let` when reassignment is necessary.
- Use descriptive `camelCase` names for functions and variables.
- Keep initialization functions focused on their responsibilities.
- Check that elements exist before attaching page-specific behavior.
- Ensure shared scripts work on the landing page and legal pages.
- Keep visual states and accessibility attributes synchronized.

---

## Internationalization

The website supports English and Spanish through:

```text
public/assets/js/i18n/en.js
public/assets/js/i18n/es.js
```

### Translation Rules

- Add matching translation keys to both dictionaries.
- Follow the existing `window.i18nDictionary` structure.
- Connect translated HTML content through `data-i18n`.
- Use descriptive keys consistent with existing sections.
- Preserve the selected language through the `preferredLang` local storage key.
- Update `document.documentElement.lang` when switching languages.
- Keep pricing labels consistent with the selected language and billing period.
- Check translations on the landing page and legal pages.

### Example

```html
<h2 data-i18n="demo_title">See SumaqAgro in action</h2>
```

Only include trusted, project-controlled markup in translation values when inserting content through `innerHTML`.

---

## Accessibility and Responsive Design

- Provide descriptive alternative text for informative images.
- Use empty `alt` attributes for decorative images.
- Preserve skip-to-content navigation.
- Ensure controls can be operated with a keyboard.
- Maintain visible keyboard focus indicators.
- Update `aria-expanded` when opening or closing navigation.
- Update `aria-pressed` when changing billing selection.
- Provide visible labels or accessible names for controls.
- Aim for WCAG AA color contrast.
- Prevent horizontal overflow on small screens.
- Provide captions or transcripts for spoken video content.

---

## Assets and Legal Pages

### Images and Videos

- Store assets in the appropriate directory under `public/assets/`.
- Use descriptive, lowercase, hyphen-separated filenames for new assets.
- Optimize image and video sizes before committing.
- Update references when renaming or moving assets.
- Confirm that assets are authorized for use and distribution.
- Verify video playback and controls.
- Remove assets only after confirming they are no longer referenced.

### Legal Pages

- Maintain shared styles and branding.
- Preserve relative links to the homepage, assets, and scripts.
- Add matching English and Spanish translations for changed content.
- Keep descriptions of data collection and storage consistent with website behavior.
- Coordinate changes to legal commitments and licensing with project maintainers.

---

## Semantic Versioning

Use the following version format:

```text
MAJOR.MINOR.PATCH
```

- **MAJOR:** Changes that break established public behavior or integrations.
- **MINOR:** Backward-compatible features.
- **PATCH:** Backward-compatible defect corrections.

Update `package.json` and `CHANGELOG.md` when preparing a release.

Use the appropriate changelog categories:

- `Added`
- `Changed`
- `Deprecated`
- `Removed`
- `Fixed`
- `Security`

Include only categories containing actual changes. Record release dates and version details accurately.

---

## Quality Assurance

Complete the relevant manual checks before submitting a pull request. Run automated checks when available.

### Manual Verification

- Open the landing page through a local static server.
- Verify desktop and mobile layouts.
- Test navigation links and mobile menu behavior.
- Switch between English and Spanish.
- Reload the page and confirm language persistence.
- Test monthly and annual pricing in both languages.
- Verify savings badge interaction with the mouse and keyboard.
- Open legal pages and test navigation and language controls.
- Confirm that images and videos load correctly.
- Check keyboard navigation and visible focus states.
- Inspect the browser console for JavaScript errors.
- Check the network panel for missing assets.

Confirm that registration and sign-in links match the intended web application deployment.

---

## Pull Request Process

Before submitting a pull request:

- [ ] Keep changes focused on a clear purpose.
- [ ] Follow existing coding conventions.
- [ ] Use Conventional Commits.
- [ ] Add matching translations when needed.
- [ ] Verify desktop and mobile layouts.
- [ ] Check keyboard interaction and accessibility attributes.
- [ ] Confirm that assets and links resolve correctly.
- [ ] Complete relevant validation.
- [ ] Update documentation and the changelog when appropriate.
- [ ] Target `develop` for feature and bugfix contributions.

### Pull Request Description

Include:

- The problem or requirement addressed.
- A brief description of the changes.
- Screenshots for visible interface changes.
- Validation performed.
- Any remaining limitations.

Request a maintainer review before merging.

---

Developed by Dymbia for the Aplicaciones Web course at UPC.