# TodoMVC Test Plan

## Overview

[TodoMVC](https://todomvc.com/) is a website which collates examples of the same "To-Do List" 
application implemented in 64 different JavaScript frameworks, for 
developers to use as examples when evaluating what framework they would like to 
use for their own application development.The simple to-do list application doesn't have any persistent storage; it 
stores its data in the user's local storage.

## Objective

This test plan intends to outline the testing which ensures the ToDoMVC website carries out the below specified functional requirements.


## Scope of Testing

We are testing functional requirements across 3 frameworks since these are the most popular frameworks according to the product owner.
* React
* Angular
* Vue.js 

### Functional scope

We will only be testing the following functionality;
1. Adding todo cards
2. Modifying a ToDo item
3. Deletion of a ToDo item
4. Toggle completion status of all ToDo items

## Test Environments

Tests will be performed using:

* Chromium engine 109
* Minimum network speed 20mbps
* Mac OS Ventura 13.1
* Automated testing performed with Playwright 1.28
* IntelliJ CE 2022.3.1
* JUnit 5.8.1

## Features To Be Tested

For each of the popular frameworks, we want to verify the following features:

1. Adding a new ToDo item
    * Can't add an item with an empty value
    * Can add a value with a single character
    * Check that every single accented character and symbol is supported
    * Check that every single emoji character is supported
2. Modifying a ToDo item
    * Double clicking an item enables editing of ToDo item
    * If you click Escape during edit, it should cancel the modification
    * A ToDo item can be ticked-off (it will appear with a line through it)
    * A completed ToDo item can be unticked again
    * A ToDo item can be reordered by dragging it up or down in the list
3. Deletion of a ToDo item
    * Delete an incomplete ToDo item
    * Delete a completed ToDo item
4. Toggle completion status of all ToDo items
    * Clicking the down arrow symbol next to the "What needs to be done?" box will 
toggle all items to Completed or Not Completed

## Test Team

We have 3 testers available for this project in our test team.
The testers assigned to this project are:
* `A.Adams` - Test Team Lead, the most experienced member of the team.
* `B.Barker` - Test Engineer who's been the primary tester on TodoMVC for the 
entire project.
* `C.Chapel` - Test Engineer who joined the company last week and is primarily 
still completing onboarding.

## Test Estimation

As a team, we have estimated how long it will take to complete a test of the 
"Features To Be Tested" for a single variant, in a single browser (e.g. just 
the React version, in Chrome). The team conservatively estimates that it will 
take around *6 hours* to complete a single such cycle. This includes the time 
required to investigate/log any defects which are encountered along the way.

Therefore we can extrapolate an approximate amount of time to execute the 
entire set of tests:

* 3 different variants listed on the TodoMVC homepage
* = 3 combinations, taking 18 hours to execute

Dividing this effort between the 3 testers that we have available, we therefore 
estimate that it will take us 18 working hours to complete this testing.

## Defect Management

When a tester encounters a bug, they will raise a defect on the GitHub Issues 
page for the project. The tester should assign one of the following priorities: 

* **1 - High:** Requires immediate attention
* **2 - Medium:** Must be addressed pre-deployment
* **3 - Low:** Can be addressed post-deployment

The list of defects will be reviewed on submission by the Development Team.

Product Owner will receive a daily update of outstanding and resolved number of defects.


## Entry Criteria

Testing will commence when:

* The testing team have been notified of the testing requirements and have access to the testing environment.

## Exit Criteria

The test plan has passed when all 3 frameworks have been tested according to the functional testing scope and any high and medium priority bugs have been addressed.

## Risks

The following table outlines all of the risks associated with this test plan, 
and how we intend to mitigate them:

| Risk | Mitigation | Priority |
| ---- | ---------- | -------- |
| Recent intermittent internet access in our office. | Allow testers to work from remote/home as needed. | Low |
| We might find more bugs than the developers have time to fix. | Follow the defect prioritisation and management policy | Medium |
| We've not tested to see how well the site performs with multiple users. | Arrange for some performance testing to happen after launch. | Medium |
| Compatability issues since entire testing env is using Mac and only testing Chrommium browsers | Schedule testing for other OS and browsers as more testers become available | Low |

## Test plan revision history

Here you will find a history of previous revisions of this test plan, with 
the name of the tester who authored the revision.

| Version | Author | Date |
| ------- | ------ | ---- |
| 1.0 (This version) | A.S.D | 16/01/2023 |
| 0.9 | T.Tester | 10/12/2022 |
| 0.8 | T.Tester | 10/10/2022 |