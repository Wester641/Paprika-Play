### Prompt to execute the end-to-end flow

Follow these steps precisely:

1) Navigate to `https://web.paprikabitdev.com/login`.
2) Click the link “Don’t have an account? Sign Up”.
3) Open a new tab `https://temp-mail.org/` and copy the generated email address. Keep this tab open.
4) Return to the Sign Up page and fill:
   - First Name: generate a realistic first name (store as FIRST)
   - Last Name: generate a realistic last name (store as LAST)
   - Email: the temp-mail address from step 3 (store as EMAIL)
   - Password and Confirm Password: generate a strong password (store as PASS)
5) Click “Sign Up”.
6) Confirm the “Verify Email” page opens and shows EMAIL.
7) Switch to the temp-mail tab, wait for an email from “Paprika Bit” with subject “Sign Up Confirmation”, open it, and extract the 6-digit code (store as CODE).
8) Return to the “Verify Email” page, enter CODE, and click “Verify”.
9) On redirect to Login, sign in with EMAIL and PASS.
10) Verify the dashboard loads (heading “Dashboards” visible).
11) Click the top-right avatar button and confirm the active organization name equals “FIRST’s Organization”.
12) Optionally, confirm the avatar initials equal the first letters of FIRST and LAST.

Constraints and quality gates:
- Avoid fixed sleeps; wait for elements using role/text selectors (e.g., headings, buttons, links).
- Do not hardcode credentials or URLs beyond those listed; use generated data for names/passwords.
- If the verification email doesn’t appear, click “Refresh” in temp-mail and retry for up to 90 seconds.
- Treat a missing dashboard or mismatched org name as a failure.

Acceptance criteria:
- Verification page appears with the correct EMAIL.
- Login succeeds and dashboard heading is visible.
- Organization name exactly matches “FIRST’s Organization”.

References:
- App: [PaprikaBit Web](https://web.paprikabitdev.com/login)
- Disposable email: [Temp Mail](https://temp-mail.org/) 


