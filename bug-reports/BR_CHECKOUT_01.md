# BR_CHECKOUT_01 — Checkout Mandatory-Field Validation

## Summary

Checkout validation does not comprehensively highlight all missing mandatory fields when First Name, Last Name, and Postal Code are left empty.

## Preconditions

- User is logged in as `standard_user`.
- User is on the checkout page.

## Steps to Reproduce

1. Log in as `standard_user`.
2. Add any item to the cart.
3. Open the Cart page.
4. Click **Checkout**.
5. Leave First Name, Last Name, and Postal Code empty.
6. Click **Continue**.

## Expected Result

Form submission should be blocked and clear validation messages/highlights should be shown for all missing mandatory fields.

## Actual Result

Only a single sequential error message is displayed, or the missing fields are not highlighted comprehensively.

## Severity

**Medium**

## Environment

- Application: SauceDemo
- Test Type: Functional / Validation
- Test Case: `TC_CHECKOUT_01`
