Download Link: https://assignmentchef.com/product/solved-itis-cs-5180-assignment13-messageme-wuth-firebase
<br>
In this assignment you will develop “MessageMe.” The App allows the user to send  and receive messages from other users. The app uses Firebase to manage the user authentication and mailbox management.

<h1>Part A: Login</h1>

This is the launcher screen of you app. The wireframe is shown in Figure 1(a). The requirements are as follows:

<ol>

 <li>The user should provide their email and password. The provided credentials should be used to authenticate the user using Firebase Authentication. Clicking the “Login” button should submit the login information to the Firebase Authentication API to verify the user’s credentials.

  <ol>

   <li>If the user is successfully logged in then start the Chat Screen, and finish the Login Screen.</li>

   <li>If the user is not successfully logged in, then show a toast message indicating that the login was not successful.</li>

  </ol></li>

 <li>Clicking the “New User?” button should start the Signup Screen Figure 1(b), and finish the login Screen.</li>

</ol>

<h1>Part B: SignUp</h1>

Create the Signup screen to match Figure 1(b), with the following requirements:

<ol>

 <li>Clicking the “Cancel” button should finish the Signup Screen and start the Login Screen.</li>

 <li>The user should provide their first name, last name, email, password and password confirmation. Preform the required validation(the given password and the repeated password must match). Clicking the “Sign Up” button should submit the user’s information to Firebase Authentication API.

  <ol>

   <li>If the signup is not successful display an error message indicating the error message received from the Firebase Authentication API.</li>

   <li>If the signup is successful, then start the Chat Screen and finish the Signup Screen.</li>

  </ol></li>

</ol>

To enable the TA to test your app, you should create all the accounts listed in Table 1.

<table width="624">

 <tbody>

  <tr>

   <td width="156"><strong>UserName</strong></td>

   <td width="156"><strong>First Name</strong></td>

   <td width="156"><strong>Last Name</strong></td>

   <td width="156"><strong>Password</strong></td>

  </tr>

  <tr>

   <td width="156"><a href="/cdn-cgi/l/email-protection" class="__cf_email__" data-cfemail="09686e606b7a6667496e276a6664">[email protected]</a></td>

   <td width="156">Austin</td>

   <td width="156">Gibson</td>

   <td width="156">test111</td>

  </tr>

  <tr>

   <td width="156"><u><a href="/cdn-cgi/l/email-protection" class="__cf_email__" data-cfemail="780b0b10190a08381f561b1715">[email protected]</a></u></td>

   <td width="156">Sally</td>

   <td width="156">Sharp</td>

   <td width="156">test222</td>

  </tr>

  <tr>

   <td width="156"><u><a href="/cdn-cgi/l/email-protection" class="__cf_email__" data-cfemail="d2a2a0b7b7a1b792b5fcb1bdbf">[email protected]</a></u></td>

   <td width="156">Phill</td>

   <td width="156">Reese</td>

   <td width="156">test333</td>

  </tr>

  <tr>

   <td width="156"><u><a href="/cdn-cgi/l/email-protection" class="__cf_email__" data-cfemail="0377606f62716843642d606c6e">[email protected]</a></u></td>

   <td width="156">Tracy</td>

   <td width="156">Clark</td>

   <td width="156">test444</td>

  </tr>

  <tr>

   <td width="156"><u><a href="/cdn-cgi/l/email-protection" class="__cf_email__" data-cfemail="bfcdd6d1dcffd891dcd0d2">[email protected]</a></u></td>

   <td width="156">Rebbeca</td>

   <td width="156">Ince</td>

   <td width="156">test555</td>

  </tr>

 </tbody>

</table>

<strong>Table 1, Users accounts to be created.</strong>

<table width="370">

 <tbody>

  <tr>

   <td width="178"></td>

   <td rowspan="2" width="13"> </td>

   <td width="178"></td>

  </tr>

  <tr>

   <td width="178">EmailPassword</td>

   <td width="178"></td>

  </tr>

 </tbody>

</table>

Inbox

<strong>BobSmith                 </strong><strong>11/8/14, 4:55 pm</strong>

<strong>Lorem ipsum dolor sit amet, consectetur  adipiscing elit Quod, inquit, quamquam…</strong>

<strong>Austin Gibson        </strong><strong>11/8/14, 10:16 am</strong>

<strong>Lorem ipsum dolor sit amet, consectetur  adipiscing elit Quod, inquit, quamquam…</strong>

<strong>Sally Sharp              </strong><strong>11/7/14, 9:15 pm</strong>

<strong>Lorem ipsum dolor sit amet, consectetur  adipiscing elit Quod, inquit, quamquam…</strong>

<strong>Phil Rees                 </strong><strong>11/7/14, 1:33 pm</strong>

<strong>Lorem ipsum dolor sit amet, consectetur  adipiscing elit Quod, inquit, quamquam…</strong>

<strong>Tracey Clark            </strong><strong>11/6/14, 8:25 pm</strong>

<strong>Lorem ipsum dolor sit amet, consectetur  adipiscing elit Quod, inquit, quamquam…</strong>

<strong>Rebecca Ince          </strong><strong>11/6/14, 10:44 am</strong>

<strong>Lorem ipsum dolor sit amet, consectetur  adipiscing elit Quod, inquit, quamquam…</strong>

(a) Login Activity                      (b) SignUp Activity                      (c) Inbox Activity

<strong>Figure 1, Wireframe for Login and SignUp Activities</strong>

<h1>Part B: Loading and Parsing Messages (Inbox Activity)</h1>

The Inbox activity should display the messages sent to the currently logged in user. The requirements are as follows:

