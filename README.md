# Techland Manual Testing Project

## Overview
This document provides a comprehensive manual testing report for the login and signup features of [Techland Bangladesh](https://www.techlandbd.com/). The testing process involves detailed planning, scenario design, test execution, and bug reporting to ensure the robustness and reliability of these key functionalities.

## Test Plan
### Objectives
- Validate the login and signup functionalities.
- Ensure proper handling of valid and invalid inputs.
- Verify system responses and user experience.

### Scope
- Testing features on desktop browsers (Chrome, Firefox).
- Functional testing of login and signup.
- UI/UX validation.

### Assumptions
- Test environment is stable.
- Test data is prepared for execution.

### Out of Scope
- Performance testing.
- Mobile device testing.

### Test Deliverables
- Test scenarios and cases.
- Bug reports.

---

## Test Scenarios
### Login Feature
1. Verify successful login with valid credentials.
2. Verify error message on login with invalid credentials.
3. Verify behavior when mandatory fields are left empty.
4. Ensure password masking is working.
5. Verify the "Forgot Password" functionality.

### Signup Feature
1. Verify successful registration with valid details.
2. Verify error message for missing mandatory fields.
3. Validate the system behavior for invalid email formats.
4. Verify duplicate account prevention.

---

## Test Cases
### Login Test Cases
| Test Case ID | Test Case Description | Steps | Expected Result | Actual Result | Status |
|--------------|-------------------------|-------|-----------------|---------------|--------|
| TC001        | Login with valid credentials | 1. Navigate to login page  
2. Enter valid email/password  
3. Click Login | Redirect to user dashboard | As expected | Pass |
| TC002        | Login with invalid password | 1. Navigate to login page  
2. Enter valid email, invalid password  
3. Click Login | Display error message | As expected | Pass |
| TC003        | Leave fields empty | 1. Navigate to login page  
2. Leave fields empty  
3. Click Login | Show required field error | As expected | Pass |

### Signup Test Cases
| Test Case ID | Test Case Description | Steps | Expected Result | Actual Result | Status |
|--------------|-------------------------|-------|-----------------|---------------|--------|
| TC101        | Register with valid details | 1. Navigate to signup page  
2. Enter valid name, email, password  
3. Click Signup | Account created successfully | As expected | Pass |
| TC102        | Missing required fields | 1. Navigate to signup page  
2. Leave fields empty  
3. Click Signup | Display error messages | As expected | Pass |
| TC103        | Invalid email format | 1. Navigate to signup page  
2. Enter invalid email format  
3. Click Signup | Display error message | As expected | Pass |
| TC104        | Duplicate account | 1. Navigate to signup page  
2. Enter existing email  
3. Click Signup | Show duplicate account error | As expected | Pass |

---

## Bug Report
| Bug ID | Title | Description | Steps to Reproduce | Expected Result | Actual Result | Severity | Status |
|--------|-------|-------------|--------------------|-----------------|---------------|----------|--------|
| BUG001 | Incorrect error message for invalid login | The error message displayed is not user-friendly when login fails due to incorrect credentials | 1. Navigate to login page  
2. Enter incorrect password  
3. Click login | "Incorrect password. Please try again." | "Login failed" | Medium | Open |
| BUG002 | Duplicate email during registration | User can initiate registration with an already registered email without receiving a clear error message | 1. Navigate to signup  
2. Enter existing email  
3. Click Signup | Show duplicate account error | No message displayed | High | Open |

## Conclusion
This manual testing document outlines the structured testing approach for Techland's login and signup features. The tests revealed key issues that require resolution to enhance user experience and functionality. Further regression testing is recommended after bug fixes.
