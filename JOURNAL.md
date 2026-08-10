## Week 7 — Issue selection

**Issue link:** https://github.com/ascherj/pathreview/issues/57

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

## Week 8 — Reproduction & solution planning

**Reproduction commit link:** https://github.com/bmurdata/pathreview/commit/290d79d1d9283261bfac60cae988131be5d3dd22

**Reproduction summary:**
Issue is that the tests do not account for GitHub tests locally. 
I verified that no such tests exist in the codebase, and none were found in the tests folder or subfolders.
The agent also has tools for GitHub that are not tested.
I plan to add intergration tests and fixtures accordingly.

**PLAN.md link:** https://github.com/bmurdata/pathreview/blob/test/57-add-mock-GitHub-test-API/PLAN.md

**Walkthrough video (recommended):** [link to your Loom video, ≤2 min — recommended, not graded]

**Blockers or open questions:**
HTTP Server intergration and exactly how to replicate the calls for GitHub mock server API.


## Week 9 — Solution building & PR submission

### Check-in 1 (mid-week)

**Current progress:**
Implemented the conftest to make the API server.
**Next steps:**
Implement the tests and testing framework using pytest httpserver.
**Blockers:**


---
### Check-in 2 (end of week)

**PR link:** [link to your submitted pull request]

**Branch:** [the branch name you worked on, e.g. `test/57-add-mock-GitHub-test-API`]

**What you built:**
Built a mock GitHub server API in conftest that calls the GitHub tool. The tool uses pytest HTTPServer to mock a GitHub server called by the tool in conftest and fixture_resolver. To get the responses, the fixture_resolver is called rathet than storing responses in GitHib_responses.
**Tests added or updated:**
To pass linter tests, tests/conftest.py and agent/tools/github_tool.py were modified. I also added a fixture_resolver to get fixtures and return a response.
**Self-review confirmation:** [x] make check passes  [x] make test-unit passes

**Draft PR feedback received from:** None