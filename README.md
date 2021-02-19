## How to use this repository

### Configure your project
In the Firebase console, navigate to the Authentication pane and then to the Sign-in method tab. Make sure the Anonymous provider is enabled.

49f043ed7b963b50.png

Note: For demonstration purposes, this application exclusively uses Anonymous Authentication. Anonymous Auth assigns each session-user an ID that uniquely identifies them to the backend. It enables you to create an onboarding experience that doesn't require users to create a permanent account immediately. In production applications, to save user data across sessions and devices, you'll need to convert users from Anonymous Auth to another sign in method.

### Get the source code
In this codelab, you start off with a version of The Fire Store sample that is nearly complete, so the first thing you need to do is clone the source code:

```
$ git clone https://github.com/firebase/emulators-codelab.git
```
Then move into the codelab directory, where you will work for the remainder of this codelab:

```
$ cd emulators-codelab/codelab-initial-state
```
Now, install the dependencies so you can run the code. If you're on a slower internet connection this may take a minute or two:


# Move into the functions directory, install dependencies, jump out.
```
$ cd functions && npm install && cd -
```
Get the Firebase CLI
The Emulator Suite is part of the Firebase CLI (command-line interface) which can be installed on your machine with the following command:

```
$ npm install -g firebase-tools
```
Next, confirm that you have the latest version of the CLI. This codelab should work with version 8.4.0 or higher but later versions include more bug fixes.

```
$ firebase --version
8.7.0
```
### Create a Firebase project
First run the following command to log in to the Firebase CLI:

```
$ firebase login
```

If you don't have a Firebase project, in the Firebase console, create a new Firebase project. Make a note of the Project ID you choose, you will need it later.

TODO(sdspikes): determine if project is actually needed

```
$ firebase init
```

select
```
? Which Firebase CLI features do you want to set up for this folder? Press Space to select features, then Enter to confirm your cho
ices. (Press <space> to select, <a> to toggle all, <i> to invert selection)
❯◯ Database: Configure Firebase Realtime Database and deploy rules
 ◯ Firestore: Deploy rules and create indexes for Firestore
 ◯ Functions: Configure and deploy Cloud Functions
 ◯ Hosting: Configure and deploy Firebase Hosting sites
 ◯ Storage: Deploy Cloud Storage security rules
 ◯ Emulators: Set up local emulators for Firebase features
 ◯ Remote Config: Get, deploy, and rollback configurations for Remote Config
```

```
? Which Firebase CLI features do you want to set up for this folder? Press Space to select features, then Enter to confirm your cho
ices. 
 ◉ Database: Configure Firebase Realtime Database and deploy rules
 ◉ Firestore: Deploy rules and create indexes for Firestore
 ◉ Functions: Configure and deploy Cloud Functions
 ◉ Hosting: Configure and deploy Firebase Hosting sites
 ◯ Storage: Deploy Cloud Storage security rules
❯◉ Emulators: Set up local emulators for Firebase features
 ◯ Remote Config: Get, deploy, and rollback configurations for Remote Config
 ```

```
? Please choose the location for your default Realtime Database instance: us-central1
```

```
=== Project Setup

First, let's associate this project directory with a Firebase project.
You can create multiple project aliases by running firebase use --add, 
but for now we'll just set up a default project.

? Please select an option: 
  Use an existing project 
❯ Create a new project 
  Add Firebase to an existing Google Cloud Platform project 
  Don't set up a default project 
```

Next run the following command to create a project alias. First, select your project from the list. When asked what alias you want to use, choose default.



```
$ firebase use --add
```
The output should look like the following example. Remember to choose your actual Firebase project from the list:

```
? Which project do you want to add? YOUR_PROJECT_ID
? What alias do you want to use for this project? (e.g. staging) default

Created alias default for YOUR_PROJECT_ID.
Now using alias default (YOUR_PROJECT_ID)
Now you're ready to run the app!
```

TODO(sdspikes): finish porting and modifying instructions from https://firebase.google.com/codelabs/firebase-emulator#1 for setup

## How to make contributions?

Please read and follow the steps in the [CONTRIBUTING.md](CONTRIBUTING.md)


## License

See [LICENSE](LICENSE)
