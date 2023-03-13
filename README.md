# Test_Automation_Task
Assesment

George Pooe

Cypress Test Suite

This code defines a test suite using Cypress, a JavaScript-based end-to-end testing framework. The test suite consists of three separate modules - login, logout, and ViewForms - and a main function called executeTestSuite() that orchestrates the individual tests.

Login

The login module exports a LoginPage class that has a single method called login. This method takes in a username and password as arguments and performs the following steps:

Visit the URL https://ryze-staging.formedix.com/sign-in
Type the username into the #username input field
Type the password into the #password input field
Click the .form-group, .sign-in button
Verify that the URL includes the correct url
The loginData variable is imported from the login.json file, which contains the login credentials that are used in the login test.

Logout

The logout module exports a LogoutButton class that has a single method called logout. This method performs the following steps:

Visit the URL /dashboard
Click on the .fdx-main-nav-item-label element
Click on the .fdx-sub-nav-menu-item-label element
Verify that the URL includes the string https://ryze-staging.formedix.com/

ViewForms

The ViewForms module exports a ViewForms class that has two methods - viewForms and MedicalHistory - which perform the following tasks:

viewForms: Clicks on the Repository and Studies elements, clicks on the .fdxicon-regular.fdx-menu.dropdown-toggle.icon element, clicks on the View element, verifies that the #FORMTypeName element contains the string Forms, and verifies that the Forms View element is visible.

MedicalHistory: Clicks on the Medical History element, clicks on the Edit form element, clicks on the Add element, types the string Description into the #assetLocaleEditTextTextareadescription input field, clicks on the Update element, and verifies that the string Description: Description is displayed.

executeTestSuite
The executeTestSuite function imports the login, logout, and ViewForms modules and calls their respective methods in the following order:

Calls the login method from the login module using the loginData.username and loginData.password values as arguments.
Calls the viewForms method from the ViewForms module.
Calls the MedicalHistory method from the ViewForms module.
Calls the logout method from the logout module.
Overall, the executeTestSuite function simulates a user logging in, viewing some forms, editing the Medical History form, and then logging out. This test suite can be run using the Cypress testing framework.
