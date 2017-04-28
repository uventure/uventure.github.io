# Table of contents

* [About uVenture](#about-uventure)
* [uVenture Mockup](#mockup)
* [Installation](#installation)
* [Development history](#development-history)
  * [Milestone 1: Mockup development](#milestone-1-mockup-development)
  * [Milestone 2: Data model development](#milestone-2-data-model-development)

# About uVenture

[uVenture](http://uventure.meteorapp.com/) is a Meteor application to plan adventures for the University of Hawaii community. When you come to the site, you are greeted by the following landing page:

<img class="ui centered image" src="../images/about.PNG">

Anyone with a UH account can login to uVenture by clicking on the login button. The UH CAS authentication screen then appears and requests your UH account and password:

<img class="ui centered image" src="../images/uh-cas-auth.PNG">
 
Once authenticated, you can create a profile that provides a bio statement and list of interests, plus links to Facebook and Instagram.

<img class="ui centered image" src="../images/profile-page.PNG">

This application uses an unofficial node module of the Google Maps API made to run Google Maps in a Meteor development environment. 
<img class="ui centered image" src="../images/gmaps.png">

## Planning an adventure

The idea is that using a Map API will give users a nice and intuitive UI so that they can easily add an adventure just by placing a point on the map. Once that point is placed, a form will appear allowing the user to set-up their own adventure (hike, sightseeing, etc.). 
<img class="ui centered image" src="../images/add.png">

In addition, the user that made the adventure can edit it. 
<img class="ui centered image" src="../images/edit.png">

## Finding an adventure
uVenture also provides a find adventure page. The option to join the adventure will only be available to those who can login to the system with their UH account.
<img class="ui centered image" src="../images/find.png">
The idea behind this page is to allow users to see what adventures are out there based on the map UI. This page also has a table of all the active adventures which users can filter by the type of adventure or organize the table by alphabetical order.

# Installation

First, [install Meteor](https://www.meteor.com/install).

Second, [download a copy of BowFolios](https://github.com/ics-software-engineering/meteor-application-template/archive/master.zip), or clone it using git.
  
Third, cd into the app/ directory and install libraries with:

```
$ meteor npm install
```

Fourth, run the system with:

```
$ meteor npm run start
```

If all goes well, the application will appear at [http://localhost:3000](http://localhost:3000). If you have an account on the UH test CAS server, you can login.  

# Development History 

The development process for uVenture conformed to [Issue Driven Project Management](http://courses.ics.hawaii.edu/ics314f16/modules/project-management/) practices. Development consists of a sequence of Milestones. Milestones consist of issues corresponding to 2-3 day tasks. GitHub projects are used to manage the processing of tasks during a milestone.  

The following sections document the development history of uVenture.

## Milestone 1: Mockup development
M1: From April 4, 2017 to April 13, 2017

The goal of Milestone 1 was to create a set of HTML pages providing a mockup of the pages in the system. To simplify things, the mockup was developed as a Meteor app. This meant that each page was a template and that FlowRouter was used to implement routing to the pages. 

Mockups for the following pages were implemented during M1:

<img width="200px" src="../images/landing.png"/>
<img width="200px" src="../images/profile.png"/>
<img width="200px" src="../images/add.png"/>
<img width="200px" src="../images/edit.png"/>
<img width="200px" src="../images/find.png"/>

Milestone 1 was implemented as [uVenture GitHub Milestone M1](https://github.com/uventure/uventure/milestone/1?closed=1):
<img class="ui centered image" src="../images/milestones.png">

Milestone 1 consisted of six issues, and progress was managed via the [uVenture GitHub Project M1](https://github.com/uventure/uventure/projects/1):
<img class="ui centered image" src="../images/m1.png">

Each issue was implemented in its own branch, and merged into master when completed.
<img class="ui centered image" src="../images/git1.png">

## Milestone 2: Data model development 
M2: From April 13, 2017 to April 27, 2017

The goal of Milestone 2 is to implement Mongo Collections and the operations upon them that would support the uVenture application.  

The data model is a set of Javascript classes. BaseCollection class provides common fields and operations. ProfileCollection and AdventuresCollection classes inherit from BaseCollection and provide the persistent data structures useful for uVenture. 

ProfileCollection was added to hold basic user data such as name, email and adventure preferences. The form for the profile page has been updated.

<img class="ui centered image" src="../images/profile-page.PNG">

AdventuresCollection was added to have the adventure name, address, type, and so on.

<img class="ui centered image" src="../images/edit.png">

An FAQ page with a developer and user guide was created.

<img class="ui centered image" src="../images/user-guide.PNG">

Milestone 2 was implemented as [uVenture GitHub Milestone M2](https://github.com/uventure/uventure/milestone/2):

<img class="ui centered image" src="../images/m2-issues.PNG">

Milestone 2 consisted of seven issues, and progress was managed via the [uVenture GitHub Project M2](https://github.com/uventure/uventure/projects/2):

<img class="ui centered image" src="../images/m2-project.PNG">

Each issue was implemented in its own branch, and merged into master when completed.
<img class="ui centered image" src="../images/m2-network.PNG">
