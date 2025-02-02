
## What is Cypress?
Cypress is a JavaScript End to End testing framework

## Installing all the dependencies

    npm install

## Opening Cypress Test Runner and running tests individually inside the Cypress TestRunner

     npm run cy:open

     select individual scenario to run and see the outcome inside the TestRunner

## Running Tests all in headless browser in terminal or command line

     npm run cy:run 

## Running individual test in headless browser

   npm run cy:run --spec "cypress/integration/scenarioAC_1.spec.ts"


## Running tests in a browser (e.g. chrome or in firefox browser)

   npm run cy:run --spec "cypress/integration/scenarioAC_1.spec.ts" -b chrome

   npm run cy:run --spec "cypress/integration/scenarioAC_1.spec.ts" -b firefox


## NOTE:
- Test cases are clean and easy to use and maintain from the QA and the developers point of view
- Need to prioritse the tasks in future to maintain the test suites stable and easy to maintain for the regresion tests and running the tests in the pipelines for the continuous develivery of the product

- I have setup the structure of the tests in the following manner:
  -   Easy to use
  -   Easy to maintain
  -   There's a proper 'before hook' used to setup the login step
  -   Easily defined the 'Actions' within the steps
  -   There are verifications steps to verify each action performed 
  -   Perform vaidation of the elements to be present/visible
  -   There are no sleeps/waits used in any scenrio or feature to improve the stability of the tests
  -   All the tests/scenarios are independent of each other and can run them separately or all in one go too
  -   I have used the 'Page Objects' which helps in maintain and fixing the elements if in future any of the elements css has changed (can navigate to the following elmenent and  
         change the css/id or the name of the element and that will update for all the rest of the steps where it is used) 
  -   I have used the a basePage for the baseURL and the viewports if in future the tests needs to be run on any particualr device such macbook Pro 16, iPhone11 or Android phone etc.
  -   I have used Typescript with Cypress


  ## Browser Support

 -   Cypress has the capability to run tests across multiple browsers. Currently, Cypress has support for Chrome-family browsers (including Electron and Chromium-based Microsoft Edge), and Firefox 

  # Command to run the tests in Edge browser
 -  npm run cy:run --browser edge (To run all the tests in edge browser)

 -  npm run cy:run --spec "cypress/integration/scenarioAC_1.spec.ts" --browser edge (to run an individual test in edge 
    browser)
    
    But first, download the plugin for Edge browser by visiting "https://www.microsoftedgeinsider.com/en-us/download/" or "https://www.microsoft.com/en-us/edge" 
    
    Cypress automatically detects available browsers on a user’s OS. Now go to the browser in the Test Runner by using the drop-down in the top right corner 

   ##    Cypress supports list of browsers:
 -  Chrome
 -  Chrome Beta
 -  Chrome Canary
 -  Chromium
 -  Edge
 -  Edge Beta
 -  Edge Canary
 -  Edge Dev
 -  Electron
 -  Firefox
 -  Firefox Developer Edition
 -  Firefox Nightly 
