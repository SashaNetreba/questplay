TEST PLAN EXECUTION

RESULTS: 
- total tests: 18 
- failed: 8
- 1st priority issues to fix: test case #1, test case #2, test case #13


###Test Case #1. Registration user-submitted data reflected in URL
FAILED

Expected Result: 
- user account was created successfully 
- URL should not display any user-submitted data
- Form data should be transmitted securely via POST
Actual Result: 
- URL displays all user-submitted data after form was submitted/after page reload
- Form data is transmitted via GET


###Test Case #2. User registration without accepting Terms and Conditions
FAILED

Expected Result: user account was not created
Actual Result: user account was created
Issue: Alert should be shown with correspondent message that Terms and Conditions were not accepted by the user



###Test Case #3. User registration success flow
PASSED

Expected Result: user account was created successfully



###Test Case #4. 'Username/Email' field check 
PASSED

Expected Result: user account was created successfully



###Test Case #5. User registration with empty 'Username/Email' field
PASSED

Expected Result: user account was not created. 'Please fill in this field' warning message is present for the 'Username/Email' field



###Test Case #6. 'Password' field check. Less than 6 characters
PASSED

Expected Result: user account was not created. 'Failed to create account' warning message is present. 'Password field' is highlighted in red 



###Test Case #7. 'Password' field check. More than 16 characters
PASSED

Expected Result: user account was not created. 'Failed to create account' warning message is present. 'Password field' is highlighted in red 



###Test Case #8. 'Password' field check. 16 characters
PASSED

Expected Result: user account was created successfully



###Test Case #9. 'Password' field validation check
FAILED

Expected Result: 'Password' field is validated and no longer highlighted red (valid data is present)
Actual Result: 'Password' field is not validated and highlighted red
Issue: After the user enters valid data in the Password field, client-side validation passes successfully. The field is not highlighted in red, and no error message is displayed



###Test Case #10. User registration with empty 'Password' field
PASSED

Expected Result: user account was not created. 'Please fill in this field' warning message is present for the 'Password' field



###Test Case #11. 'Repeat Passwod' field check. Success flow
PASSED

Expected Result: user account was created successfully 



###Test Case #12. User registration with empty 'Repeat Passwod' field
PASSED

Expected Result: user account was not created. 'Please fill in this field' warning message is present for the 'Repeat Password' field



###Test Case #13. 'Repeat Passwod' field check. Invalid data
FAILED

Expected Result: user account was not created. 'Failed to create account' warning message is present. 'Repeat Password' field is not validated and highlighted in red 
Actual Result: 'Password' field is successfully validated
Issue: After the user enters invalid data in the 'Repeat Password' field, client-side validation is absent. The field is not highlighted in red, and no error message is displayed



###Test Case #14. Check of the 'Registration' form fields tags
FAILED

Expected Result: Filed and tag naming is the same for each separate field
Actual Result: 
- 'Password' field naming and tag are diferrent
- 'Repeat Password' field spelling error in the field name
Issue: 
- field name is 'Repeat Passwod'. Spelling should be fixed and changed to "Repeat Password"
- tag name is 'Enter Password'. Should be fixed and changed to "Password"



###Test Case #16. The registration form is not responsive: it does not adjust to different screen sizes
FAILED

Expected Result: Registration form is responsive to different screen sizes
Actual Result: Registration form is not responsive to different screen sizes



###Test Case #17. WebSocket connection is intentional and not stuck after registration form was submitted
FAILED

Expected Result: WebSocket connection is intentional and not stuck
Actual Result: WebSocket connection is in pending status



###Test Case #18. After registration form was submitted - page has a redirection/load a success page
FAILED

Expected Result: Page has a redirection/load a success page
Actual Result: Page reloads the form page instead of success page
