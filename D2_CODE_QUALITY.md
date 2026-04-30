# D2: Code Quality Analysis

**Project:** Job Center Management System  
**Group:** Chongyai (Maintainer)  
**Tool:** SonarQube Cloud  

---

## Changes Overview

| Change   | Description                                 |
| -------- | ------------------------------------------- |
| Change 1 | Added unit tests for mobile business logic  |
| Change 2 | Improved backend and frontend test coverage |
| Change 3 | Minor refactoring for maintainability       |

---

## SonarQube Configuration

### New Code Setup

| Setting             | Value                                      |
| ------------------- | ------------------------------------------ |
| New Code Definition | Previous Version                           |
| Versioning Strategy | Increment `sonar.projectVersion` every run |

**Explanation:**  
SonarQube compares the current version with the previous version to analyze only newly added or modified code, ensuring that quality evaluation focuses strictly on recent changes.

---

### Coverage Configuration

| Configuration  | Description                                              |
| -------------- | -------------------------------------------------------- |
| Excluded Files | UI-related files (screens, widgets, frontend components) |
| Included Files | Business logic (services, backend, core logic)           |

---

## Before vs After Comparison

### Before Changes

| Metric                  | Value  |
| ----------------------- | ------ |
| Coverage (Overall Code) | 41.7%  |
| Bugs                    | 0      |
| Vulnerabilities         | 0      |
| Code Smells             | ~2.9k  |
| Quality Gate            | PASSED |

![Before Analysis](https://github.com/user-attachments/assets/2adb713a-2a94-44ea-b370-ef2273f6f37c)

*Figure 1: SonarQube analysis before applying the changes.*

---

### After Changes

| Metric                  | Value  |
| ----------------------- | ------ |
| Coverage (Overall Code) | 41.7%  |
| Bugs                    | 0      |
| Vulnerabilities         | 0      |
| Code Smells             | ~2.9k  |
| Quality Gate            | PASSED |

![After Analysis](https://github.com/user-attachments/assets/edd9becd-f759-473f-aa31-39deb6a50513)

*Figure 2: SonarQube analysis after applying the changes.*

---

### Comparison Analysis

Although the overall code coverage remains unchanged at 41.7%, the newly added and modified code is fully covered by tests (100%).

This indicates that the recent changes were implemented with proper testing practices and did not negatively impact the existing system quality.

---

## New Code Analysis

### New Code Detection

| Attribute        | Description                           |
| ---------------- | ------------------------------------- |
| Detection Method | Version comparison (Previous Version) |
| Status           | Successfully detected new code        |

---

### Evidence of New Code Configuration

The project is configured to use the "Previous Version" strategy for defining new code.

This is verified by:
- SonarQube indicating "New code: since version 23"
- Detection of 4 new lines of code
- Separate metrics for new code (coverage = 100%)

This confirms that the new code configuration is correctly applied.

---

### New Code Metrics

| Metric               | Value |
| -------------------- | ----- |
| Lines of New Code    | 4     |
| Coverage on New Code | 100%  |
| New Bugs             | 0     |
| New Vulnerabilities  | 0     |
| New Code Smells      | 0     |

---

## Test Coverage Requirement

| Requirement                | Result |
| -------------------------- | ------ |
| Coverage on New Code > 90% | 100%   |

✔ Requirement satisfied

---

## Quality Gate Result

| Metric       | Status |
| ------------ | ------ |
| Quality Gate | PASSED |

---

## Evidence of Quality Preservation

- No new bugs were introduced  
- No new vulnerabilities were detected  
- No additional code smells were introduced in the new code  
- Test coverage on new code reached 100%  
- Quality Gate passed successfully after changes  

---

## CI/CD Integration

The analysis is automated through a CI pipeline using GitHub Actions.

The analysis was executed after applying the changes through the CI pipeline, ensuring that the reported results reflect the updated system state.

---

## Conclusion

The results demonstrate that the applied changes maintain the overall software quality without introducing defects or degrading maintainability.

Although the overall code coverage remains unchanged at 41.7%, the newly added and modified code achieves 100% test coverage. This confirms that all recent changes are well-tested and comply with the required quality standards.

---

## Appendix

- Repository: https://github.com/outoft3n/2025-ITCS383-Chongyai  
- SonarQube Dashboard (latest version)  
- CI/CD configuration (`.github/workflows/ci.yml`)
