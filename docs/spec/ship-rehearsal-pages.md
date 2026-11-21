---
title: Ship rehearsal pages
license: CC0-1.0
lifecycle: ai-full
---

## Problem

The `pages-deploy` recipe of the `ship` stage has never run against a real GitHub Pages site. Its tests use fakes, so nobody yet knows how long GitHub takes to serve a deploy, whether `.nojekyll` is served, or how long the CDN serves an older copy. The Hee-Lee Oss maintainers need to see one real deploy shipped and fetched back before any real publication.

## Beneficiary

The Hee-Lee Oss maintainers. This is an internal rehearsal with no outside beneficiary. The output is one tiny web page and a record of what happened, reached through this repository's Pages site.

## Scope

One page, `site/index.html`, for milestone M1. The milestone is read, covered and shipped as a Pages deploy of this repository, and the page is fetched back from its public address and compared.

## Non-goals

No real publication, no site and no content that anyone is meant to read. Nothing in this project is delivered to anyone.

## Acceptance criteria

| AC | Case | Required evidence |
|---|---|---|
| AC-01 | `site/index.html` is a page whose body holds the line "rehearsal pages" | The file at the tip of the default branch |

## Inputs and provenance

None
