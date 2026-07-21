## Week 7 — Issue selection

**Issue link:** [\[paste link here\]](https://github.com/ascherj/pathreview/issues/57)

**Issue title:** Add a mock GitHub API server for integration tests

**Tier:** [ ] Tier 1  [x] Tier 2  [ ] Tier 3

**Problem summary:**
AI Agent tests are skipping GitHub tooling tests because live API access is required. To get around this limitation, a mock API server needs to be setup. Files to setup: 
tests/integration/test_github_tool.py
tests/fixtures/github_responses/

Success will have tests for the GitHub server work with a mock server. 
**Branch name:** [paste branch name here]

**Setup confirmation:** [x] App runs locally at localhost:5173
(Linux only, Windows still having some issues.)
**Cohort ledger:** [x] Issue added to cohort ledger

**Issue Fit and Selection**
I have worked with multple interlinked systems before and can intergrate them toegeher. I have also setup mock API servers and can get pytests to run with them. I am okay with the 3-4 others working on the issue and estimate I can complete before week 9.