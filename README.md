# TCOLE3277 Identity Theft Pre-Quiz

This repository contains a standalone interactive HTML element used in an online course for the topic represented by the repository title: identity theft prevention.

The interaction is intended to be launched from an LMS-built course as an external web asset. Because the course needs a hosted URL to deliver the experience to learners, this project is published as a static site through GitHub Pages.

## Purpose

This project exists to support a pre-course quiz experience that:

- presents learners with a short interactive assessment before or during course participation
- runs as a self-contained static HTML page
- can be linked from an LMS course using a hosted public URL
- does not require a separate application server or build pipeline

## How It Is Delivered

The learner-facing experience is served from `index.html`.

GitHub Pages is used as the hosting layer so the LMS can point learners to a stable web URL. In practice, that means:

- content is stored in this repository
- changes are pushed to the main branch
- GitHub Actions publishes the static files to GitHub Pages
- the LMS references the deployed GitHub Pages URL when launching the interaction

## Repository Contents

- `index.html`: primary learner-facing interactive quiz
- `Identity_Theft_Prevention_Pre-Course_Quiz_AssessmentStyle_Selected (2).html`: alternate or earlier HTML version retained in the repo
- `.github/workflows/`: GitHub Actions workflows related to GitHub Pages deployment

## Authoring Model

This is a static web object rather than a packaged LMS-native activity. That approach was chosen because the course itself is built in an LMS, but this interaction still needed to be delivered through a hosted URL that the LMS could open for the learner.

Using GitHub Pages gives the team a lightweight way to:

- host the interaction externally
- version the source in Git
- update the learner experience without managing separate infrastructure

## Updating The Experience

To update the interaction:

1. Edit `index.html`.
2. Commit and push the change to the repository's main branch.
3. Allow the GitHub Pages workflow to publish the updated files.
4. Confirm the hosted URL still loads correctly from the LMS course.

## Notes

- This repository is currently structured as a simple static site.
- No application framework or build tooling is required for the current implementation.
- If the LMS requires a specific launch URL, use the GitHub Pages URL that resolves to `index.html`.
