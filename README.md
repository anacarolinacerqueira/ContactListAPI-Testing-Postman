## :desktop_computer: Contact List API - Testing Project using Postman and Newman

<p align="center">
  <img alt="GitHub powered by" src="https://img.shields.io/badge/API%20Tests-Postman-orange">
  <!--- <img alt="GitHub language count" src="https://img.shields.io/github/languages/count/anacarolinacerqueira/ContactListAPI-Testing-Postman">
  <img alt="GitHub top language" src="https://img.shields.io/github/languages/top/anacarolinacerqueira/ContactListAPI-Testing-Postman"> --->
  <img alt="GitHub last commit" src="https://img.shields.io/github/last-commit/anacarolinacerqueira/ContactListAPI-Testing-Postman">
</p>
<p align = "center">
<img alt="GitHub test status" src="https://github.com/anacarolinacerqueira/ContactListAPI-Testing-Postman/actions/workflows/github-actions-newman-htmlextraReport.yaml/badge.svg?branch=main">
</p>
  This repo is destined to store a set of API testing, using postman test scripts and Newman with html-extra template to report the test execution results. The flow is set in continuous integration (CI) pipeline with Github Actions. For each update, the routine runs, and a report is generated at the "Actions" tab.

### :spiral_notepad: About the service under Test

The [Contact List API](https://documenter.getpostman.com/view/4012288/TzK2bEa8) is a service provide as example in the book ["The Complete Software Tester"](https://www.amazon.com/Complete-Software-Tester-Strategies-High-Quality-ebook/dp/B09NGVVCJ9) by Kristin Jackvony, that i'm currently reading. To this service is available some HTTP methods to manipulate users and contacts. To practice, I planned and executed tests exploring the scenarios (successfullies and failures) involving the contacts endpoint. For each request, a different situation is tested and automatically validated using the postaman library (JavaScript based).

## :arrow_forward: How to run this project

### :pushpin: Getting the last execution report

- Click on "Actions" tab in this repo; <br> 
- Click on the last workflow run; <br>
- In the page bottom, you can verify the "Artifacts" session; <br>

![Gif tutorial to access the actions tab at this repo](/assets/continuous%20integration%20-%20github%20actions.gif)

- Download the html report file, and open it in your favorite browswer to verify the test results.<br>

![Report example with htmlextra](/assets/test%20execution%20report.gif) <br>

### :next_track_button: Running tests on GitHub Actions

- Access the "Actions" tab;
- Select the last run workflow;
- Click in "Re-run all jobs".

### :floppy_disk: Running tests locally

- Install [postman](https://learning.postman.com/docs/getting-started/installation-and-updates/); <br>
- Download the collection and environment files in the directory `/files`, and import it in postaman;
- Run the collection to verify the test results.

![Postman runner example](/assets/postman-running.gif)

or, to generate a html-extra report, aditionally: 

- Install [npm](https://docs.npmjs.com/downloading-and-installing-node-js-and-npm); <br>
- Instal [newman](https://www.npmjs.com/package/newman) library; <br>
- Install ["htmlextra" template reporter](https://www.npmjs.com/package/newman-reporter-htmlextra); <br>
- Run on terminal:

```
newman run files/Contact-List.postman_collection.json -e files/Contact-list.postman_environment.json -r htmlextra
```
---
Author: [Ana Carolina Cerqueira](https://www.linkedin.com/in/anacarolinacerqueira/) :v:
