# Bug Report

## BUG-001 — Admin Cannot Change Own Profile Picture

### Title

**Admin user receives a permission error when attempting to change their own profile picture**

### Severity

**Medium**

### Environment

* Application: BookStack Demo
* Browser: Google Chrome
* User Role: Admin
* Test Account: `admin@example.com`

### Preconditions

* User is logged in with an Admin account.
* User has access to the My Account/Profile page.

### Steps to Reproduce

1. Log in to BookStack using an Admin account.
2. Open **My Account / Profile**.
3. Navigate to the profile picture/avatar section.
4. Select the option to change/upload the profile picture.
5. Attempt to save the new profile picture.

### Expected Result

The Admin user should be able to change their own profile picture successfully.

### Actual Result

The application displays the following error:

> **You do not have permission to access the requested page.**

The profile picture cannot be changed.

### Reproducibility

**Reproducible**

The same behavior was observed when repeating the profile picture change operation using the Admin account.

### Impact

An Admin user cannot update their own profile picture through the profile settings interface.

### Severity Justification

**Medium** — The issue prevents a user from completing a profile-management function, but it does not prevent access to or management of the main BookStack content workflow.

### Evidence

Screenshot showing the Admin account attempting to change the profile picture and receiving:

> **You do not have permission to access the requested page.**

### Result

**FAIL**
