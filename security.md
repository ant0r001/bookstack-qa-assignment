# Security Testing

## SEC-01 — Direct URL Access

**Scenario:** Logged-out user attempts to access the User Management page.

**Steps:**

1. Log out from BookStack.
2. Directly open `/settings/users`.

**Expected Result:**
Unauthenticated users should not be able to access the User Management page.

**Actual Result:**
The application displayed:

> You do not have permission to access the requested page.

The User Management page was not accessible.

**Result:** PASS

**Severity:** N/A — No security issue found.

**Evidence:** Screenshot showing the permission-denied message.

---

## SEC-02 — Authorization / Permission

**Scenario:** An Editor user attempts to access the User Management page.

**Steps:**

1. Log in as an Editor user.
2. Directly open `/settings/users`.

**Expected Result:**
An Editor user should not be able to access the User Management page.

**Actual Result:**
The application displayed:

> You do not have permission to access the requested page.

The User Management page was not accessible.

**Result:** PASS

**Severity:** N/A — No authorization issue found.

**Evidence:** Screenshot showing the permission-denied message.

---

## SEC-03 — Access After Logout

**Scenario:** Access a protected admin URL after logout.

**Steps:**

1. Log in to BookStack.
2. Access a protected page.
3. Log out.
4. Open `/settings/users` directly.

**Expected Result:**
The protected User Management page should not be accessible after logout.

**Actual Result:**
The application displayed:

> You do not have permission to access the requested page.

The protected page was not accessible.

**Result:** PASS

**Severity:** N/A — No security issue found.

**Evidence:** Screenshot showing the permission-denied message.

---

## Security Testing Summary

All tested authorization controls behaved as expected.

The following areas were tested:

* Direct URL access
* Authorization/permission control
* Access to protected resources after logout

No security vulnerability was identified during these tests.
