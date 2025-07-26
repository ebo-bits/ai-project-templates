# Stage 3: Complete Test Coverage

<!-- Path Configuration - Update these paths if directory structure changes -->
<!-- BASE_DIR = . (current working directory) -->
<!-- AI_DIR = .ai -->
<!-- PHASE1_DIR = .ai/phase1-plan -->
<!-- PHASE2_DIR = .ai/phase2-work -->
<!-- COMMANDS_DIR = .claude/commands/wildbot/steps -->
<!--
Usage in this file:
- Feature recommendations: {PHASE1_DIR}/02-feature-recommendations.md
- Feature work: {PHASE2_DIR}/features/
- Test results and coverage reports
- Command references: {COMMANDS_DIR}/*.md
-->

This is the final stage where we ensure comprehensive test coverage and 100% passing tests.

This stage may only begin when the work stage is completed.

## Problem

We have implemented all features from the plan, but we need to ensure that:
1. We have comprehensive test coverage across all implemented functionality
2. All tests are passing (100% success rate)
3. Tests cover unit, integration, and end-to-end scenarios
4. Code quality and reliability are verified through testing

Without comprehensive testing, we cannot be confident that our implementation is correct, maintainable, or production-ready. This stage ensures that all code functions as intended and handles edge cases appropriately.

## Goals / Exit Criteria

### Goals
- Achieve 100% passing test suite across all test types
- Ensure comprehensive functional coverage of all implemented features
- Validate that all features work correctly in isolation (unit tests) and together (integration/e2e tests)
- Identify and fix any bugs, edge cases, or integration issues
- Prepare code for production deployment with confidence

### Exit Criteria
The exit criteria is to have 100% passing tests with comprehensive coverage.
You can exit the stage when:
- All unit tests are written and passing (100% success rate)
- All integration tests are written and passing (100% success rate)
- All end-to-end tests are written and passing (100% success rate)
- Test coverage meets or exceeds project standards
- All identified bugs and issues have been resolved
- A final PR has been submitted with all test improvements

### Definition of done
It is complete if the following are true:
- Condition 1: Complete test suite runs successfully with 0 failures, 0 errors
- Condition 2: Unit tests exist for all core functionality with appropriate coverage
- Condition 3: Integration tests validate feature interactions and data flow
- Condition 4: End-to-end tests verify complete user workflows
- Condition 5: All test types (unit, integration, e2e) achieve 100% pass rate
- Condition 6: Code coverage meets project requirements (typically 80%+ for critical paths)
- Condition 7: A PR has been submitted with all test improvements and fixes

## Process

### General Testing Strategy

**Start with Unit Tests, then Integration, then E2E**
- Unit tests: Test individual functions, methods, and components in isolation
- Integration tests: Test how different parts of the system work together
- End-to-end tests: Test complete user workflows and system behavior

**Don't stop until all tests are passing**
- Run the complete test suite repeatedly
- Address each failure systematically
- Iterate on both tests and implementation code as needed
- Ensure tests are reliable and not flaky

**Complete Functional Coverage**
- Every feature should have corresponding tests
- Edge cases and error conditions must be tested
- Both happy path and failure scenarios should be covered

### Step 1. Run Initial Test Assessment

Run the complete test suite to establish baseline:
```bash
# Run all tests and capture results
npm test # or appropriate test command for your project
# Document current pass/fail status
```

If any tests are failing, proceed to Step 2. If all tests pass but coverage is insufficient, proceed to Step 3.

### Step 2. Fix Failing Tests

For each failing test:
1. Analyze the failure reason (bug in code vs. bug in test)
2. Fix the underlying issue (update implementation or test)
3. Re-run the specific test to verify the fix
4. Re-run the full suite to ensure no regressions

Repeat until all existing tests pass.

### Step 3. Identify Coverage Gaps

Review each feature from `{PHASE1_DIR}/02-feature-recommendations.md`:
1. Check if unit tests exist for all core functionality
2. Check if integration tests cover feature interactions
3. Check if e2e tests cover complete user workflows
4. Identify missing test scenarios

### Step 4. Write Missing Unit Tests

For each feature lacking unit test coverage:
1. Write tests for individual functions and methods
2. Test both success and failure cases
3. Test edge cases and boundary conditions
4. Ensure tests are isolated and don't depend on external systems
5. Run unit tests and fix any failures

### Step 5. Write Missing Integration Tests

For each feature lacking integration test coverage:
1. Write tests that verify feature interactions
2. Test data flow between components
3. Test API integrations and database operations
4. Verify error handling across system boundaries
5. Run integration tests and fix any failures

### Step 6. Write Missing End-to-End Tests

For each complete user workflow:
1. Write tests that simulate real user interactions
2. Test complete scenarios from start to finish
3. Verify UI behavior and user experience
4. Test cross-browser compatibility if applicable
5. Run e2e tests and fix any failures

### Step 7. Achieve 100% Pass Rate

Iteratively run the complete test suite and address issues:
1. Run full test suite: `npm test` (or project-specific command)
2. For each failure:
   - Investigate root cause
   - Fix implementation or test code
   - Verify fix doesn't break other tests
3. Repeat until 0 failures, 0 errors
4. Verify test coverage meets requirements

### Step 8. Submit Final PR

When all tests are passing:
```bash
# Commit all test improvements
git add -A
git commit -m "Complete test coverage - all tests passing"

# Push and create PR
git push origin feature-branch
# Create PR with description of test improvements
```

## Tips for Claude Code

- **Be systematic**: Work through each test type methodically
- **Focus on reliability**: Ensure tests are deterministic and not flaky
- **Test the right things**: Focus on business logic and critical paths
- **Keep tests maintainable**: Write clear, readable test code
- **Use appropriate test doubles**: Mock external dependencies in unit tests
- **Test error conditions**: Don't just test the happy path
- **Run tests frequently**: After each change, run relevant tests
- **Document test failures**: When tests fail, understand why before fixing
- **Consider test performance**: Ensure test suite runs in reasonable time
- **Validate test quality**: Ensure tests actually verify the intended behavior




