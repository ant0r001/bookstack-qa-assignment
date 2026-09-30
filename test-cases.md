# Exploratory Testing — BookStack

## Test Scope

**Application:** BookStack Demo

**Feature/Workflow:** Book → Chapter → Page creation and management

**Testing Types:** Positive, Negative, Boundary, and Edge Case Testing

---

|   ID   | Scenario                                          |   Type   | Expected Result                                                                                                      | Actual Result                                                                                              | Result | Screenshot |
| :----: | :------------------------------------------------ | :------: | :------------------------------------------------------------------------------------------------------------------- | :--------------------------------------------------------------------------------------------------------- | :----: | :--------- |
| TC-001 | Create book with valid name                       | Positive | Book should be created successfully.                                                                                 | Book "Test Book" was created successfully.                                                                 |  PASS  |            |
| TC-002 | Create book with empty name                       | Negative | Application should prevent book creation and display a validation message.                                           | Book was not created and the validation message "The name field is required." was displayed.               |  PASS  |            |
| TC-003 | Create book with minimum/very short name          | Boundary | Application should handle a one-character book name correctly.                                                       | Book with the name "a" was created successfully.                                                           |  PASS  |            |
| TC-004 | Create book with name exceeding 255 characters    | Boundary | Application should reject a book name longer than 255 characters and display a validation message.                   | Application displayed: "The name may not be greater than 255 characters."                                  |  PASS  |            |
| TC-005 | Create book with special characters               |   Edge   | Application should handle valid special characters without errors.                                                   | Book was created successfully and the special characters were displayed correctly.                         |  PASS  |            |
| TC-006 | Create chapter with valid name                    | Positive | Chapter should be created successfully.                                                                              | "QA Test Chapter" was created successfully.                                                                |  PASS  |            |
| TC-007 | Create chapter with empty name                    | Negative | Application should prevent chapter creation and display a validation message.                                        | Chapter was not created and "The name field is required." was displayed.                                   |  PASS  |            |
| TC-008 | Create chapter with 1-character name              | Boundary | Application should handle a one-character chapter name correctly.                                                    | Chapter with the name "A" was created successfully.                                                        |  PASS  |            |
| TC-009 | Create chapter with name exceeding 255 characters | Boundary | Application should reject a chapter name longer than 255 characters and display a validation message.                | Application displayed: "The name may not be greater than 255 characters." and the chapter was not created. |  PASS  |            |
| TC-010 | Create chapter with special characters            |   Edge   | Application should handle valid special characters correctly.                                                        | Chapter with special characters was created successfully.                                                  |  PASS  |            |
| TC-011 | Create page with valid title and content          | Positive | Page should be created successfully with the provided title and content.                                             | "QA Test Page" was created successfully and the test content was saved.                                    |  PASS  |            |
| TC-012 | Create page without a title                       | Negative | Application should prevent page creation and display a validation message because the title is required.             | Application displayed "The name field is required." and the page was not created.                          |  PASS  |            |
| TC-013 | Create page with empty content                    |   Edge   | Application should handle an empty-content page without errors.                                                      | Application allowed the page to be created successfully with an empty content body.                        |  PASS  |            |
| TC-014 | Create page with special characters in title      |   Edge   | Application should accept valid special characters and display the page title correctly.                             | Page with special characters in the title was created and displayed successfully.                          |  PASS  |            |
| TC-015 | Edit an existing page                             | Positive | User should be able to edit an existing page and save the updated content.                                           | Page was edited successfully and the updated content was displayed.                                        |  PASS  |            |
| TC-016 | Delete an existing page                           | Positive | User should be able to delete an existing page after confirmation, and the page should no longer appear in the book. | The page was deleted successfully and was removed from the book.                                           |  PASS  |            |

## Exploratory Testing Summary

A total of **16 test cases** were executed.

The testing covered:

* Positive scenarios
* Negative scenarios
* Boundary conditions
* Edge cases
* Book creation
* Chapter creation
* Page creation
* Page editing
* Page deletion

**Overall Result:** 16/16 test cases passed.
