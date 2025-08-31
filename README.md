# Trello API Testing with Postman & Newman

This project demonstrates how to automate API testing for the **Trello API** using a **Postman collection** executed via **Newman**, making it suitable for CI/CD pipelines such as Jenkins.

## Overview

- **Tools used:**
  - [Postman](https://www.postman.com/) – for API request creation and testing
  - [Newman](https://www.npmjs.com/package/newman) – CLI runner for Postman collections
  - [Node.js](https://nodejs.org/) – required to install Newman
  - [Jenkins](https://www.jenkins.io/) – for CI/CD automation
  - [Docker](https://www.docker.com/) – to containerize the CI/CD environment

- **Tested API:** [Trello REST API  ](https://developer.atlassian.com/cloud/trello/rest/api-group-actions/#api-group-actions)
  - Creates a board
  - Creates TODO and DONE lists
  - Creates and moves a card
  - Deletes the board and verifies deletion

## Repository Structure
```bash
trello-api-newman/
│
├── README.md                          # Project documentation
├── Trello_API.postman_collection.json # Trello Postman collection 
├── reports/                           # Folder for Newman HTML reports
│   └── newman-report.html
└──  screenshots/                       # Screenshots
     ├── newman-run-dashboard.png
     └── newman-output.png

```

## How to Run Locally

1. **Clone this repository:**
   ```bash
   git clone https://github.com/sergiodealencar/api-test-automation.git
   cd api-test-automation

2. **Install Newman globally:**
   ```bash
   npm install -g newman

3. **Run the Postman collection provided:**
   ```bash
   newman run Trello_API.postman_collection.json

4. **(Optional) Generate an HTML report:**
   ```bash
   newman run Trello_API.postman_collection.json -r cli,html

## Environment Variables

The collection uses the following variables (already included in the JSON file):

*  baseUrl – API base URL
*  trelloKey – Trello API key
*  trelloToken – Trello API token
*  boardId, todoListId, doneListId, cardId – dynamically set during tests

## Screenshots

* [Newman CLI Output](https://github.com/sergiodealencar/api-test-automation/blob/main/screenshots/newman-output.png)
* [Newman Report](https://github.com/sergiodealencar/api-test-automation/blob/main/screenshots/newman-run-dashboard.png)
