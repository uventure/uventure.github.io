# Table of contents

* [About uVenture](#about-uventure)
* [uVenture Mockup](#mockup)
* [Installation](#installation)
* [Development history](#development-history)
  * [Milestone 1: Mockup development](#milestone-1-mockup-development)
  * [Milestone 2: Data model development](#milestone-2-data-model-development)
  * [Milestone 3: Test and polish](#milestone-3-test-and-polish)
  * [Initial User Study](#initial-user-study)


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
The idea behind this page is to allow users to see what adventures are out there based on the map UI. This page also has a table of all the active adventures ordered by the newest adventure out there.

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

An FAQ page was created and contains the following:

**User Guide**

<img class="ui centered medium image"  src="../images/user-guide.PNG">

**Developer Guide**

<img class="ui centered medium image"  src="../images/dev-guide.PNG">

**Terms of Service**

<img class="ui centered medium image" src="../images/tos.PNG">

A mockup page for the suggested adventures was created.

<img class="ui centered image" src="../images/m2-suggested-mockup.PNG">

Milestone 2 was implemented as [uVenture GitHub Milestone M2](https://github.com/uventure/uventure/milestone/2):

<img class="ui centered image" src="../images/m2-issues.PNG">

Milestone 2 consisted of seven issues, and progress was managed via the [uVenture GitHub Project M2](https://github.com/uventure/uventure/projects/2):

<img class="ui centered image" src="../images/m2-project.PNG">

Each issue was implemented in its own branch, and merged into master when completed.

<img class="ui centered image" src="../images/m2-network.PNG">

## Milestone 3: Test and polish 
M3: From April 27, 2017 to May 2, 2017

The goal of Milestone 3 is to fully implement user functionality and conduct a user test. 

The ProfileCollection, AdventureCollection, and InterestCollection will respond to the actions of the user and store the relevant data.

Some notable additions in this milestone are the Suggested Adventures page and UH Calendar page.


<img class="ui centered image" src="../images/suggestion.png">
The Suggested Adventures page helps both users and non-users find some Yelp-approved adventures in Hawaii. 

<img class="ui centered image" src="../images/calendar.png">
The UH Calendar page helps UH Manoa students plan out their next adventure and ensures that their adventure doesn't fall within an important event like Finals Week or Commencement.

We also implemented an AdventureSeed which will populate three adventures if there are no adventures in the database. 

Milestone 3 was implemented as [uVenture GitHub Milestone M3](https://github.com/uventure/uventure/milestone/3):

<img class="ui centered image" src="../images/m3-issues.PNG">

Milestone 3 consists of eight issues, and progress was managed via the [uVenture GitHub Project M3](https://github.com/uventure/uventure/projects/3):

<img class="ui centered image" src="../images/m3-todo.PNG">

## Initial User Study
Conducted from May 8, 2017 to May 9, 2017

User feedback results:

<img width="200px" src="../images/surveyg1.jpg"/>
<img width="200px" src="../images/surveyg2.jpg"/>
<img width="200px" src="../images/surveyg3.jpg"/>
<img width="200px" src="../images/surveyg4.jpg"/>
<img width="200px" src="../images/surveyg5.jpg"/>
<img width="200px" src="../images/surveyg6.jpg"/>
<img width="200px" src="../images/surveyg7.jpg"/>
<img width="200px" src="../images/surveyg8.jpg"/>
<img width="200px" src="../images/surveyg9.jpg"/>

<p>	Five undergraduate students were recruited for the study. Our group chose to survey students who were not in the ICS program so they are unfamiliar with the project and the its requirements. Questions from the survey were designed around each individual page of the site to better isolate the part of the site which needs improvement. This also helps keep suggestions clear as to which part needs to be improve upon. We wanted to give the testers a site that made it simple to add adventures and to be able to view the adventures they added as well. The site needed to be lively and captivating to inspire users to build experiences for the UH community. Having this goal in mind we asked questions such as “Was it easy to add an adventure”, “Was the site easy to navigate”, and “How visually appealing was the site?”. These questions and its responses would help give the feedback necessary to better improve upon our goals for the site. Following all the responses, it seemed that most users liked the design of the website but one also felt skeptical about the site being able to gather the UH community together and create adventures for everyone. Some other responses included fixing a link that routed to the wrong adventure and there was a suggestion of possibility adding more information for our adventures. All responses were reviewed and put into consideration for any feature development that may happen with the site.</p>

Responses can be viewed at: <a href="https://goo.gl/eWscou">https://goo.gl/eWscou</a> 

