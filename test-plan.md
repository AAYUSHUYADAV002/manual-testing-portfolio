# Test Plan — SauceDemo E-commerce Application

## 1. Objective
To verify the core functionality of the SauceDemo application — login, product browsing, cart, and checkout — and identify any functional defects through manual testing.

## 2. Scope

### In Scope
- User Login (standard_user, locked_out_user, problem_user, invalid credentials)
- Product Listing (display, sorting by name/price)
- Shopping Cart (add item, remove item, cart badge count)
- Checkout Flow (customer information form, order overview, order completion)

### Out of Scope
- Actual payment processing
- Backend/database validation (no accessible DB for this app)
- Mobile app testing

## 3. Test Approach

Manual black-box functional testing using the following test design techniques:
- **Equivalence Partitioning** — for checkout form fields (name, zip code)
- **Boundary Value Analysis** — for any numeric/length-limited fields
- **Decision Table Testing** — for login logic (valid/invalid username × valid/invalid password combinations)
- **Exploratory Testing** — for uncovering unexpected UI/behavior issues, especially using the intentionally-buggy `problem_user` login

## 4. Test Environment

| Item | Detail |
|---|---|
| Application URL | https://www.saucedemo.com |
| Browser | [e.g. Chrome 128] |
| OS | [e.g. Windows 11] |
| Test Data / Users | standard_user, locked_out_user, problem_user, performance_glitch_user (password for all: `secret_sauce`) |

## 5. Entry Criteria
- Application is accessible and stable
- Test cases have been written and reviewed

## 6. Exit Criteria
- All planned test cases have been executed
- All identified bugs have been logged with severity/priority
- No open critical/blocker bugs remain undocumented

## 7. Risks
- Application is a public demo site and may change without notice
- Some bugs are intentionally built into the site (e.g. `problem_user`) to aid learning — these are expected findings, not real production defects

## 8. Deliverables
- Test cases (`/test-cases/test-cases.xlsx`)
- Bug reports (`/bug-reports/bug-reports.md`)
- Test summary (in `README.md`)
