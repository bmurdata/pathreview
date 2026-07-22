## Solution plan

**Issue:**Add a mock GitHub API server for integration tests  https://github.com/ascherj/pathreview/issues/57

### Understand
What is the root cause of this issue? What behavior is expected vs. actual?
Root cause is missing web server for GitHub. The expected behavior is that it tests for GitHub and it does not do that.
### Map
Which files, functions, or modules are involved?
List the specific files you expect to touch.
Files I will need to add:
tests/integration/test_github_tool.py
This file should have setup script for the HTTP server and environment for the application.

tests/fixtures/github_responses/

This folder should have responses that are called. I will have to review this later
### Plan
What are the steps to fix this issue?
Break it into 3–5 concrete sub-tasks.
Check and test current testing suite
Create pytest file to create a HTTP server for GitHub
Create test cases as in other test suites.
### Inputs & outputs
What does your fix take as input? What should it produce or change?

### Risks & unknowns
What could go wrong? What are you still unsure about?
Testing suite could break or the AI tests could run into an infinite loop.
### Edge cases
What inputs or states should your fix handle gracefully?