<ol>

 <li>In Firebase design the required Realtime database to manage the users’ inbox. For each message store the message data, which includes the sender, receiver, message, and isRead (Boolean), created at and any other data required for managing the message.</li>

 <li>Retrieve all the messages sent to the currently logged in user. The message row items should be displayed as shown in Figure 1(c). The items should be displayed in descending order by the message sent date (most recent at the top and older messages at the bottom).</li>

 <li>The message row items should display the sender’s name, time/date sent, and a short preview of the message, which is two lines with maximum 45 characters in length, so format the message to fit these constraints. A blue circle beside the message row item indicates the message has not been read, and a grey circle indicates the message has been read. Use the provided image files provided.</li>

 <li>Clicking a message row item should start the ReadMsgActivity, which provides a more detailed view of the selected message item.</li>

 <li>The ActionBar should show a compose icon: Clicking the compose icon should start the ComposeMsgActivity, which allows the current user to compose a new message.</li>

 <li>The Inbox Activity should be refreshed when ever the activity is resumed to display the up to date message inbox.</li>

</ol>

<h1>Part C: Read Message Activity</h1>

The ReadMsgActivity shows details of the selected message item. The user can view the message, reply to sender, or delete the message. The requirements are as follows:

<ol>

 <li>The activity’s wireframe is shown in Figure 2(a). The UI should display the message sender’s name, and the complete message text.</li>

 <li>The message status should be updated to read status and should the updated status should be stored on Firebase.</li>

 <li>Pressing the back key should return to the Inbox Activity.</li>

 <li>The ActionBar should contain two icons: a trash, and a reply arrow.

  <ul>

   <li>Clicking the trash icon should delete the message from the user’s inbox and return to the Inbox Activity after the message is successfully deleted. The Inbox Activity should be refreshed to reflect the up to date messages stored in the user’s inbox.</li>

   <li>Clicking the reply arrow should start the</li>

  </ul></li>

</ol>

<table width="463">

 <tbody>

  <tr>

   <td width="174"></td>

   <td rowspan="7" width="113"> </td>

   <td width="176"></td>

  </tr>

  <tr>

   <td width="174"><strong>From: Bob Smith</strong></td>

   <td width="176"><strong>To: Bob Smith                        </strong></td>

  </tr>

  <tr>

   <td width="174">Lorem ipsum dolor sit amet, consectetur adipiscing elit. Beatus sibi videtur esse moriens. Memini me adesse P. Egone quaeris, inquit, quid sentiam? Certe non potest. Quis</td>

   <td rowspan="5" width="176"></td>

  </tr>

  <tr>

   <td width="174">enim redargueret? Quid me istud rogas? Duo Reges: constructio interrete. Restinguet citius, si ardentem acceperit. Ut pulsi</td>

  </tr>

  <tr>

   <td width="174">recurrant? Quid, de quo nulla dissensio est?Tollenda est atque extrahenda radicitus. Explanetur igitur. An hoc usque quaque, aliter in vita? Laboro autem non sine causa; Sed</td>

  </tr>

  <tr>

   <td width="174">fortuna fortis; Restatis igitur vos;Nam de isto magna dissensio est. Praeteritis, inquit, gaudeo. Quid ad utilitatem tantae pecuniae? Quis est tam dissimile homini. Quid sequatur, quid repugnet, vident. Facete M. Sedplane dicit quod intellegit. Iam id ipsum absurdum, maximum malum neglegi.</td>

  </tr>

  <tr>

   <td width="174">Erat enim Polemonis. Quare attende, quaeso. Urgent tamen et nihil remittunt.</td>

  </tr>

 </tbody>

</table>

(a) Read Msg Activity                                                      (b) Compose Msg Activity entered via clicking the reply button in the Read Msg Activity

<strong>Figure 2, Wireframe for Inbox Activity</strong>

<h1>Part D: Compose Message Activity</h1>

The ComposeMsgActivity allows the user to either compose a new message or reply to a message item selected from the Inbox. The requirements are as follows:

<ol>

 <li>If the Compose Message Activity is started by Read Message Activity, then the “To:” TextView should be pre-initialized with the name of original message sender, to which the user would like to reply. The user should not be allowed to change the preinitialized name. See Figure 2(b).</li>

 <li>If the Compose Message Activity is started by the Inbox activity by selecting the composed icon, then the “To: ” row should be empty, see Figure 3(a).

  <ol>

   <li>Clicking the “Contact” icon should display an alert dialog containing a list of all the full names of the users from Firebase. Selecting a name should initialize the “To: ” TextView field. See Figures 3(b)&amp;(c).</li>

  </ol></li>

 <li>After allowing the user to type in the desired message, pressing the “Send” button should upload the message to Firebase. After the message is successfully sent, a Toast message should be displayed indicating the message has been successfully sent, finish the ComposeMsgActivity and return to the Inbox Activity.</li>

</ol>

<table width="540">

 <tbody>

  <tr>

   <td width="372"></td>

   <td width="169">


    <table width="151">

     <tbody>

      <tr>

       <td width="151"></td>

      </tr>

      <tr>

       <td width="151"><strong>To: Phil Reese                      </strong></td>

      </tr>

      <tr>

       <td width="151">Lorem ipsum dolor sit amet, consectetur adipiscing elit. Beatus sibi videtur esse moriens. Memini me adesse P. Egone quaeris, inquit, quid sentiam? Certe non potest. Quis enim redargueret? Quid me istud rogas? Duo Reges: constructio interrete. Restinguet citius, si ardentem acceperit. Ut pulsi recurrant? Quid, de quo nulla dissensio est?Tollenda est atque extrahenda radicitus.</td>

      </tr>

     </tbody>

    </table></td>

  </tr>

 </tbody>

</table>

<ol>

 <li>Selecting the users icon (b) Users loaded from Firebase              (c) Sending the message</li>

</ol>

Figure 3, Wireframe for Compose Msg Activity