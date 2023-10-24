# Berkeley EECS Apps Guide

This is a draft of a checklist for locally developed apps.

## Documentation / Notes
- [ ] Has a `README.md`
- [ ] Has a LICESE
- [ ] CHANGELOG.md
- [ ] CONTRIBUTING.md
- [ ] Has a `docs/` folder or similar
  - [ ] Documentation should include something about roles and persmissions
- [ ] `.gitignore` should be present

## Stack & Testing
- [ ] Note the tools needs in some dependencies file (`Gemfile`, `package.json`, `requirements.txt`, etc)
- [ ] There should be automated test cases
- [ ] The tool needs to have an awareness of different environments, e.g. `development`, `test`, `staging`, `production`.
  - [ ] This should be controlled by a default variable for the language/stack like `NODE_ENV`, `RAILS_ENV`, etc.
- [ ] The app should have a `.github/` folder with a CI script
  - [ ] Should be able to run unit tests
  - [ ] Shuld run full integration tests
  - [ ] Tests should use a headless browser for some tests
- [ ] Tests should be able to run with an internet connection
- [ ] Scripts should go in a local `bin/` directory, e.g. `bin/setup`, etc.
- [ ] Local environments should require minimal secrets to boot the app
- [ ] Complicated installations should maybe have a `Dockerfile`
- [ ] Consider a local `.vscode/` configuration

## Audting and Tools
- [ ] CI should run through GitHub Actions
- [ ] Tools must have a CI Suite and should report code coverage
  - [ ] The README should include badges
- [ ] Tools should use a code linter (eslint, rubocop, pep8 / pylance, etc)
- [ ] Automatic security vuln scanning (CodeQL, snyk, brakeman, etc)
- [ ] axe accessibility auditing should run in Dev and CI
- [ ] Front end UI should default to Bootstrap unless there is good reason to deviate
- [ ] GitHub Issues / Project boards should be configured

## Deploymnets
- [ ] The tool must be able to read environment variables
- [ ] Document how are secrets shared/accessed?
- [ ] Document URLs, SSL certs needed, etc.
- [ ] the app should have a staging server which does not send out live emails
- [ ] UC Berkeley SPAs (Special Purpose Accounts) should be used for shared ownership where possible
- [ ] Tools should use Sentry for error reporting.

---

## TODO:

This repo should ideally serve as a template for CI scripts, axe configurations, notes about tools, etc.

We should eventually publish this publicly.
