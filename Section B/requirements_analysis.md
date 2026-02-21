TICKET REQUIREMENTS ANALYSIS AND QUESTIONS FROM QA TEAM:

1. There is no tag requirements for the fields. I can create an issue for the 'Password' field, but no requirements for that. 

- field name is Password
- tag name is Enter Password
ISSUE CAN BE CREATED HERE, BUT NO REQUIREMENTS ARE PRESENT
SEE TEST CASE #14

2. There is no requirement if user registration data should be ferlected in the URL. Now it is and issue was created. 
SEE TEST CASE #1


3. 'Password' field: what exactly the content of the alert should be? For now there is only 'Failed to create account' warning message and field is highlighted in red. It is better to give the user understanding of what exactly is wrong. 

For example: 
- If the Password field is empty, display: “Password is required”  
- If the password is too short, display: “Password must be at least 6 characters long”  
- If the password is too long, display: “Password must be maximum 16 characters long”  


4. 'Repeat Password' field: what exactly the content of the alert should be? For now there is only 'Failed to create account' warning message and field is highlighted in red. It is better to give the user understanding of what exactly is wrong.

For example: 
- If the Password field is empty, display: “Please confirm your password”  
- If the Repeat Password doesn't match the enetered Password, display: “Passwords do not match”  

5. Terms & Privacy. There is no requirement for the content of the alert when user is not accepted Terms & Privacy. 

For example: 
- If Terms & Privacy checkbox was not checked, display: "You must accept the Terms and Conditions to register"


<!--
Description:
As a new user of the application, I want to be able to register an account with a username/email address and a password. I should be able to read the terms of the application before deciding to register, and I must accept said terms before I create my account. When I submit the form, I want to be presented with an alert that shows me whether my registration was a success or whether there are any issues.


### Acceptance Criteria:
1. I need to enter either an email or username - the format of which does not currently matter to this ticket
2. I need to enter a password with a minimum character count of 6, and a maximum character count of 16
3. I must be prompted to re-enter my password, and the entered value must match the password
4. I must be able to view the terms and conditions before I submit the form
5. I need to accept the terms and conditions before I can register
6. When I click the register button, I am shown an alert. The content of the alert will depend on whether the form was completed in line with the acceptance criteria. If the form doesn't adhere to points 1-5 of the acceptance criteria, the alert message will suggest a failure, and the form will fail to submit. However, if the form is completed as per the acceptance criteria, the alert will a success message, and the form will be submitted
-->
