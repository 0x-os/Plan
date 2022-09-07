# Project WebRM

Project WebRM (Web Remanage) is an attempt to give users control over the way information is presented to them.

## Overview

WebRM will enable the user to be able to personalise webpages to their preferences (styling as well as the contents of the information presented). WebRM aims to achieve this by utilising similar techiques to MitB (Man in the Browser) attacks to modify the content of webpages (client-side).

## Road Map

### Phases
Phase 1:
    develop frontend micro framework

Phase 2:
    develop a tool that is able to convert website data into a format that is readable to the frontend micro framework

Phase 3:
    Develop a tool that is able to conbine the previous two phases into a web extension that is supported on atleast safari and chrome

### Phase 1
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

- [ ] Plasmo
- [ ] Next js
- [ ] Astro
- [ ] Scraping Library
    - [ ] JSoup
    - [ ] Selenium
    - [ ] BeautifulSoup

