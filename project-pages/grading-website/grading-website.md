---
title: Grading Website
---

**[PHP Code](https://github.com/TroyNech/CP317_MLS_Project/tree/php)**
**[Python Code](https://github.com/TroyNech/CP317_MLS_Project/tree/python)**

*Note: Some of the content in this document was written by other students who worked on the project*

<body>
    <h2>Introduction</h2>
    <p>
        ezMarker is a web application that allows instructors at Wilfrid Laurier University to bulk upload grades and feedback into <a href="https://mylearningspace.wlu.ca" target="_blank"><b>MyLearningSpace (MLS)</b></a>, with the integration of the Brightspace API supported by D2L. The goal of ezMarker is to solve the issues regarding inefficient manual grade uploading through the current MyLearningSpace interface. On average, it can take markers a few hours to manually upload grades for one class. Marking time is cut down to minutes with the use of ezMarker's bulk file uploading.</p>

    <h2>General Homepage</h2>
    <p>
        If the user is not already logged in:</p>
    <ul>
        <li>
            Courses, username and logout button will be hidden</li>
    </ul>
    <ul>
        <li>
            The user will be given an option to select either Docs or Login</li>
    </ul>
    <img class="prototype-img" src="img/homepage.png" border="1">
    <h3>Documents Page</h3>
    <p>
        If Docs is selected, the user will be sent to the documents page.</p>
    <img class="prototype-img" src="img/docs_page.png" border="1">
    <h3>Login Page</h3>
    <p>
        If Login is selected, the user will be sent to the Login page. In order to login, the user
        needs to have MyLearningSpace credentials.</p>
    <img class="prototype-img" src="img/brightspace_login.png" border="1">
    <p>
        If login is unsuccessful, the user is be shown an error message, and needs to retry.</p>
    <img class="prototype-img" src="img/login_failed.png" border="1">
    <h3>Accessing the Homepage</h3>
    <p>
        The user can always access the ezMarker homepage by clicking on the ezMarker logo on the
        Navigation Bar.</p>
    <img class="prototype-img" src="img/homepage_access.png" border="1">

    <h2>User Homepage</h2>
    <p>
        Once the user is logged in they will have access to the Courses and Help page as well as the
        option to logout.</p>
    <h3>Navigation Bar</h3>
    <p>
        The user can select between Courses or Help on the navigation bar. </p>
    <ul>
        <li>
            If Courses is selected, the user will be taken to the Course List page with a list of course
            grade items.</li>
    </ul>
    <ul>
        <li>
            If Help is selected, the user will be taken to the Help page for step by step instructions on
            how to navigate the ezMarker website.</li>
    </ul>
    <img class="prototype-img" src="img/navbar_options.png" border="1">
    <p>
        The user will also be shown their name and the option to logout.</p>
    <img class="prototype-img" src="img/navbar_logout.png" border="1">
    <p><strong>Note: </strong></p>
    <ul>
        <li>
            <strong>Logging out will not redirect the user to ezMarker. Instead the user will be directed
                to the Brightspace instance.</strong></li>
    </ul>

    <h2>Course List Page</h2>
    <p>
        Upon login or selection, the user is taken to the Courses page where the user can select a
        Grade Item to update or review.</p>
    <img class="prototype-img" src="img/course_listpage.png" border="1">
    <p>
        To modify a specific course, the user can select that course and expand it to show the
        course's individual grade items. If a grade item is clicked the user will be taken to the
        Grade Item page.</p>
    <img class="prototype-img" src="img/gradeitem_a1.png" border="1">

    <h2>Grade Item page</h2>
    <p>
        Once the user selects a grade item, they are redirected to the grade item page. This page
        allows the user to:</p>
    <ul>
        <li>
            Change Grade Maximum: Give user the ability to change the max grade limit</li>
    </ul>
    <ul>
        <li>
            Automated Upload: Give user the ability to upload an Autograder file</li>
    </ul>
    <ul>
        <li>
            Manual Grade Input: Give user the ability to update student grades manually</li>
    </ul>
    <img class="prototype-img" src="img/gradeitems_page.png" border="1">


    <h3> Change Maximum Grade</h3>
    <p>
        The user can update the grade item's maximum grade value by entering a positive number and
        submitting the form with Update Grade Maximum button. The user can also use the Enter key to
        submit Grade Maximum update.
    </p>
    <img class="prototype-img" src="img/update_grade_max.png" border="1">
    <h4>Confirm update </h4>
    <p>
        When the user submits the form, a message appears to confirm the user wants to proceed.</p>
    <img class="prototype-img" src="img/confirm_update_max.png">
    <h4>Successful update </h4>
    <p>
        If the user confirms and they submit a valid grade maximum, a success message will appear and
        the UI will be updated appropriately.</p>
    <img class="prototype-img" src="img/update_max_success.png" border="1">
    <h4>Invalid update </h4>
    <p>
        If an invalid grade maximum is given, an error message will appear and the user will have to
        check their input.</p>
    <img class="prototype-img" src="img/update_max_error.png" border="1">


    <h3> Automated Upload </h3>
    <p>
        The user is prompted to choose a file to upload that follows the Autograder file format of
        <strong>brightspace_id, grade, name, comment</strong>.
    </p>
    <img class="prototype-img" src="img/automated_upload.png" border="1">
    <h4>Upload successful</h4>
    <p>
        If the file is valid and grades are uploaded through the Brightspace API, the user is brought
        to the report page.
    </p>
    <p>Note:</p>
    <ul>
        <li>
            The comment for student feedback is not required.</li>
    </ul>
    <img class="prototype-img" src="img/auto_reports_page.png" border="1">
    <p></p>
    <h4>Upload error</h4>
    <p>
        If the file is invalid an error message will be shown. There are cases where the file is
        valid but if the marks are invalid, a pop-up will appear to give the user a chance to correct
        the errors and re-submit.</p>
    <img class="prototype-img" src="img/automated_upload_error.png" border="1">


    <h3> Manual Grade Input</h3>

    <p>
        The user can also upload grades manually.</p>
    <img class="prototype-img" src="img/manual_grade_input.png" border="1">

    <h4>Adding students</h4>
    <p>
        Students can be added in 3 ways:</p>
    <ul>
        <li>
            Search for a student using their name</li>
    </ul>
    <img class="prototype-img" src="img/manual_input_name.png" border="1">
    <ul>
        <li>
            Search for a student using their ID</li>
    </ul>
    <img class="prototype-img" src="img/manual_input_id.png" border="1">
    <ul>
        <li>
            Select all option will quickly add input boxes for all students</li>
    </ul>
    <img class="prototype-img" src="img/manual_input_all.png" border="1">
    <h4>Removing students</h4>
    <p>
        Once a student is added, they can be removed by hitting the X- button beside their name. A message in red will
        appear indicating which student was removed. </p>
    <img class="prototype-img" src="img/manual_grade_remove.png" border="1">

    <h4>Grade input successful</h4>
    <p>
        Grade input is required and must be a positive number. Some grade items allow for the grade to
        exceed the maximum grade value, while others do not.
    </p>
    <p>Note:</p>
    <ul>
        <li>The comment for student feedback is not required.</li>
    </ul>

    <h4>Grade input error</h4>
    <p>
        If there are any errors with the user's upload, a pop-up will appear with an appropriate
        warning or error message. The user must fix these issues and re-submit to successfully upload
        student grade, otherwise cancel their upload. If the grade item does not allow inputted
        grades to be greater than the maxamum grade value, an error message will appear if the
        inputted grade exceed the max value. In this case, the user is forced to input a grade less
        than or equal to the maximum grade value.
    </p>
    <img class="prototype-img" src="img/manual_upload_error.png" border="1">
    <h4>Grade input warning</h4>
    <p>
        A warning message saying the inputted grade exceeds the grade item's maximum grade value may
        be ignored. The UI is just confirming
        with the user that this was their intention.</p>
    <img class="prototype-img" src="img/manual_upload_warning.png" border="1">

    <h2>Report Page</h2>
    <p>
        The report page shows a summary of the user's upload. It shows how many grades were
        successfully set by the Brightspace API, any errors from the API, and a summary of the
        students that had their grades changed.
    </p>
    <img class="prototype-img" src="img/report_page_help.png" border="1">

    <h2>Logout Page</h2>
    <p>
        The user can logout (end their MLS session) by pressing the logout button of the navigation
        bar. </p>
    <img class="prototype-img" src="img/logout.png" border="1">

    <p><strong>Note: </strong></p>
    <ul>
        <li>
            <strong>Logging out will not redirect the user to ezMarker. Instead the user will be directed
                to the Brightspace instance.</strong></li>
    </ul>

</body>

<style>
    img {
        width: 65%;
        margin: 20px 0px;
    }

    prototype-img
{
	width: 80%;
	border: 1px solid #330072;
}

</style>
