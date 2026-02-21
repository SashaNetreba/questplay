TEST PLAN

###Test Case #1. Registration user-submitted data reflected in URL

*Steps*
1. Enter valid data to the 'Username/Email' field
2. Enter valid data to the 'Password' field: 123456
3. Enter data from step2 to the 'Repeat Password' field
4. Accept 'Terms and Conditions'
4. Click 'Register' button

Expected Result: 
- user account was created successfully 
- URL should not display any user-submitted data
- Form data should be transmitted securely via POST



###Test Case #2. User registration without accepting Terms and Conditions (issue)

*Steps*
1. Enter valid data to the 'Username/Email' field
2. Enter valid data to the 'Password' field: 123456
3. Enter data from step2 to the 'Repeat Password' field
4. Click 'Register' button

Expected Result: user account was not created 
Reason: Terms and Conditions were not accepted by the user



###Test Case #3. User registration success flow

*Steps*
1. Enter valid data to the 'Username/Email' field
2. Enter valid data to the 'Password' field: 123456
3. Enter data from step2 to the 'Repeat Password' field
4. Accept 'Terms and Conditions'
5. Click 'Register' button

Expected Result: user account was created successfully



###Test Case #4. 'Username/Email' field check 

*Steps*
1. Enter the next data to the 'Username/Email' field: "1"
2. Enter valid data to the 'Password' field: 123456
3. Enter data from step2 to the 'Repeat Password' field
4. Accept 'Terms and Conditions'
5. Click 'Register' button

Expected Result: user account was created successfully
NOTE: for current ticket there are no restrictions about the format of 'Username/Email' field. For additional checks you can use also as entered data "e"/"123456"/"1234af56"/"1234af&*"



###Test Case #5. User registration with empty 'Username/Email' field

*Steps*
1. Enter no data to the 'Username/Email' field (leave empty)
2. Enter valid data to the 'Password' field: 123456
3. Enter data from step2 to the 'Repeat Password' field
4. Accept 'Terms and Conditions'
5. Click 'Register' button

Expected Result: user account was not created. 'Please fill in this field' warning message is present for the 'Username/Email' field


###Test Case #6. 'Password' field check. Less than 6 characters

*Steps*
1. Enter valid data to the 'Username/Email' field
2. Enter the next data to the 'Password' field: 1234
3. Enter data from step2 to the 'Repeat Password' field
4. Accept 'Terms and Conditions'
5. Click 'Register' button

Expected Result: user account was not created. 'Failed to create account' warning message is present. 'Password field' is highlighted in red 



###Test Case #7. 'Password' field check. More than 16 characters

*Steps*
1. Enter valid data to the 'Username/Email' field
2. Enter the next data to the 'Password' field: 1234ad7ksbnt@14b%7
3. Enter data from step2 to the 'Repeat Password' field
4. Accept 'Terms and Conditions'
5. Click 'Register' button

Expected Result: user account was not created. 'Failed to create account' warning message is present. 'Password' field is highlighted in red 



###Test Case #8. 'Password' field check. 16 characters

*Steps*
1. Enter valid data to the 'Username/Email' field
2. Enter the next data to the 'Password' field: 1234ad7ksbnt@14b%
3. Enter data from step2 to the 'Repeat Password' field
4. Accept 'Terms and Conditions'
5. Click 'Register' button

Expected Result: user account was created successfully



###Test Case #9. 'Password' field validation check

*Steps*
1. Enter valid data to the 'Username/Email' field
2. Enter the next data to the 'Password' field: 12&
3. Enter data from step2 to the 'Repeat Password' field
4. Accept 'Terms and Conditions'
5. Click 'Register' button
6. Click 'OK' on 'Failed to create account' warning message
7. See that validation for 'Password' field is present. Field is highlighted red.
8. Enter valid data to the 'Password' field: 123456

Expected Result: 'Password' field is no longer highlighted red (valid data is present)



###Test Case #10. User registration with empty 'Password' field

*Steps*
1. Enter valid data to the 'Username/Email' field
2. Enter no data to the 'Password' field (leave empty)
3. Enter the next data to the 'Repeat Password' field: 123456
4. Accept 'Terms and Conditions'
5. Click 'Register' button

Expected Result: user account was not created. 'Please fill in this field' warning message is present for the 'Password' field



###Test Case #11. 'Repeat Passwod' field check. Success flow

*Steps*
1. Enter valid data to the 'Username/Email' field
2. Enter valid data to the 'Password' field: 123456
3. Enter data from step2 to the 'Repeat Password' field
4. Accept 'Terms and Conditions'
5. Click 'Register' button

Expected Result: user account was created successfully 



###Test Case #12. User registration with empty 'Repeat Passwod' field

*Steps*
1. Enter valid data to the 'Username/Email' field
2. Enter valid data to the 'Password' field: 123456
3. Enter no data to the 'Repeat Password' field (leave empty)
4. Accept 'Terms and Conditions'
5. Click 'Register' button

Expected Result: user account was not created. 'Please fill in this field' warning message is present for the 'Repeat Password' field



###Test Case #13. 'Repeat Passwod' field check. Invalid data

*Steps*
1. Enter valid data to the 'Username/Email' field
2. Enter valid data to the 'Password' field: 123456
3. Enter the next data to the 'Repeat Password' field: 1234567hj
4. Accept 'Terms and Conditions'
5. Click 'Register' button

Expected Result: user account was not created. 'Failed to create account' warning message is present. 'Repeat Password' field is highlighted in red 



###Test Case #14. Check of the 'Registration' form fields tags

*Steps*
1. Open the registration form: http://127.0.0.1:8080/html/form.html
2. Make sure that field and tag naming is the same: 

- field name is Username/Email
- tag name is Username/Email

- field name is Password
- tag name is Password

- field name is Repeat Password
- tag name is Repeat Password

Expected Result: Filed and tag naming is the same for each separate field




###Test Case #15. The Registration form is not adjustable to the different screen sizes

*Steps*
1. Open the registration form: http://127.0.0.1:8080/html/form.html
2. Make sure that field and tag naming is the same: 

- field name is Username/Email
- tag name is Username/Email

- field name is Password
- tag name is Password

- field name is Repeat Password
- tag name is Repeat Password

Expected Result: Filed and tag naming is the same for each separate field



###Test Case #16. The registration form is not responsive: it does not adjust to different screen sizes

*Steps*
1. Open the registration form: http://127.0.0.1:8080/html/form.html
2. Go to DevTools and change screen size

Expected Result: Registration form is responsive to different screen sizes



###Test Case #17. WebSocket connection is intentional and not stuck after registration form was submitted

*Steps*
1. Enter valid data to the 'Username/Email' field
2. Enter valid data to the 'Password' field: 123456
3. Enter data from step2 to the 'Repeat Password' field: 1234567hj
4. Accept 'Terms and Conditions'
5. Click 'Register' button

Expected Result: WebSocket connection is intentional and not stuck



###Test Case #18. After registration form was submitted - page has a redirection/load a success page

*Steps*
1. Enter valid data to the 'Username/Email' field
2. Enter valid data to the 'Password' field: 123456
3. Enter data from step2 to the 'Repeat Password' field: 1234567hj
4. Accept 'Terms and Conditions'
5. Click 'Register' button

Expected Result: Page has a redirection/load a success page
