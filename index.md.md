![[Pictures/gitlab-logo-100.png | 250]]

# Gitlab User Manual

*The following document is a manual which aims to be a guide for agile work space GitLab*

## Introduction to GitLab
GitLab aims to bring teams together and tackle all aspects of the agile development in one Development Operations Platform.   
As the name entails the main software that GitLab runs off of would be Git, aka the Global Information Transformation. Git is a open source software that tracks file changes and branching to allow for programmers to collaborate with eachother while developing source code. 

## Accounts
### Account Creation
### SSH Keys

## Repositories 
### Create Repo


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

## Activity

## Dashboards 
### Environments Dashboard
### Operations Dashboard
### Security Dashboard 
