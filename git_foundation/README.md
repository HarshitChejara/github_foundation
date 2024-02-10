-------------------------------------------------------------------
* Day-1 - from 00:00 t0 30:00 minutes of github foundation course.
* For better understand you can see the topic images in day-1 folder.
----------------------------------------------------------------------
* Topics

1. Study Guide and Objective Domains.
There are seven domains. the domains are discribe diffrent things about github like - support for users and key stakeholders, user authentication, deployed-distributed and licensed, access permission based on membership, secure software development, github actions and benefits.

2. (VCS) Version Control Systems to track changes or revisions to code.
There are four VCS - CVS 
                     Subversion 
                     Mercurial 
                     Github
there are two parts of VCS - Centralized VCS - type (CVS, Subversion)
                             Decentralized VCS - type (Mercurial, Github)  

3. About Git
It is a (DVCS) Distributed version control systems.
It contain complete a copy of the repo locally.
Each changes of your code can be captured by git commit and tracked throughout the history of your project. 

4. Common Git Terms
Repository, Commit, Tree, Remote, Branches, Clone, Checkout, Pull, Push, Fetch, Reset, Merge, Staging files. With the help of all these, you can put project on the git, create new ones, make changes etc.

5. (VCS) Version Control Services
often we call these services "git providers"
There four types of VCS - Github
                          GitLab
                          BitBucket
                          SourceForge 
This are fully managed cloud services that hosts your version controlled repositories.

6. About Github
It is a grate way to showcase your work.
It initially offered hosting managed remote git repositories and expanded to provide other offerings like - project management tools, Issue Tracking, Pull Request, Code review, Repository Hosting etc. 





-------------------------------------------------------------------
* Day-2 - from 30:00 t0 01:05 minutes of github foundation course.
* For better understand you can see the topic images in day-2 folder.
-------------------------------------------------------------------

7. Tow factor authentication for sequrity
GitHub Mobile is an application allows you to interact with github on your phone. its also use as an authentication tool for github
we can set our perferred methood to use two-factor authentication when signing into Github.  

8. Create Github Account
from github.com
enter your email, password, username then go ahed with continue and create your account.
then enter code which you get on your email.

9. Multiple Github Accounts
You can add multiple accounts for that click your profile from right corner of dashboard and set your email and password and create your another account in github.

10. Create github repository
Click New from left side on your github dashbord.
Then Select Owner if you have multiple accounts then enter repositry name, description.
Then set public for anyone can see this on internet. or dont want then choose private.
Click add README file for write description for your project. and then create repository.

11. Setup Github Organization
It collaborate with an unlimited number of people across many projects at once.
Click top right corner on dashboard. then click "Your organizations".
Then start with New organization and choose create a free organization. and create organization then invite person you want.

12. create and upload Avatar
you create Avatar from myoctocat.com and download it. 
Then go to your profile and upload it.

13. Github Octocat
It symbolizes github friendly and engaging nature in the world of software development and collabration.

14. Git VS GitHub
Git- It is DVCS, it manages source code history, it access local system installation, its scope of local repository management, its usage command-line interface, in this local changes-requires manual sharing.
GitHub - It is VCaaS, it provide cloud storage for git repositories, it accessed via web interface, its scope of online collaboration and repository hosting, its usage is graphical interface and additional features, it integrated tools for collabration.

15. GitHub Repo
It is your git repo that you push upstream to GitHub. and GitHub allows you access and manage your git repo with several functionality.





-------------------------------------------------------------------
* Day-3 - from 01:05 to 02:38 minutes of github foundation course.
-------------------------------------------------------------------

16. Git quick and dirty crash course
go in github.com/ExamProCo, then get new repo there, then click fork (this will make an copy of another referance to do it), then enter repository name there and create fork.
now open github.dev, To open the repository in the same browser tab, press . while browsing any repository or pull request on GitHub. To open the repository in a new browser tab, press > . Change the URL from "github.com" to "github.dev". When viewing a file, select the dropdown menu and click github.dev.

Then create new file in new folder, here we can do commit & push from left side icon source-control (you can see your git commits on your repo)

Then from your repo open code > codespace > create codspace on main
from here you can see the terminal which is easy to handle git commands.
we can clone three ways: HTTPS, SSH, Github CLI
since we are using Github Codespace we'll a create temporary directory in our workspace.
command : mkdir /workspace/tmp
        : cd /workspace/tmp 

