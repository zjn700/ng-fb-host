
# ng-fb-host

# Preflight


nvm ls
->      v6.11.2
         system
default -> 6 (-> v6.11.2)
node -> stable (-> v6.11.2) (default)
stable -> 6.11 (-> v6.11.2) (default)
iojs -> N/A (default)

# if angular cli is not installed run:
    npm install -g @angular/cli
## otherwise:


# Creating an Angular App

# create a new app
ng new ng-fb-host

# go into our new app
cd ng-fb-host

# serve it locally and see it in action
ng serve --host 0.0.0.0 --disable-host-check


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

# answer the resulting questions
Here's the answers to the questions Firebase tools will ask:

Are you ready to proceed? Yes
Which Firebase CLI features? Hosting (In the future, use whatever you need! Press space to select.)
Select a default Firebase project? ng-fb-host (Choose whatever app you created in the earlier steps)
What do you want to use as your public directory? dist (This is important! Angular creates the dist folder.)
Configure as a single-page app? Yes


# Deploying

# Build the angular app, which creates the angular dist folder
ng build --prod

# select firebase features you want (space bar selects, arrow keys move between options, enter when done)
# change public folder to dist, when prompted


# deploy the production app to firebase
firebase deploy

# open the app...of course, this does not work from c9, but it will give you the url
https://ng-fb-host.firebaseapp.com

firebase open hosting:site

https://github.com/zjn700/ng-fb-host


REFERENCE:
https://scotch.io/tutorials/deploying-an-angular-cli-app-to-production-with-firebase