# Project WebRM

Project WebRM (Web Remanage) is an attempt to give users control over the way information is presented to them.

## Overview

WebRM will enable the user to be able to personalise webpages to their preferences (styling as well as the contents of the information presented). WebRM aims to achieve this by utilising similar techiques to MitB (Man in the Browser) attacks to modify the content of webpages (client-side).

## Discussion

possible processes:
 - If website is marked as edited redirect any attempts to visit the page to another page that is webscraping the data from the orginal site
 - Webextension that activates when a site that has be marked edited is loaded and replaces the entire website data

P).
    Needs to be performant efficient as some peoples internet speed may not be able to handle heaving page renders.
S).
    Island architecture utilising partial hydration to ensure only components that need to be shipped with javascript get reloaded and not static components.
P).
    All frameworks supporting island architecture are designed for websites that have multiple pages, for this only a single page needs to be accounted for. (bloat)
S).
    Design a frontend mirco-framework that is tuned specifically for webrm (performance efficient)
P).
    Having web data sent from the web server to the user's browser and then to the webrm server and back again may result with slow page load times if the user in limited in terms of bandwidth. (privacy cncerns as well)
S).
    Have everything rendered on the user's side, potential for having enabling on site SSR (user's own server) or an opt in usage of a webrm server.

## Road Map

### Phases
Phase 1:
    develop frontend micro framework

Phase 2:
    develop a tool that is able to convert website data into a format that is readable to the frontend micro framework

Phase 3:
    Develop a tool that is able to conbine the previous two phases into a web extension that is supported on atleast safari and chrome

### Phase 1
development of PRIRE (Partially Reactive Island Rendering Engine)

Required features:
 - island architecture
 - partial hydration
 - component based
 - virtual DOM with shadow DOM integration

### Phase 2

#### Currently there are three options:
1. Use an extension framework

|Pros|Cons|
|:-|:-|
|Convenient|No control on when updates get pushed meaning vulnerabilities may be prevalent|
|Decreased development time?|If such framework stops being maintained the could be detimental to WebRM|
||If a browser has a breaking change we'd ave to wait for the framework to account for such changes (if they even attempt to do so)|

2. Create our own extension framework

|Pros|Cons|
|:-|:-|
|More performant efficient|Takes time to make a framework from the group up|
|Able to fix vulnerabilities as soon as possible|Needing to maintain the framework|
|We'd have control on the maintenance of the framework|Whenever a supported browser has a breaking change we may have to be made to the framework|

3. Directly inject code into the browser

|Pros|Cons|
|:-|:-|
||Breaking changes to browsers|
||Takes a lot of developing time|
||May get caugth by antivirus|