Colne with HTTP:-
then for clone your project go on your repo click code >> local >> copy http path
commands : git clone (your repos http path)
         : cd Github-Examples

If we wanted to create a git repo in a new project we create the folder and the initalize that repo using 'git init'
command : mkdir /workspaces/tmp/new-project
        : cd /workspaces/tmp/new-project
        : git init
        : touch Readme.md
        : code Readme.md
        : git status
        : git add .
        // makes changes to readme.md 
        : git commit -m "add readme file"

commits - when we want to commit code we can write git commit which will open up the commit edit message in the editor of choice.
command : git commit        

Set the global editor
command : git config --global core.editor emacs

Add - When we want to stage changes that will be included in the commit we can use the "." to add all possible files.
command : git add Readme.md
        : git add .

Reset - it allows you to move Staged changes to be unstaged. this is useful when you to revert all files not to be not commited
command : git add .
        : git reset
git reset will revet a git add .       

Status - Git status shows you what files will or will not be commited.
command : git status

Log - git log will show recent git commits to the git tree 

Gitconfig file - it is what stores your global configuration for git such as email, name, editor and more.
showing the content of our .gitconfig file
command : git config --list

When you first install Git on a machine you are suppose to set up your name and email
command : git config --global user.name "Jhon Doe"
        : git config --global user.email "jhondoe@example.com"

Push - When we want to push a repo to our remote origin
command : git push

for access repo on localhost 
clone repo
then do changes and push
if its is not working.. you will need to generate a personal access token
then git dashboard >> settings >> developer settings >> personal access tokens >> fine-grained personal access tokens >> generate new token >> get token 
and write it as an password when you login. give it access to contents for Commits

Clone with SSH:-
Cpmmand : git clone (SSH path)
        : cd GitHub-Examples

we will need to create our own SSH rsa key pair
command : sshe-keygen -t rsa

For WSL users and if you create a non default key you might need to add it
command : eval `ssh-agent`
        : ssh-add /home/andrew/.ssh/alt-github_id_rsa
        
we can test our connection here
command : ssh -T git@github.com

Clone with Github CLI:-
Install the CLI 
Command : sudo apt update
        : sudo apt install gh
        : gh login
        : gh clone (your CLI path)

Branches:-
List of branches
command : git branch
create a new branch
command : git branch branch-name
checkout the branch
command : git checkout dev

Remotes:-
we can add remote but often you will just add remote via upsteam when adding a branch 
command : git remote add .
        : git branch -u origin new-feature

Merging:-
command : git checkout dev
        : git merge main

Stashing:-
command : git stash list
        : git stash
        : git stash save my-name
        : git stash apply
        : git stash pop






-------------------------------------------------------------------
* Day-4 - from 02:38 to 04:16 minutes of github foundation course.
* For better understand you can see the topic images in day-4 folder.
-------------------------------------------------------------------

17. Git Commit
it represent incremental changes to a codebase represented with a  git tree ar a spacific time.

18. Git Branch
it is a divergence of the state of the repo. also as being copies of a point in time that have been modified to be different.

19. Git Remote
it represents the reference to remote location where a copy of the repository is hosted.

20. Git Remote upstream and downstream
upstream:- the repository to which we push changes.
downstream:- the repository rhat pulls or clones from another repository.

21. GitHub Flow
it is a light-weight workflow for multiple developers working on a single repository.

22. GitHub CLI
it is a command line interface to interact with your GitHub Account.

23. SSH Keys
it is common strategy for authenticating to perform git operations on you remote GitHub reop is using SSH keys.

24. Deploy Keys
it allows you attach public keys directly to a Git Repo

25. Personal Account Access Tokens
This are an alternative to using password for authentication to GitHub when using then GitHub API or the command line.

26. GitHub APIs
GitHub has two APIs REST API and GraphQL API

27. GitHub SDKs
it is use for programmatically interact with the Git REST API. ex:- Octokit





-------------------------------------------------------------------
* Day-5 - from 04:16 to 07:08 minutes of github foundation course.
* For better understand you can see the topic images in day-5 folder.
-------------------------------------------------------------------

28. GitHub Desktop
It is a stand-alone application to interact with GitHub repos without the browser or via code. an common Git and GitHub operations can be performed via the GUI for an easy-to-use experience.

