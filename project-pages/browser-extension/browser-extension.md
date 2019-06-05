---
title: Course Registration Browser Extension
---   

<head>
    <link rel="stylesheet" href="css/help.css">
</head>

**[Code](https://github.com/TroyNech/CP476-BrowserExtension)**

<body>
    <h1>LaurierLinks User Guide</h1>
    <hr>
    <img src="images/help/extension.png">
    <h1>Login/Register</h1>
    <p>All functionality is disabled until the user logs in.</p>
    <h2>Login</h2>
    <p>Enter a previously registered email with corresponding password, then click Login. If the login is invalid, an alert
        appears. If it is valid, the following happens:</p>
    <ul>
        <li>A success icon will briefly display</li>
        <li>The Login tab will close and transition into a logout button</li>
        <li>The other tabs will be unlocked</li>
    </ul>
    <img src="images/help/successfulLogin.png">
    <h2>Register</h2>
    <p>To register, enter an email and password, then click Register. Confirm the password in the Confirm Password field that
        appears, then click Register again. An appropriate error message appears if the passwords do not match or if the
        email is already registered. If the registration is successful, an acknowledgement message appears, then the same
        tab actions occur as on a successful login.</p>
    <img src="images/help/register.png">
    <img src="images/help/successfulRegister.png">
    <h1>Logout</h1>
    <img src="images/help/logout.png">
    <p>Click the logout tab to logout.</p>
    <h1>Add Course</h1>
    <img src="images/help/addCourse.png">
    <p>Enter the course code and select the term of the course to add. The term is used to determine the start of the course's
        semester. The year of the semester is determined as follows:</p>
    <ul>
        <li>Fall: The current year</li>
        <li>Winter: The next year</li>
        <li>Spring: The year of the current month plus 1</li>
    </ul>
    <p>An error message appears if the term and course code combination is invalid. If it is valid, a success message appears.</p>
    <img src="images/help/invalidCourse.png">
    <br>
    <br>
    <img src="images/help/courseAdded.png">
    <h1>Saved Courses</h1>
    <img src="images/help/savedCourses.png">
    <p>Click on a course to add it to the Course Detail page. The page will opened if it is not currently the active tab.</p>
    <img src="images/help/courseDetail.png">
    <p>Click the Remove Icon to remove a course from the list of saved course. The course will transition out of the popup.</p>
    <img src="images/help/removingCourse.gif">
    <h1>Add Schedule</h1>
    <img src="images/help/addSchedule.png">
    <p>The Add Schedule tab allows users to save the active VSB schedule.</p>
    <p>If the VSB is not open on the current tab, the Add Schedule tab acts as a button that redirects to the VSB.</p>
    <img src="images/help/addScheduleRedirect.png">
    <p>
        <em>VSB:
            <a href="https://scheduleme.wlu.ca/vsb" target="_blank">https://scheduleme.wlu.ca/vsb</a>
        </em>
    </p>
    <p>A success message appears when a schedule is added, like when a course is added.</p>
    <h1>Saved Schedules</h1>
    <img src="images/help/savedSchedules.png">
    <p>Click a schedule to open the corresponing VSB page.</p>
    <p>Click the Remove Icon to remove a schedule from the list. The schedule will transition out of the popup, like when a
        course is removed.</p>
    <h1>Register Courses</h1>
    <p>This tab is only available on the VSB page. When clicked, the extension takes the CRNs of the courses currently on the
        VSB page and autofills them into LORIS' Registration page.</p>
    <p>The user is prompted to enter their LORIS credentials. The extension then attempts to login and navigate through LORIS
        to the Registration page, on which it will autofill the CRNs from the VSB page. It is left to the user to finish
        the registration process by clicking Submit.</p>
    <img src="images/help/vsbCrns.png">
    <br>
    <br>
    <img src="images/help/registration.gif" style="max-width: 600px">
    <h1>Help</h1>
    <p>Click the Help icon at the bottom of the popup window to open the Help page (this page).</p>
    <h1>Install Instructions</h1>
    <ul>
        <li>Download the .zip file from
            <a href="https://github.com/TroyNech/CP476-BrowserExtension/blob/prod/extension.zip" target="_blank">https://github.com/TroyNech/CP476-BrowserExtension/blob/prod/extension.zip</a>
            <ul>
                <li>
                    <em>Note: The unzipped folder has been provided in the project submission</em>
                </li>
            </ul>
        </li>
        <li>Unzip the file into the desired install directory</li>
        <li>In Chrome, open
            <a href="chrome://extensions/" target="_blank">chrome://extensions/</a>
        </li>
        <li>Enable Developer Mode</li>
        <li>Click Load Unpacked and select the extension folder</li>
        <li>Disable Developer Mode</li>
        <li>Done!</li>
    </ul>
</body>