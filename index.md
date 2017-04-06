# Table of contents

* [About uVenture](#about-uventure)
* [uVenture Mockup](#mockup)
* [Installation](#installation)
* [Development history](#development-history)
  * [Milestone 1: Mockup development](#milestone-1-mockup-development)


# About uVenture

uVenture is a Meteor application to plan adventures for the University of Hawaii community. When you come to the site, you are greeted by the following landing page:

<img class="ui centered image" src="../images/home.png">

Anyone with a UH account can login to uVenture by clicking on the login button. The UH CAS authentication screen then appears and requests your UH account and password.
 
Once authenticated, you can create a profile that provides a bio statement and list of interests, plus links to Facebook and Instagram.

This application plans to make use of the Google Map API or Leaflet or whichever Map API we plan to use once we find out that it's stable. 
<img class="ui centered image" src="../images/g.png">

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

# Development History (WORK IN PROGRESS FOR M1 TO M5)

The development process for BowFolios conformed to [Issue Driven Project Management](http://courses.ics.hawaii.edu/ics314f16/modules/project-management/) practices. In a nutshell, development consists of a sequence of Milestones. Milestones consist of issues corresponding to 2-3 day tasks. GitHub projects are used to manage the processing of tasks during a milestone.  

The following sections document the development history of BowFolios.

## Milestone 1: Mockup development

This milestone started on December 6, 2016 and ended on January 31, 2017.

The goal of Milestone 1 was to create a set of HTML pages providing a mockup of the pages in the system. To simplify things, the mockup was developed as a Meteor app. This meant that each page was a template and that FlowRouter was used to implement routing to the pages. 

Mockups for the following four pages were implemented during M1:

Milestone 1 was implemented as [BowFolio GitHub Milestone M1](https://github.com/bowfolios/bowfolios/milestone/1)::

Milestone 1 consisted of five issues, and progress was managed via the [BowFolio GitHub Project M1](https://github.com/bowfolios/bowfolios/projects/1):

Each issue was implemented in its own branch, and merged into master when completed:

## Milestone 2: Data model development 

This milestone started on Jan 31, 2017 and ended on Feb 2, 2017.

The goal of Milestone 2 was to implement the data model: the underlying set of Mongo Collections and the operations upon them that would support the BowFolio application.  We implemented the data model as a set of Javascript classes. The BaseCollection class provides common fields and operations. The ProfileCollection and InterestCollection classes inherit from BaseCollection and provide the persistent data structures useful for BowFolios. 
 
Also in this milestone, we implemented a set of mocha tests for the data model classes. These tests make sure we can create, manipulate, and delete the data model documents successfully.  These tests are documented above.

Milestone 2 was implemented as [BowFolio GitHub Milestone M2](https://github.com/bowfolios/bowfolios/milestone/2)::

Milestone 2 consisted of two issues, and progress was managed via the [BowFolio GitHub Project M2](https://github.com/bowfolios/bowfolios/projects/2):

Each issue was implemented in its own branch, and merged into master when completed:

## Milestone 3: Connect UI to data model

This milestone started on Feb 2, 2017 and ended on Feb 10, 2017.

The goal of Milestone 3 was to connect the user interface to the underlying data model. This meant that we updated the templates for each page with calls to helper functions, and we created Javascript files for the templates with helper functions. We used the form control templates from [meteor-example-form](https://ics-software-engineering.github.io/meteor-example-form/) to simplify implementation of form processing.

Milestone 3 was implemented as [BowFolio GitHub Milestone M3](https://github.com/bowfolios/bowfolios/milestone/3)::

Milestone 3 consisted of four issues, and progress was managed via the [BowFolio GitHub Project M3](https://github.com/bowfolios/bowfolios/projects/3):

Each issue was implemented in its own branch, and merged into master when completed:

## Milestone 4: Authentication

This milestone started on Feb 10, 2017 and ended on Feb 14, 2017.

The goal of Milestone 4 was to set up authentication using the University of Hawaii test CAS system. We used the templates from [meteor-example-uh-cas](http://ics-software-engineering.github.io/meteor-example-uh-cas/) to guide the implementation. Although the example restricts logins to those in a list in the configuration file, BowFolios allows anyone with a UH account to access the system. 

Authentication also implies that users cannot access the profile or filter page associated with another user.

Milestone 4 was implemented as [BowFolio GitHub Milestone M4](https://github.com/bowfolios/bowfolios/milestone/4)::

Milestone 4 consisted of two issues, and progress was managed via the [BowFolio GitHub Project M4](https://github.com/bowfolios/bowfolios/projects/4):

Each issue was implemented in its own branch, and merged into master when completed:

## Milestone 5: Administration

This milestone started on Feb 14, 2017 and is ongoing.

[BowFolio GitHub Milestone 5](https://github.com/bowfolios/bowfolios/milestone/5) involves the creation of an administrator role in the system. The administrator can manage the set of defined interests. (Currently, interests are defined in the database file loaded at system startup time.)

This milestone will also include the implementation of Meteor methods and removal of the insecure package. 

We will manage progress on this milestone using [BowFolio GitHub Project M5](https://github.com/bowfolios/bowfolios/projects/5).
