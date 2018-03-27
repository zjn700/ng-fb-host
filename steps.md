
# ng-fb-host
## Angular Firebase Hosting


# Preflight

# make sure you have the right version of node installed (6 or greater)
    nvm ls
    
# here are the results from my current config:
->      v6.11.2
         system
default -> 6 (-> v6.11.2)
node -> stable (-> v6.11.2) (default)
stable -> 6.11 (-> v6.11.2) (default)
iojs -> N/A (default)

# if angular cli is not installed run:
    npm install -g @angular/cli


# Creating an Angular App

# create a new app
    ng new ng-fb-host

# go into our new app
    cd ng-fb-host

# serve it locally and see it in action
    ng serve --host 0.0.0.0 --port 8080 --disable-host-check


# Creating the Firebase App

# go to firebase. open account if you don't have one. then create app of same name as the angular app
# then install the firebase tools here
    npm install -g firebase-tools


# Installing the Firebase Tools

# login to firebase from the command line
# for c9 add --no-localhost...go to the printed url to get/copy a authorization code
# paste the code and hit enter 
    firebase login --no-localhost


# Using Firebase In Our Angular App

# initialize the firebase in the angular app
    firebase init

# Answer the resulting questions
# select firebase features you want (space bar selects, arrow keys move between options, enter when done)
# change public folder to dist, when prompted

# Here's the answers to the questions Firebase tools will ask:
    Are you ready to proceed? Yes
    Which Firebase CLI features? Hosting (In the future, use whatever you need! Press space to select.)
    Select a default Firebase project? ng-fb-host (Choose whatever app you created in the earlier steps)
    What do you want to use as your public directory? dist (This is important! Angular creates the dist folder.)
    Configure as a single-page app? Yes


# Deploying

# Build the angular app, which creates the angular dist folder
    ng build --prod


# deploy the production app to firebase
    firebase deploy

# open the app...of course, this does not work from c9, but it will give you the url
    firebase open hosting:site


https://ng-fb-host.firebaseapp.com


# Update app by rebuilding and redeploying
    ng build --prod
    firebase deploy

## may have to refresh screen of firebase 


# Github
    git status
    git add .
    git status
    git commit -m 'your commit message'

# create a repository in github. i used the same name (ng-fb-host)

## then push the existing repository from the command line:
    git remote add origin https://github.com/zjn700/ng-fb-host.git
    git push -u origin master

https://github.com/zjn700/ng-fb-host




REFERENCE:
https://scotch.io/tutorials/deploying-an-angular-cli-app-to-production-with-firebase