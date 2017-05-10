# Table of contents

* [About uVenture](#about-uventure)
* [Deployment](#deployment)
* [Installation](#installation)
* [Development history](#development-history)
  * [Milestone 1: Mockup development](#milestone-1-mockup-development)
  * [Milestone 2: Data model development](#milestone-2-data-model-development)
  * [Milestone 3: Test and polish](#milestone-3-test-and-polish)
  * [Initial User Study](#initial-user-study)
  * [Future Plans](#future-plans)



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

The central idea around uVenture is that using the Google Maps API will give users a nice and intuitive UI so that they can easily add an adventure just by placing a point on the map. 

Once that point is placed, a form will appear allowing the user to set-up their own adventure (hike, sightseeing, etc.). 
<img class="ui centered image" src="../images/add.png">

With the Google Maps API, users will also be able to scope out or have a general view of the area their adventure will be held at by using dragging the "Yellow Man" icon on a potential location for an adventure.

In addition, the user that made the adventure can edit it by selecting it on the Find Adventures page. 
<img class="ui centered image" src="../images/edit.png">

## Finding an adventure
uVenture also provides a find adventure page. The option to join the adventure will only be available to those who can login to the system with their UH account.
<img class="ui centered image" src="../images/find.png">

The idea behind this page is to allow users to see what adventures are out there based on the map UI. This page also has a table of all the active adventures ordered by the newest adventure there is out there.

## Miscellaneous

Some other notable pages in uVenture is the Suggested Adventures page and UH Calendar page.

<img class="ui centered image" src="../images/suggestion.png">
The Suggested Adventures page helps both users and non-users find some Yelp-approved adventures in Hawaii. 

<img class="ui centered image" src="../images/calendar.png">
The UH Calendar page helps UH Manoa students plan out their next adventure and ensures that their adventure doesn't fall within an important event like Finals Week or Commencement.

<img class="ui centered image" src="../images/find.png">
An AdventureSeed also populates three adventures if there are no adventures in the database.

# Deployment

[uVenture](http://uventure.meteorapp.com/) is currently deployed using Galaxy, a platform-as-a-service (PaaS) for Meteor applications. You can find the latest deployment on: http://uventure.meteorapp.com/

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

The goal of Milestone 3 is to fully implement some user functionality and conduct a user test. 

The ProfileCollection, AdventureCollection, and InterestCollection will respond to the actions of the user and store the relevant data. An AdventureSeed was added to populate some adventure ideas if there are not any available in the database.

Some notable additions in this milestone are the Suggested Adventures page and UH Calendar page.

**Suggested Adventures Page**

<img class="ui centered image" src="../images/suggestion.png">

**Calendar Page**
<img class="ui centered image" src="../images/calendar.png">

In addition, a Calendar Page was also made to assist users in planning an adventure by displaying special holidays and dates pertaining to the UH system. 

The Suggestion page was also made to help both users and non-users of uVenture to make an adventure based on some popular Hawaii tourist activities that are Yelp-reviewed. 

Milestone 3 was implemented as [uVenture GitHub Milestone M3](https://github.com/uventure/uventure/milestone/3):

<img class="ui centered image" src="../images/m3-issues.PNG">

Milestone 3 consists of eight issues, and progress was managed via the [uVenture GitHub Project M3](https://github.com/uventure/uventure/projects/3):

<img class="ui centered image" src="../images/m3-todo.PNG">

## Initial User Study
Conducted from May 8, 2017 to May 9, 2017

Five undergraduate students were recruited for the study. Our group chose to survey students who were not in the ICS program so they are unfamiliar with the project and the its requirements. Questions from the survey were designed around each individual page of the site to better isolate the part of the site which needs improvement. This also helps keep suggestions clear as to which part needs to be improve upon. 

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

We wanted to give the testers a site that made it simple to add adventures and to be able to view the adventures they added as well. The site needed to be lively and captivating to inspire users to build experiences for the UH community. Having this goal in mind we asked questions such as “Was it easy to add an adventure”, “Was the site easy to navigate”, and “How visually appealing was the site?”. 

These questions and its responses would help give the feedback necessary to better improve upon our goals for the site. Following all the responses, it seemed that most users liked the design of the website but one also felt skeptical about the site being able to gather the UH community together and create adventures for everyone. 

Some other responses included fixing a link that routed to the wrong adventure and there was a suggestion of possibility adding more information for our adventures. All responses were reviewed and put into consideration for any feature development that may happen with the site.

The survey responses can be viewed at: <a href="https://goo.gl/IEkrZ6">https://goo.gl/IEkrZ6</a> 

## Future Plans
After a through review of the the survey results from the Initial User Study, we plan to further enhance the uVenture experience for UH Manoa students in the near future. 

<img class="ui centered image" src="../images/add.png">
The Add Adventure form currently has a horizontal structure which can be a hassle to move back and forth from the form to the Google Map when filling out an Adventure. One change that could be implemented is to move the Google Map to the right side of the form so that the users can both fill the form and navigate around the Google Map at the same time-- much like [Airbnb's](https://www.airbnb.com/) housing search dashboard. 

<img class="ui centered image" src="../images/find.png">
The Find Adventure page currently has no Google Maps view which can make it hard for some users to find where the exactly location of an adventure is before they can commit to it. Sure they can just contact the person or organization in charge of the adventure and ask them where it is, but it would be much easier if they can find where the adventure exactly is all in one page. 

With these plans in mind, a future addition to uVenture would allow this application to be more easy to use and more intuitive to address user concerns. 

We understand that nothing is perfect. The initial user study showed us that there is room to improve before making the ultimate adventure planning experience. 

*Our adventure is helping you plan your ultimate adventure.*
