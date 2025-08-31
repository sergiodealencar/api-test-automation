# Trello API Testing with Postman & Newman

This project demonstrates how to automate API testing for the **Trello API** using a **Postman collection** executed via **Newman**, making it suitable for CI/CD pipelines such as Jenkins.

## Overview

- **Tools used:**
  - [Postman](https://www.postman.com/) – for API request creation and testing
  - [Newman](https://www.npmjs.com/package/newman) – CLI runner for Postman collections
  - [Node.js](https://nodejs.org/) – required to install Newman
  - (Optional) [Jenkins](https://www.jenkins.io/) – for CI/CD automation
  - (Optional) [Docker](https://www.docker.com/) – to containerize the CI/CD environment

- **Tested API:** Trello REST API  
  - Creates a board
  - Creates TODO and DONE lists
  - Creates and moves a card
  - Deletes the board and verifies deletion

## How to Run Locally

1. **Clone this repository:**
   ```bash
   git clone https://github.com/your-username/trello-api-newman.git
   cd trello-api-newman
