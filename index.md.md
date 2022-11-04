![[Pictures/gitlab-logo-100.png | 250]]

# Gitlab User Manual

*The following document is a manual which aims to be a guide for agile work space GitLab*

-------------------------------------------------------------------------------

## Introduction to GitLab

GitLab aims to bring teams together and tackle all aspects of the agile development in one free Development Operations Platform.   

As the name entails the main software that GitLab runs off of would be Git, aka the Global Information Transformation. Git is a open source software that tracks file changes and branching to allow for programmers to collaborate with eachother while developing source code. 

-------------------------------------------------------------------------------

## Accounts

A gitlab account is needed to access all the features of the agile development platform.

### Account Creation

The home page for https://gitlab.com is just information about what the platform is capable of and features that you would recieve when you sign up. The portal to loging in and account creation is on the top right of the homepage with the button being `Login`.

![[home-page.png | 700]] 

After hitting the `Login` button it will take you to the following screen where you can login if you already have an account, register for a dedicated gitlab account, or sign in using a third party account like google. 

![[login-page.png | 400]]

To create an account the navigation you would go would either be the [[https://gitlab.com/users/sign_up |Register now]] hyperlink or signing in with the third party. After hitting the [[https://gitlab.com/users/sign_up |Register now]] hyperlink the following screen prompts to create an account as well as gives you another chance to sign in with a third party account. 


![[register-page.png | 400]]

There will be a verification for your account but once that is done you are logged in your homepage for [[https://gitlab.com |GitLab]] should change to a completely different page where you have access to all of GitLab's functionality. 

![[logged-in-homepage.png | 700]]

### Basic Settings and Preferences

Just like any good collaboration space for developers, GitLab allows for you to change account information as well as preferences to add a little bit of uniqueness to your GitLab experience. The way to access this is from your homepage and hit the profile drop down on the top right. 

![[profile-dropdown.png | 400]]

There are four options on this dropdown: `Set status`, `Edit profile`, `Preferences`, and `Sign out`. The most obvious one would be `Sign out` where it would take you back to the original GitLab page prior to being signed in to your account. You can also set your status with the `Set status` button which allows for you to broadcast to your fellow collaborators how you are currently feeling and if you are currently busy.

![[set-status.png]]

The last two drop down options both take you to the User Settings in different tabs, with `Edit profile` going to the profile tab of User Settings. This page is where you can change your main profile settings like TimeZone, Avatar, and little about yourself in the User Information. 

![[user-profile.png]]

As expected the `Preferences` button takes you to the Preferences tab of the User Settings and the following is what you can do in each tab:
- Profile: Houses your main profile settings
- Account: Allows for you to change your username and manage other acconts with 2FA (Two-Factor-Authentication)
- Billing: Current User Git Plan and monthly charge
- Applications: Place to manage applications that can use GitLab as an OAuth provider
- Chat: Shows your acconts chats
- Account Tokens: Where you would create personal account tokens for your API's
- Emails: Place for you to link more emails to your Git Account
- Password: Where you change your password for your Git Account
- Notification: Manage your notifications for your emails and what notifications Git sends you
- SSH Keys: Key to access git from your computer
- GPG Keys: Key to allow for verification of commits
- Preferences: Customize how your Git looks through Themes and Styles
- Active Sessions: Shows GitLab session ran on which devices
- Authentication Log: Security log of authentication events
- Usage Quotas: GitLab usage charts 


-------------------------------------------------------------------------------

## Repositories 

A **repository** is a directory or folder that is stored in your GitLab account. GitLab acts as a version control system for your repository, which means that GitLab allows changes to your repository to be easily moderated. In this **repository** section of the manual, you will learn how to create a remote repository in GitLab, clone that repository to your local machine, and push changes from your local repository to your remote GitLab repository.

### Creating a Remote Repository in GitLab

GitLab provides a way to very easily create a repository on your account. To create a repository, you must have a GitLab account. For information on how to create a GitLab account, refer to the "Creating Account" section above. The repository hosted on your GitLab account is referred to as a **remote** repository, because it is stored remotely on the web. 

1. Navigate to your GitLab Dashboard. If you are currently signed in to GitLab, then navigating to https://gitlab.com/ should take you to the dashboard. The dashboard page looks like this if you don't have any projects:

![[Pasted image 20221027124044.png]]

If you do have projects, the dashboard looks like this:

![[Pasted image 20221027130632.png]]

2. Click "Create a Project" (or "New project"). This should navigate you to https://gitlab.com/projects/new.
3. Click on "Create Blank Project". If you wish, you may also explore available templates by clicking "Create from Template".
4. You should see a page that has text boxes corresponding to "Project name" and "Project slug". The URL of the webpage is https://gitlab.com/projects/new#blank_project. Here's what it looks like:

![[Pasted image 20221027124848.png]]

5. Type the name of your project into the text box that says "My awesome project". This should automatically populate the "Project slug" text box. If you would like to have a different project slug, replace the automatically generated text in the text box with whatever you would like your slug to be.
6. Make sure the check box that says "Initialize repository with a README" is checked.

![[Pasted image 20221027125614.png]]

7. (OPTIONAL) If you would like to set a deployment target or change the Visibility Level of your repository, you may do so now.
8. Click the button that says "Create project".
9. This will create the repository, and navigate you to the webpage for your new repository.
10. To find your repository from any point on the GitLab website, just click on the fox icon in the top left, look for your repository in the list, and click on it:
![[Pasted image 20221027131102.png]]

![[Pasted image 20221027131234.png]]

### Cloning a Repository

To be able to make edits to the code in your repository, you have to be able to **clone** your remote GitLab repository onto your local machine. Cloning a repository will allow you to have access to the code in your remote repository on your local machine. To clone a repository, you will need to have access to a terminal on your computer. For this demonstration, Git Bash will be the terminal used. If you would like to download Git Bash, consult https://git-scm.com/downloads. After you have a terminal on your machine that you are comfortable using, you can follow this guide to clone a repository onto your local system. 

There are two primary methods of cloning a repository: Using HTTPS, and using SSH. Both methods will be discussed in this guide.

#### Cloning with HTTPS

1. On GitLab, navigate to your desired repository. Navigating to an existing repository in GitLab is outlined in Step 10 of the "Creating a Repository in Gitlab" section above, or by typing a link of the form https://gitlab.com/{YOUR_USERNAME_HERE}/{YOUR_PROJECT_SLUG_HERE}
2. Click on the button that says "Clone":

![[Pasted image 20221104111859.png]]

4. Click the clipboard icon next to the text box labeled "Clone with HTTPS":

![[Pasted image 20221027154233.png]]

This will copy the HTTPS address of the repository to your clipboard. 

4. Open the terminal of your choice, and navigate to the directory you would like to put your repository in using the `cd` command. If you need to create a directory to house your repository, you can use the `mkdir` command to create one.

![[Pasted image 20221027154915.png]]

5. Input the following command:
	`$ git clone {Paste URL you copied in Step 3}`
	Note that in Git Bash you can paste text by right clicking with the mouse and then selecting "Paste". Press enter to execute the command. If prompted, enter your Gitlab username and password. If you were prompted for your username and password, the output should look like this:

![[Pasted image 20221027155627.png]]

Otherwise, the output should look something like this:

![[Pasted image 20221027160803.png]]

6. Enter the command `$ ls` into your terminal. This will list directories and files inside your current working directory. You should see a directory whose name matches the **project slug** of your repository. Navigate into that directory using `$ cd {Directory Name}`.

![[Pasted image 20221027161322.png]]

7. The directory which as the same name as your **project slug** is the cloned repository. In Git Bash, there will be a word in parenthesis (probably "main"), which indicates that you are inside your repository!
8. Congratulations! You have successfully cloned your remote Gitlab repository using HTTPS!

#### Cloning with SSH

If you would prefer cloning the repository using SSH, you must have an SSH key associated with your machine on your GitLab account. For instructions on how to do this, consult the "Creating an SSH Key" guide in the "Creating Account" section above.

1. On Gitlab, navigate to your desired repository. Navigating to an existing repository in GitLab is outlined in Step 10 of the "Creating a Repository in GitLab" section above, or by typing a link of the form https://gitlab.com/{YOUR_USERNAME_HERE}/{YOUR_PROJECT_SLUG_HERE}
2. Click on the button that says "Clone"
3. Click the clipboard icon next to the text box labeled "Clone with SSH":

![[Pasted image 20221027162555.png]]

4. Follow Steps 4-7 in the "Cloning with HTTPS" guide above. Some of the screenshots will look slightly different from your output; don't be alarmed by this. 

### Pushing Code to a Repository

To **push** to a repository means to take changes you've made to your local repository and put them into your repository on GitLab. This requires that you have your repository created in GitLab, and cloned on your local machine. For the purposes of this demonstration, we will just add a `.txt` file with some text. However, pushing will usually be done with code or documentation files in practice.

1. Create a file named "HelloWorld.txt" and open it. On Windows, this can be done by typing the command 
    `$ notepad HelloWorld.txt` 
    and then clicking "yes" if prompted to create a new file.
    
![[Pasted image 20221031101935.png]]

![[Pasted image 20221031101857 1.png]]

2. Make a change to the file and save it. You can now exit your text editor.

![[Pasted image 20221031102151.png]]

3. You now have a change on your local repository that is not yet on the remote repository on GitLab. To view your changes, enter the command `$ git status` :

![[Pasted image 20221031114455.png]]

4. Sets of changes are pushed to the remote GitLab repository in groups. A group of changes to be pushed to the remote repository is called a **commit**. To add a file to a commit, use the command `$ git add { file name(s) }`, or use `$ git add .` to add everything in your current working directory. You can then do another `$ git status` to verify that your file has been added to the commit:

![[Pasted image 20221031115026.png]]

5. Now that you have added the files you wish to commit and push to GitLab, its time to make the commit. This wraps your changes up nice and neatly so that you can push them as a group, and come back to them later if needed. To commit your added changes, input this command:
	`$ git commit -m "{Enter a message about your commit here}"`

![[Pasted image 20221031115427.png]]

6. Now that you have made your commit, you can push that commit to GitLab. To do this, use the command :
	`$ git push` 
	If you've done things correctly, your output should look similar to the screenshot below:

![[Pasted image 20221031115544.png]]

7. Now that you've pushed your commit, you should be able to see your commit on your GitLab repository. It is a good idea to verify that your commit was pushed to GitLab correctly. To find your commit, navigate to your GitLab repository. You should be able to see the latest commit in a card right underneath the button labelled "Clone":

![[Pasted image 20221031120010.png]]

If not, you can click on the "Commits" button (highlighted in red above). This will take you to a page that contains **all** commits to your repository. 

![[Pasted image 20221031120150.png]]

The bolded text on the commit should match the commit message you inputed in Step 5. Congratulations! You've successfully pushed changes you made on your local machine to your remote GitLab repository.

-------------------------------------------------------------------------------

## Collaboration

## Issues

A useful feature of GitLab is the advanced issue tracking. An issue is any bug or feature request that is to be added. These can be created by the end user through the service desk or by the develpers themselves. This can be used as a Scrum board (similar to kanban board) to better track what each team member is doing. Each issue has multiple properties to aid in sorting and visualize. 
### Issue Creation

1. Navigate to either List or Boards under the issues tab. In this example we will use the List tab.

![[IssuesListSelected.png]]

2. Then select the New Issue button to bring up the Issue creation page.

![[IssuesNewIssueButton.png]]

3. The issue needs a name. To better use issues, it is recommended to give each issue a type, description, and applicable labels. For collaboration you can assign any developer in the repository quickly. We will see this on the issue board later.

![[IssuesCreateNewIssue.png]]

4. Finally select the create issue button to finish creating your issue. This will take you to the issue's new page. This is a great place to see all of the detail relating to the issue and update any information that is missing.

![[IssuesMainIssuePage.png]]

Returning to the original list page you can now see the issue you have created. While the list view gives a good overview, it is difficult to navigate. This is where the boards page comes in.

### Boards

Boards help organize the teams work flow and provides a great visual for both the developers and the project managers. This creates a central place to track the design and implementation of new features. Selecting this page under issues, you can see the issue you just created under open. By default there is only the open and closed column, but these can be expanded to meet your needs. We will walk through creating a in progress column to be able to show what is actively being worked on:

![[IssuesBoardDefault.png]]

1. First start by selecting Create List and select which tag this list should track. Here we have created a new tag called InWork. This can be done under the issue page mentioned before.

![[IssuesCreateList.png]]

2. After adding this to the board you will now be able to drag and drop issues between lists to organize your work flow and edit the tag automatically.

![[IssuesMovedIssue.png]]

As you can see this has allowed us to shift each issue individually between steps in the development process. Clicking each issue will open a side bar summary of the issue, allowing for quick edits. This also displays each developer assigned icon by the issue so at a glance it is clear what each person is working on. 

### Service Desk

Until now we have only covered how the developers can interact with issues. GitLab provides a way for the end user to send a direct issue to the board via the Service Desk feature. This automatically creates an email the user can submit issues to.

![[IssuesServiceDeck.png]]

1. Selecting the service desk will provide you with this email. This email can be embeded into a built in help features or provided directly to users. This can be customized to the repository.
## Snippets

The snippets tab is a place to store your code snippets. Small pieces of code that have it's independent functionality that you can share with the rest of your team. 

![[Pasted image 20221101114526.png]]

There are two tabs here, one for your current snippets and the other is for Exploring other snippets. 
On the Explore snippets you can see the most recently created public snippets.

![[Pasted image 20221101114755.png]]

To create a snippet all you have to do is hit `New snippet` on the "Your snippets" tab, there is also a button that links to the documentation behind how code snippets work if that is what you are looking for.

![[Pasted image 20221101114846.png]]

When you press `New snippet` you it allows for you to enter a Title, Description, File Name, the code you want in that snippet, optional more files, and whether the code snippet is private or public. 

![[Pasted image 20221101115213.png]]

The following is what it looks like after you have created a code snippet and the options it gives you to fiddle with it.

![[Pasted image 20221101115429.png]]

The Snippets page will have also added that as well and increase tabs for Private, Internal, Public, and All of you code snippets. 

![[Pasted image 20221101115534.png]]

