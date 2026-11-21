---
title: Ship rehearsal pages
riskTier: low
license: CC0-1.0
lifecycle: ai-full
beneficiary: Hee-Lee Oss maintainers (a ship rehearsal fixture; no public deliverable)
definitionOfShipped: A GitHub Pages deploy of the project repository for the milestone; nothing is delivered to anyone.
reviewPolicy:
  humanCheckpoints: [spec, plan, ship]
milestones:
  - { id: M1, title: Rehearsal pages, rows: [AC-01] }
definitionOfShippedRecipe:
  kind: pages-deploy
  params:
    dir: site/
---

## Summary

A throwaway project used once to rehearse the `pages-deploy` recipe of the `ship` stage against a real GitHub Pages site. It holds one tiny page, `site/index.html`. It has no outside beneficiary.

## Scope

In scope: `site/index.html` for milestone M1, and one Pages deploy of the project repository. Out of scope: any real publication, any site or content anyone is meant to read, and any other host.

## Risk

Low. There is no personal data, no high-stakes advice, no outside beneficiary and no real deliverable. The licence is CC0-1.0 and the project's only input is one line of text written for the rehearsal. It carries no evaluators, because the sandbox half of the shipped-tree evaluation is not built, and a project that needs one cannot ship yet.

## Approach

The maintainer writes the page by hand on the donated lane and merges its pull request. The milestone then has one real coverage read, whose record is merged by a person. Before the ship, the repository's Pages is set to serve the `gh-pages` branch, which the tool never sets. `hee-lee-oss ship` is run at a terminal, with a person typing the plan's digest. It publishes the page to `gh-pages`, waits for GitHub to serve it, fetches the page back from its public address and compares the bytes, and records how long GitHub took, whether `.nojekyll` is served, and how long the CDN served an older copy.

## Definition of shipped

A Pages deploy exists for the milestone, the page fetched back from its public address matches the bytes in the repository, and `SHIPPED.md` records it. Nothing is delivered to anyone.
