# BookStack QA Assignment

## Application

**BookStack Demo**

## Objective

This project contains the QA testing performed on the BookStack Demo application as part of the QA assignment.

The testing covered exploratory testing, bug hunting, security testing, and automation planning.

---

## Testing Scope

The main workflow tested was:

**Book → Chapter → Page**

The following areas were covered:

* Book creation
* Chapter creation
* Page creation
* Page editing
* Page deletion
* Input validation
* Boundary conditions
* Special characters
* Authorization and access control
* Logout access control

---

## Test Documentation

| File            | Description                                    |
| --------------- | ---------------------------------------------- |
| `test-cases.md` | Exploratory testing scenarios and test results |
| `bug-report.md` | Reproducible bug report                        |
| `security.md`   | Security testing findings                      |
| `automation.md` | Three recommended automation scenarios         |

---

## Exploratory Testing

A total of **16 test cases** were executed covering:

* Positive scenarios
* Negative scenarios
* Boundary cases
* Edge cases

The tested workflow included Book, Chapter, and Page management.

**Result:** 16/16 test cases passed.

Detailed test cases are available in [`test-cases.md`](test-cases.md).

---

## Bug Hunting

One reproducible issue was identified during testing:

**Admin user receives a permission error when attempting to change their own profile picture.**

The complete reproduction steps, expected result, actual result, severity, and evidence are documented in [`bug-report.md`](bug-report.md).

---

## Security Testing

The following security scenarios were tested:

1. Direct URL access to the User Management page while logged out.
2. Authorization check using an Editor user.
3. Access to a protected admin URL after logout.

All tested authorization controls behaved as expected.

Detailed results are available in [`security.md`](security.md).

---

## Automation

Three scenarios were selected for future automation:

1. Create Book with valid data
2. Validate required name fields
3. Page Create → Edit → Delete workflow

The reasoning for each automation candidate is documented in [`automation.md`](automation.md).

---

## Test Environment

**Application:** BookStack Demo

**Browser:** Google Chrome

**Testing Type:** Manual Exploratory & Functional Testing

---

## Repository Structure

```text
BookStack-QA-Assignment/
│
├── README.md
├── test-cases.md
├── bug-report.md
├── security.md
└── automation.md
```

---

## Conclusion

The BookStack Demo application was tested across core content-management workflows and selected security scenarios.

The testing identified one reproducible issue related to profile picture management for an Admin user. The remaining tested workflows and authorization scenarios behaved as expected.
