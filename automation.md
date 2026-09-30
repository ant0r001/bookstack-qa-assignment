# Automation Testing

## Automation Approach

The following three scenarios are good candidates for automation because they are repeatable, stable, and important for regression testing.

---

## 1. Create Book with Valid Data

**Scenario:** Create a new Book with a valid name.

**Example Test:**

1. Login as Admin.
2. Navigate to Books.
3. Click Create New Book.
4. Enter a valid Book name.
5. Save the Book.
6. Verify that the Book appears successfully.

**Why Automate?**

Book creation is a core application workflow and may be executed frequently during regression testing. Automating this scenario would reduce repetitive manual effort and quickly identify failures after application changes.

**Priority:** High

---

## 2. Validate Empty Name Fields

**Scenario:** Verify that Book, Chapter, and Page creation is prevented when the required name/title field is empty.

**Example Test:**

1. Open the Book creation form.
2. Leave the name field empty.
3. Click Save.
4. Verify that the validation message is displayed.

The same validation can also be automated for Chapter and Page creation.

**Why Automate?**

Required-field validation is repetitive and predictable. Automation can verify the same validation across multiple content types and prevent regression issues.

**Priority:** High

---

## 3. Page Create → Edit → Delete Workflow

**Scenario:** Automate the complete Page lifecycle.

**Example Test:**

1. Open a Book and Chapter.
2. Create a new Page.
3. Verify that the Page is created.
4. Edit the Page content.
5. Save the changes.
6. Verify the updated content.
7. Delete the Page.
8. Verify that the Page is no longer accessible.

**Why Automate?**

This is an important end-to-end workflow involving multiple related actions. Automating it provides regression coverage for Page creation, editing, saving, and deletion while reducing the time required for repeated manual testing.

**Priority:** High

---

## Summary

The three selected scenarios are suitable for automation because they are:

* Frequently repeated
* Important application workflows
* Easy to verify with clear expected results
* Useful for regression testing
* Time-consuming when repeatedly performed manually
