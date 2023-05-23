# 1. Playwright as E2E framework

Date: 2023-05-23

## Status

proposed

## Context

Our current E2E testing strategy with Selenium has the following issues:
* **Configurations and tests are complex to write and maintain** and this leads to outdated tests and low engagement in the community, with low quality as result.
* **Documentation is not reliable**, some examples for the more advanced features are not clear and sometimes missleading.
* **Some test implementations are flaky**, even following the best practices sometimes the test results are inconsistent.

Given this context, the community discussed the current state of the art of E2E frameworks and work on a PoC for the most popular ones:
* [Cypress](https://www.cypress.io/app/) and [Cypress Cloud Solution](https://www.cypress.io/cloud/)
* [PlayWright](https://playwright.dev/) on our current Jenkins CI

## Decision

After reviewing the PoC, the community decided that PlayWright is more suited for our currently needs because the following reasons:
* Migration from Selenium to Playwright is easy and doesnt implies any new SaaS cost.
* Playwright supports visual comparisons, snapshots, videos and traces for free.
* Playwright is language independant and gets by default JS/TS, Python, C# and Java support. 
* Playwright [fixtures](https://playwright.dev/docs/test-fixtures) and JS async/await pattern makes very easy to write tests.
* Playwright provides paralelisation for free. Cypress only in the SaaS cloud version.
* Cypress is not able to work with multipage. Playwright has the ability to test across multiple pages and domains.

## Consequences

* Due to the simplicity of this new framework, the engagement with E2E should improve after this changes.