29. GitHub Desktop VS Github
Git is a version control system that helps you manage your code and keep track of it, and GitHub is a cloud-based hosting platform that enables developers to manage their Git repositories. GitHub Desktop is an application that lets users interact better with GitHub through a GUI.

30. GitHub Mobile
It is a mobile application you can install in phone to perform read-only or basic GitHub repo management tasks.

31. GitHub Mobile Notifications
You can set save, markeas read, marke as done, unsubscribe etc. this type of notifications with as you want your option(like:-swipe) and you can also change style here.

32. Types of GitHub Accounts
There are three types of GitHub Accounts:
Personal: This are individual account, they can own resources like repos-projects, actions.
Organization: In this multiple people collaborate on projects. they have also own resources but managed through individual accounts.
Enterprise: It allows for central management of multiple organizations.

33. GitHub Free VS GitHub Pro 
f you use GitHub Free, private repositories owned by your personal account have a limited feature set. You can upgrade to GitHub Pro to get a full feature set for private repositories.

34. GitHub  Organizations Plans
There are three plans: Free, Teams, Enterprise

35. GitHub Enterprises Deployment Options
It have two options: cloud(hosted on GitHub.com), Server(Self-hosted)

36. Markdown
It is an easy-to-read, easy-to-write language for formatting plain text. You can use Markdown syntax, along with some additional HTML tags, to format your writing on GitHub, in places like repository READMEs and comments on pull requests and issues.
syntax:- "`"

37. Text Formatting Toolbar
Every File on GitHub contain text formating toolbar.
It is allows you to format you text without learning markdown syntax.

38. Slah Commands
It provides convenience features such as formatting markdown.

39. GFM (GitHub Flavoured Markdown)
It is the dialect of Markdown that is currently supported for user content on GitHub.com and GitHub Enterprise.

40. Markdown on GitHub
goto your repo >> Add file >> write foldername >> create README.md >> write content >> commit changes 

41. Uploading Files
you can directly upload files by dragging them into the markdown supported textareas in GitHub.

42. GitHub User Profile Features
In your personal account you can have a piblic GitHub User profile to showcase yourself as a developer.

43. README Files
It is a markdown files that provided documentation information. In a repo this file will be rendered on the GitHub repo page page for each access.

44. Basic Repo Navigation
within a Github repo you'll have a navigation bar to the various feature of your GitHub repo.

45. Create a GitHub Repo
choose owner >> set repo name >> choose public or private >> add readme file >> create.

46. Repo Templates
This is a feature for public repos that allow other GitHub users to make a copy of the contents of the template repo.

47. Cloning a Repo
you can clone a repo in three ways: HTTPS, SSH, GitHub CLI
you can add file

48. Creating branches
using git we can create new branch. then push upstream on branch.

49. Starring repos
It is way to make a repository as interesting or to keep track of it for reference.

50. Watching Repos
It allows you to stay informed about activities occurring within a repo

51. Feature Previews
It allows you to enable or disable features that are in beta in your personals account.

52. Tags
Tagging is used to capture a point in history to marked version release of your codebase.

53. GitHub Releases
It allows you to create releases with release notes and linked assets such as zip source or binaries for specific platforms.

54. GitHub Packages
It is a platform for hosting and manageing packages, including containers and other dependencies.

55. Repo Insights
For a GitHub Repo under the Insights tab you can gain lots of statistical graphs about the repo.

56. Creating Issues
GitHub Issues are items you can create in a repository to plan, discuss and track work.

57. Issues VS Discussion VS Pull Requests

58. Create a Branch from an Issue
A common workflow is creating Feature or Bug branches. By defining your Issues upfront you quickly create branches.

59. Search and Filter Issues 

60. Issue Templates
This are markdown templates that are preloaded for new Issues.
They help ensure users creating issues provide all the relevant and expected Infprmation.

61. Issues Forms
It is the evolution of issues templates. you use a YAML formatted file to create Issue forms for stricter entry of issue information.

62. Pinning Issues
Upto 3 issues can be pinned so the appear at the top of the Issue page.

63. Pull Requests
It is a formal process to put forth changes, that can be manually or automatically reviewed before its accepted into your base (main) branch.

64. Pull Requests - Base and Compare
It determines the direction of the merge for a pull request.

65. Draft Pull Requests
Its on GitHub; feature that allows you to open a pull request but mark it as a work in progress.





