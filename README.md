# 🧪 Manual Web Application Testing Portfolio

> A practical **Manual Software Testing / SQA** project covering functional testing, login testing, UI and form validation, e-commerce testing, positive/negative testing, boundary testing, edge-case testing, and structured bug reporting.

![Manual Testing](https://img.shields.io/badge/Testing-Manual%20Testing-blue)
![SQA](https://img.shields.io/badge/Domain-Software%20Quality%20Assurance-green)
![Test Cases](https://img.shields.io/badge/Test%20Cases-12-orange)
![Status](https://img.shields.io/badge/Status-Completed-success)

---

## 📌 Project Overview

This repository contains the completed work for a beginner-level **Web Application Manual Testing Assessment**.

The project was designed around three live practice applications:

1. **SauceDemo** — Functional & Login Testing
2. **DemoQA** — UI & Form Validation Testing
3. **Magento Software Testing Board** — E-commerce & Bug Reporting

The original assessment contains **12 scenario-based questions** and requires at least one relevant test case to be written and executed for every scenario. The assessment is divided into three sections covering functional/login testing, UI/form validation, and e-commerce/bug reporting.

The completed test cases and bug report are maintained in the accompanying Excel workbook.

---

## 🎯 Project Objectives

The main goals of this project were to demonstrate practical knowledge of:

- Manual software testing
- Functional testing
- Login and authentication testing
- UI testing
- Form validation testing
- Positive testing
- Negative testing
- Boundary value testing
- Edge-case testing
- E-commerce testing
- Shopping cart testing
- Search testing
- Password validation
- Wishlist testing
- CRUD testing
- Defect identification
- Bug reporting
- Severity classification
- Expected vs. actual result analysis
- Test case documentation

---

## 🌐 Applications Tested

| Application | Testing Area | URL |
|---|---|---|
| **SauceDemo** | Functional & Login Testing | https://www.saucedemo.com/ |
| **DemoQA** | UI & Form Validation Testing | https://demoqa.com/ |
| **Magento Demo Store** | E-commerce & Bug Reporting | https://magento.softwaretestingboard.com/ |

> These are public training/demo applications. Their behavior can change over time, so the recorded results in this repository represent the test execution documented for this project.

---

# 📊 Testing Scope

## Section A — Functional & Login Testing

**Application:** SauceDemo

Covered scenarios:

1. Locked-out user login
2. Product addition and cart verification
3. Checkout form validation
4. Problem-user UI and functional defect identification

---

## Section B — UI & Form Validation Testing

**Application:** DemoQA

Covered scenarios:

5. Empty Practice Form validation
6. Mobile number input validation
7. JavaScript alert behavior
8. Web Table CRUD operations and edge cases

---

## Section C — E-commerce & Bug Reporting

**Application:** Magento Demo Store

Covered scenarios:

9. Product search with valid and invalid keywords
10. Password and confirm-password validation
11. Guest wishlist authentication behavior
12. Shopping cart update and quantity boundary testing

---

# 🔐 Test Credentials

The assessment supplied the following SauceDemo practice credentials:

| Username | Password | Purpose |
|---|---|---|
| `locked_out_user` | `secret_sauce` | Locked-user login testing |
| `standard_user` | `secret_sauce` | Normal functional testing |
| `problem_user` | `secret_sauce` | Problem/defect testing |

> These credentials belong to the public SauceDemo training application and are included here only as part of the documented testing scenario.

---

# 🧪 Test Case Summary

A total of **12 test cases** were documented in the Excel test-case sheet.

| TC ID | Scenario | Application | Test Type |
|---|---|---|---|
| TC_LOGIN_01 | Locked-out user login | SauceDemo | Negative / Functional |
| TC_CART_01 | Verify cart item details | SauceDemo | Functional |
| TC_CHECKOUT_01 | Empty checkout form validation | SauceDemo | Validation / Negative |
| TC_EXPLORE_01 | Problem-user product listing | SauceDemo | UI / Functional |
| TC_FORM_VAL_01 | Empty practice form validation | DemoQA | Validation |
| TC_FORM_VAL_02 | Mobile number input validation | DemoQA | Negative / Validation |
| TC_ALERT_01 | JavaScript alert behavior | DemoQA | Functional |
| TC_TABLE_CRUD_01 | Add, edit and delete table record | DemoQA | CRUD / Functional |
| TC_SEARCH_01 | Valid and invalid product search | Magento | Functional / Negative |
| TC_REG_VAL_01 | Password and confirmation validation | Magento | Validation / Negative |
| TC_WISHLIST_01 | Guest wishlist authentication | Magento | Functional / Access Control |
| TC_CART_MATH_01 | Cart update after item removal | Magento | Functional / Calculation |

---

# 📝 Detailed Test Scenarios

## 1. TC_LOGIN_01 — Locked-Out User Login

### Objective

Verify that a locked-out user cannot log in and receives a clear error message.

### Preconditions

User is on the SauceDemo login page.

### Steps

1. Open SauceDemo.
2. Enter `locked_out_user` in the Username field.
3. Enter `secret_sauce` in the Password field.
4. Click **Login**.

### Expected Result

Login should fail and a clear message should be displayed:

> `Epic sadface: Sorry, this user has been locked out.`

### Result

**Pass**

The recorded result confirmed that the message clearly explains why login failed.

---

## 2. TC_CART_01 — Verify Cart Item Details

### Objective

Verify that selected products are correctly added to the shopping cart.

### Preconditions

User is logged in as `standard_user`.

### Steps

1. Add **Sauce Labs Backpack** to the cart.
2. Add **Sauce Labs Fleece Jacket** to the cart.
3. Open the shopping cart.

### Expected Result

The cart should contain:

- Sauce Labs Backpack — **$29.99**
- Sauce Labs Fleece Jacket — **$49.99**

The quantities, product names, prices, Remove controls, and Checkout button should also be checked.

### Result

**Pass**

---

## 3. TC_CHECKOUT_01 — Checkout Validation

### Objective

Verify validation when mandatory checkout fields are empty.

### Preconditions

User is on the checkout information page.

### Steps

1. Leave First Name empty.
2. Leave Last Name empty.
3. Leave Zip/Postal Code empty.
4. Click **Continue**.

### Expected Result

The form must not proceed without required information and should display the appropriate validation message.

### Recorded Result

The application displays:

> `Error: First Name is required`

The application validates the missing fields sequentially.

### Related Defect

A bug report was documented separately for the requirement that all missing mandatory fields should be handled comprehensively.

---

## 4. TC_EXPLORE_01 — Problem User Product Listing

### Objective

Verify product image rendering, Add to Cart functionality, and product links for `problem_user`.

### Steps

1. Log in as `problem_user`.
2. Observe product images.
3. Click **Add to cart** for Sauce Labs Backpack.
4. Click the product title.

### Expected Result

- Each product should display its correct image.
- Add to Cart should update the cart correctly.
- Product title should open the correct product details page.

### Recorded Defects

Three issues were identified during the assessment:

| Defect | Expected Behavior | Severity |
|---|---|---|
| Product images display the same dog placeholder | Each product should display its own relevant image | Minor |
| Add to Cart may fail to update the cart | Cart badge and button state should update correctly | Critical |
| Product links may open the wrong/broken page | Each title should open its corresponding product details | Major |

---

# 5. TC_FORM_VAL_01 — Empty Practice Form

### Objective

Verify required-field validation on the DemoQA Practice Form.

### Steps

1. Open DemoQA Practice Form.
2. Leave all fields empty.
3. Click **Submit**.

### Expected / Recorded Validation

The following fields were observed as validation failures:

- First Name
- Last Name
- Gender
- Mobile Number

The recorded assessment also notes that fields such as Email, Date of Birth, Subjects, Hobbies, Current Address, State, and City did not show the same strict mandatory validation behavior.

### Result

Validation behavior was documented for further assessment.

---

# 6. TC_FORM_VAL_02 — Mobile Number Validation

### Objective

Verify that invalid characters are not accepted as a mobile number.

### Test Input

```text
abc!@#
```

### Expected Result

A mobile number field should accept numeric digits rather than letters or special characters.

### Recorded Result

The invalid input was rejected/flagged visually.

### Defect?

**No defect was recorded.**

The behavior was considered appropriate input validation for a mobile-number field.

---

# 7. TC_ALERT_01 — JavaScript Alert

### Objective

Verify that a JavaScript alert opens and closes correctly.

### Steps

1. Open the Alerts section of DemoQA.
2. Click the button that opens an alert.
3. Verify the browser alert.
4. Click **OK**.

### Expected Result

- Alert should appear.
- Correct message should be displayed.
- Clicking OK should close the alert.
- The parent page should remain usable.

### Positive Test

Open the alert → verify the message → click OK → verify normal page interaction.

### Negative Test

Trigger a timed alert and interact with the page around the expected alert time to check for crashes, frozen UI, or unhandled behavior.

---

# 8. TC_TABLE_CRUD_01 — Web Table CRUD

### Objective

Verify Add, Edit, and Delete operations in DemoQA Web Tables.

### Steps

1. Click **Add**.
2. Enter the required record information.
3. Submit the record.
4. Edit the newly created record.
5. Change a field such as Age.
6. Save the record.
7. Delete the same record.

### Expected Result

- New row should appear immediately.
- Edited information should update immediately.
- Deleted row should disappear immediately.
- Browser refresh should not be required.

### Edge Cases

Two important edge cases documented for Add Record:

1. **Very long input**
   - Try a very long first/last name.
   - Check whether the table breaks or handles the text correctly.

2. **Duplicate record**
   - Enter details identical to an existing record.
   - Check whether duplicates are accepted or properly handled.

---

# 9. TC_SEARCH_01 — Magento Search

### Objective

Verify valid and invalid product searches.

### Test 1 — Valid Search

Search:

```text
yoga
```

### Expected Result

Relevant products should appear with:

- Product names
- Prices
- Images
- Relevant product results

### Test 2 — Invalid Search

Search:

```text
xyzabc123
```

### Expected Result

The application should show a clear no-results message rather than an error page.

### Recorded Result

The assessment recorded the message:

> `Your search returned no results...`

### Result

**Pass**

---

# 10. TC_REG_VAL_01 — Password Validation

### Objective

Verify weak-password and password-mismatch validation.

### Test Input

Password:

```text
abc
```

Confirm Password:

```text
xyz
```

### Expected Result

Registration should be blocked.

The password field should report the minimum-length problem and the confirmation field should report the mismatch.

### Recorded Messages

Minimum password length:

> `Minimum length of this field must be equal or greater than 8 symbols.`

Mismatch:

> `Please enter the same value again.`

### Result

**Pass**

---

# 11. TC_WISHLIST_01 — Guest Wishlist Access

### Objective

Verify that unauthenticated users cannot add products to a personal wishlist without authentication.

### Preconditions

User is browsing as a guest.

### Steps

1. Open a product details page.
2. Click **Add to Wish List**.

### Expected Result

Guest user should be redirected to login/register and should receive a clear explanation.

### Recorded Result

The user is redirected to the login page and receives:

> `You must login or register to add items to your wishlist.`

### Result

**Pass**

---

# 12. TC_CART_MATH_01 — Cart Update After Removing an Item

### Objective

Verify that cart item count and price are recalculated after removing an item.

### Preconditions

Cart contains exactly three different products.

### Steps

1. Open the Shopping Cart.
2. Record the initial item count and total.
3. Remove one product.

### Expected Result

- Removed item disappears.
- Cart item count decreases correctly.
- Total price decreases by the correct amount.
- UI updates without requiring a full page refresh.

### Recorded Result

The cart updated immediately and recalculated the item count and estimated total.

### Result

**Pass**

---

# 🐞 Bug Reporting

The project uses the standard bug-report structure:

- Bug ID
- Serial Number
- Preconditions
- Title / Description
- Steps to Reproduce
- Expected Result
- Actual Result
- Severity
- Comments

## Documented Bug — Checkout Validation

### Bug ID

`BR_CHECKOUT_01`

### Title

**Checkout form allows incomplete mandatory-field validation / does not comprehensively highlight all missing required fields.**

### Preconditions

User is logged in and on the checkout page.

### Steps to Reproduce

1. Log in as `standard_user`.
2. Add any item to the cart.
3. Open the Cart page.
4. Click **Checkout**.
5. Leave First Name, Last Name, and Postal Code empty.
6. Click **Continue**.

### Expected Result

Form submission should be blocked and clear validation messages/highlights should be presented for the missing required fields.

### Actual Result

Only a single sequential error message is displayed, or missing fields are not highlighted comprehensively.

### Severity

**Medium**

---

# 🔎 Testing Techniques Used

## Functional Testing

Checks whether features work according to their expected behavior.

## Positive Testing

Uses valid input and expected user actions.

Example:

```text
Search for "yoga"
```

## Negative Testing

Uses invalid input or unexpected actions.

Example:

```text
Search for "xyzabc123"
```

## Boundary Testing

Checks values around acceptable limits.

Examples:

```text
Cart quantity = 0
Cart quantity = -1
Cart quantity = 99999
```

## Edge-Case Testing

Checks unusual but possible conditions.

Examples:

- Very long text
- Duplicate records
- Empty required fields
- Invalid characters
- Extremely large quantities

## UI Testing

Checks visual and interaction behavior.

Examples:

- Product images
- Buttons
- Error messages
- Page responsiveness after alerts

## Validation Testing

Checks whether invalid or incomplete input is correctly rejected.

---

# 📋 Test Case Documentation Format

Each test case follows a structured format:

| Field | Description |
|---|---|
| Test Case ID | Unique identifier |
| Serial No. | Test case sequence |
| Preconditions | Required starting condition |
| Title / Description | Purpose of the test |
| Steps | Actions performed |
| Expected Result | Expected system behavior |
| Actual Result | Observed behavior |
| Status | Pass / Fail where applicable |
| Comments | Additional observation |

---

# 🐛 Bug Report Format

Each bug report should contain:

```text
Bug ID
Serial No.
Prerequisites
Title / Description
Steps to Reproduce
Expected Result
Actual Result
Severity
Comments
```

This makes defects easier for developers and QA engineers to understand and reproduce.

---

# 📁 Recommended Repository Structure

```text
manual-web-application-testing/
│
├── README.md
│
├── test-cases/
│   └── manual-testing-test-cases.xlsx
│
├── bug-reports/
│   └── BR_CHECKOUT_01.md
│
├── test-evidence/
│   ├── screenshots/
│   └── execution-results/
│
├── documents/
│   └── assessment-reference.docx
│
└── .gitignore
```

### Recommended contents

**`README.md`**
- Project overview
- Scope
- Test applications
- Test scenarios
- Test results
- Defects
- Testing techniques

**`test-cases/`**
- Completed Excel test cases

**`bug-reports/`**
- Individual Markdown bug reports

**`test-evidence/`**
- Screenshots and execution evidence

**`documents/`**
- Assessment/reference document, if redistribution is permitted

---

# 📊 Project Statistics

| Metric | Value |
|---|---:|
| Applications Tested | 3 |
| Total Scenarios | 12 |
| Test Cases Documented | 12 |
| Main Testing Sections | 3 |
| Documented Bug Reports | 1 |
| Testing Type | Manual |
| Primary Domain | Web Applications |

---

# 🧰 Tools & Technologies

This project is primarily a **manual testing project**, so no automation framework is required.

### Tools

- Web Browser
- Microsoft Excel / Spreadsheet
- Git
- GitHub
- Markdown

### Testing Skills

- Test Case Design
- Test Execution
- Functional Testing
- UI Testing
- Validation Testing
- Negative Testing
- Boundary Testing
- Edge-Case Testing
- Bug Reporting
- Severity Classification

---

# 📚 Learning Outcomes

Through this project, I practiced how to:

- Convert a scenario into a test case.
- Define preconditions and test steps.
- Write clear expected results.
- Compare expected and actual behavior.
- Identify defects from real web applications.
- Decide whether unexpected behavior is actually a defect.
- Select useful positive and negative tests.
- Test field validation.
- Test e-commerce workflows.
- Test CRUD operations.
- Design boundary and edge-case scenarios.
- Write reproducible bug reports.
- Assign practical severity levels.
- Organize QA artifacts in a professional repository.

---

# ⚠️ Important Note About Test Results

This repository documents testing performed against public demonstration websites.

Because these applications are externally hosted:

- UI behavior may change.
- Product data may change.
- Error messages may change.
- URLs or workflows may change.
- Previously observed defects may be fixed.
- New defects may appear.

Therefore, the documented results should be treated as **test execution evidence for the project period**, not as a permanent statement about the current production behavior of the websites.

---

# 👨‍💻 Author

**Abdullah Nazmus-Sakib**

Computer Science & Engineering  
Jahangirnagar University

### Areas of Interest

- Software Quality Assurance
- Manual Testing
- Software Testing
- Full-Stack Development
- AI/ML
- Software Engineering

---

# ⭐ Repository Purpose

This repository is intended as a **QA/SQA portfolio project** demonstrating practical manual testing skills through real interaction with publicly available web applications.

It can be used to showcase:

- Test case writing
- Test execution
- Defect identification
- Bug reporting
- Testing techniques
- QA documentation

---

## 📌 Assessment Reference

The project is based on the supplied **Manual Testing Assessment — Web Application Testing (Beginner Level)** document. The assessment specifies three practice applications, 12 scenario-based questions, and a requirement to write and execute at least one relevant test case for each scenario.

The completed Excel workbook contains the documented test cases and the recorded checkout-validation bug report.
