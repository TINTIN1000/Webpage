# Byron Museza — Personal Profile Website

A semantic HTML5 personal profile webpage showcasing my background, skills, software engineering interests, and contact information.

## Project Features

- Semantic HTML5 structure
- Personal profile and background information
- Skills section
- Contact form
- Native HTML5 form validation
- Accessible image alternative text
- Properly associated form labels
- Responsive viewport configuration
- AI-assisted content documented in `PROMPT_LOG.md`

## Technologies Used

- HTML5
- Git
- GitHub

## Semantic HTML5 Elements

The page uses the following semantic HTML5 elements:

- `<header>` — contains my profile information and navigation.
- `<nav>` — provides navigation links to sections of the page.
- `<main>` — contains the primary page content.
- `<section>` — organizes the About, Background, Skills, and Contact content.
- `<article>` — contains information about my approach to software development.
- `<aside>` — contains information about what I am currently learning.
- `<footer>` — contains copyright and contact information.

## Contact Form

The Contact Me form uses native HTML5 validation.

The form includes:

- Text input for Full Name
- Email input for Email Address
- Telephone input for Phone Number
- Textarea for Message

Validation attributes include:

- `required`
- `type="email"`
- `pattern`
- `minlength`

No JavaScript is required for the basic form validation.

## AI-Assisted Content

The AI prompt, raw AI response, edited version, and reflection are documented in:

`PROMPT_LOG.md`

## Accessibility Review

### Peer Review Issue

During the peer review, the navigation structure was identified as an accessibility and HTML structure issue because the navigation links were placed inside a `<div>` without a proper unordered list structure.

### Fix Applied

I changed the navigation structure so that the navigation links are contained inside a semantic `<ul>` element with individual `<li>` elements. I also kept the `<nav>` element and added an accessible `aria-label` to identify the primary navigation.

I also ensured that the profile image has meaningful alternative text and that every form field has an associated `<label>`.

## Version Control

The project was developed using Git with incremental commits.

Example commit history:

1. `Create semantic HTML5 profile structure`
2. `Add contact form and native validation`
3. `Fix navigation and heading hierarchy`
4. `Add project documentation and prompt log`

## How to Run

1. Clone or download the repository.
2. Make sure `index.html` and `Profile.jpg` are in the correct location.
3. Open `index.html` in a web browser.

No external libraries or JavaScript are required.
