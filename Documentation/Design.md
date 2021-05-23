# Design Documentation 

## Storyboard Layout
We sought out to make RoommateHub as applicable and relevant to students in the real world as possible and therefore took a lot of feedback from fellow classmates as well as other iOS apps which we really enjoyed. Upon loading the app, users are greeted with a login page prompting them to enter their email, password, and room credentials. We stored all our data in the Firebase Realtime Database, which essentially serves as a master JSON file. We implemented user authentication with firebas which ensures that each user is a distinct case with security (users need a email, password, and dorm address to access their own information). By sorting items by room credentials, we were able to narrow the scope of children in the database to only include those which pertained to the users’ specific room. First-time users have the option to create their user account before logging in again. 

Once the user is past the login page, users are greeted by a simple yet eye-catching home page. The central banner displays the user’s name and room and 3 buttons lie below: Roommates, Task List, and Messages.

Selecting the Roommates button directs users to a UITableView of all the other user profiles that signed up for same room. The dorm and dorm number are used to make a unique room id which is used to connect roommate to each other and their relevant data. Users can click into any listed roommate profile. There, they can see primary information about the selected person (first name, last name, concentration, hometown, etc.) and also have the option to send them an iMessage or SMS right from the app (this feature is only available on a phone, not simulator, because of callerID). 

Selecting the Task List button directs users to a UITableViewController with an option to create new tasks. First all the related task data for a specific room id is gathered from firebase and appended to a master array of tasks which is then accessed and manipulated for all the other Task List functionalities. Users can create a new task by pressing the "+" button on the upper right which segues you to a new page that prompts the user for some text (the task you want to add). There is also a switch on this page that denotes whether a task is important or not. If a task is important, there will be a red exlaimation point next to it on the UITableViewController. By tapping the add button, the task is created and the user is brought back to the  UITableViewController with the list of tasks. By tapping a cell, the user is brought to a page allows a task to be marked as completed. If the "complete" button is clicked, it is hidden from the user and taken off screen. The user can then click the upper left button to go back to the task list page. To see the changes on the list, however, the user must go back one more page (to the homepage with the three buttons to Roommate, Task List, and Message Board). Clicking on and entering TaskList would reveal that the list is updated to exclude the tasks that were marked as complete. Clicking the "Completed Items" button on the top right would reveal a list of the completed items.

Finally, selecting the Message button directs the user to another UITableView with options to click into anonymous messages. Users will have the option to submit an anonymous message that can be viewed by users connected with the unique room id (roommates). However, once the messages are created they save into the firebase and are immutable. As college students with multiple roommates, we thought that having an anonymous message board would be a pretty useful feature that our users would enjoy.

And of course, users have the option of logging out in the home page which pops you back to the login/sign up page.

## Designing the UI/UX 
When it came to design, we wanted RoommateHub to be modern, simplistis, and fun. Our primary colors of indigo, white, and black give the app a clean user interface, but adding emojis to various pages injects small bursts of colors and fun which keep users engaged. 
Overall, RoommateHub is an app that we would certainly find useful as college students and our hope is that our fellow classmates feel the same way. 