-------------------------------------------------------------------
* Day-6 - from 07:08 to 09:54 minutes of github foundation course.
* For better understand you can see the topic images in day-6 folder.
-------------------------------------------------------------------

66. Linked-Activity-within-a-pull-request
You can link Issues to pull requests so that the state of the pull request will automatically close the issue.

67. Pull Request Statuses
open, draft, closed, merged, changes requested, review required, approved, conflict, ready for review.

68. Codeowners file
It define individuals or teams that are responsible for specific code in a repository

69. Pull Request Options

70. Required Reviewers
pull request can have multiple required reviewers who must write a review that approves the changes.

71. Pull Request Templates
This are similar to Issue Templates, It will populate the pull request textarea with the specified template.

72. Github Discussions
It is community communication tool for your public or private GitHub repos.

73. Notification Configuration Options, Notification Inbox
In your account settings you have a notifications tab to configure notifications options.
and notification inbox provides a chronological list of notification threads.
notification watching, subscriptions

74. GitHub Gists
It provide a simple way to share code snippets with others every gist is a Git repository which means that it can be forked and cloned.
Fork and Clone Gists

75. GitHub Wiki
It is collaborative way to quickly create documentation with multiole nested pages.

76. GitHub Pages
It allows you to directly host a static website via a GitHub repo.

77. GitHub Actions
It is a CI/CD pipeline directly integrated with your GitHub Repo.

78. Copilot
It is an AI developer tool that can be used with multiple IDEs via an extension.

79. GitHub Codespaces
It is cloud developer environment (CDE) integrated with you GitHub Repo.

80. Deep Links
It is an easy way to generate shareable link that will launch a codespace for a specific GitHub repo.

81. Dev Container Configuration 
It allows you to configure your docker container via json file.

82. GitHub.dev Editor
It is a Vs Code browser that instantly loads that has no attached comuter.

83. Open Source
It is a source code made freely available for possible modification and redistribution.

84. GitHub Sponsors
It allows GitHub users to collect donations for their GitHub hosted own-source projects.

85. GitHub and Open Source Project

86. Inner Source
It is Organization and development best practices of non-open-source and proprietary software.

87. Forking
It allows you to create a copy of a repo.

88. Discoverable repos
It can be set as public, making repos easily searchable on GitHub and via search engines.

89. Labels
This are used to categorize issues, pull req. and discussions

90. GitHub Milestones
It allows you to group multiple issue into an end goal which show completion towards the goal for each closed Issued.

91. GitHub Projects
It is a planning and tracking tool when on working on GitHub Repo.

92. Managing Saved Replies
When commenting on an issue or pull request, you can add a saved replay that you have already set up.

93. Assigning Issues and Pull Requests
you can assign issues and pull requests to specific users. you can also filter Issues.

94. Securing Account with 2FA
when you use second device to enter a code as an extra security precaution when signing-in or performing sensitive actions.

95. Access Permissions - personal accounts
It has two permissions;
Repository owner:- In this a person who owns the account, thats you.
collaborators:- In this a people you add as collaborators.

96. EMUs
It allows you to manage the lifecycle and authentication of your users on GitHub.com from an external identity management system.

97. Managing Features
GitHub Repo have multiple features we can enable or disable them.

98. Repo Permission levels
When you add a collaborator and they accept the invite. you can choose from predifined roles with different level of access.

99. Branch Protection Rules
It is used to enforce certain workflows or requirements before changes can be merged into a branch.

100. Sequrity Tab features and options
It will present a repo security checklist of security options to configure

101. Managing Collaborators
It allows you to let other GitHub users have access to your repo based on the permission levels you provide.

102. Organization Teams Tab
It can group organization members in teams.

103. GitHub Connect
It allowing your GHES (GitHub Enterprise Server) instance access some of GitHub.com cloud only offerings.

104. GitHub Internal Repos
GitHub Enterprise Cloud accounts have a third special GitHub Repo type called Internal. It is a default setting for all new repositories created in an organization owned by an enterprise account.

105. GitHub Advanced Security
GitHub make extra security features available to customers under a GitHub Advanced Security License.

106. SAML and SCIM
SAML:- It is about securely transmitting user authentication and authorization data for single sign-on purposes.
SCIM:- It is about managing user identities across different systems to simplify account maintenance and provisioning.