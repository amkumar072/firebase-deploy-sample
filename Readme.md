# Deploy ionic application in firebase

## Installation

Make sure you have installed the firebase-tools. If not, please find the following command to install

```
npm install -g firebase-tools
```

## Login & Test the connection

1. Login to Firebase.

```
firebase login:ci
```

![Firebase](/images/firebase_ci.jpg)

2. Check the list of projects available. It display the list of project's available.

```
firebase projects:list
```

![Firebase project list](/images/firebase_list.jpg)

## Initilize a project

Initilize the project with the following command.

```
firebase init
```

Follow as per instructions and pick the Hosting and then select the project.
Post selection set of question will pop up

- What do you want to use as your public directory? - Mention your build folder (e.g www).

- Configure as a single-page app (rewrite all urls to /index.html)? - No

- Set up automatic builds and deploys with GitHub? - Y

It request you to authorize the GitHub by CLI url.

- For which GitHub repository would you like to set up a GitHub workflow? (format: user/repository) - Updated the user and repository (e.g amkumar072/firebase-deploy-sample)

It will setup an account FIREBASE_SERVICE_ACCOUNT for your project.

- Set up the workflow to run a build script before every deploy? (y/N) - Select depend upon your request. I have selected YES, then next question will appear.

- What script should be run before every deploy? (npm ci && npm run build) - Provide the build script/commands or else press enter to take default.

* Set up automatic deployment to your site's live channel when a PR is merged? (Y/n) - Select depend upon your request. I have selected NO.

Initilization is completed. By the time you would able to see the 3 files are created

- .firebaserc
- firebase.json
- firebase-hosting-pull-request.yml

![Firebase init](/images/firebase_init.jpg)

![Firebase commands](/images/firebase_cmds.jpg)

## Deploy to Firebase
