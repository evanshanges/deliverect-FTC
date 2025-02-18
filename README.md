# Interview Challenge for Frontend Developers

## Overview

Create a simplified wizard that goes through some basic account registration steps.

The wizard steps should be structured/organized in a way to collect the necessary information but maintain a good user experience.

<img width="569" alt="image" src="https://github.com/ksooley/frontend-technical-challenge/assets/102975243/b5d7e3b5-3401-48ed-9401-3cdb3981c2cd">



## Requirements

- Account Information to collect:
    - First and Last Name
    - Email
    - Business Name
    - Business Size (integer)
    - Business Type (choose from list)
        - SMB
        - Midmarket
        - Enterprise
    - Point of Sale used by business (choose from list)
        - Use `/pos` route (See info under Server section below)
        - Note the payload in this route is an example but assume there can be more than 200
    - Delivery Channel used by business (choose from list)
        - Use `/channel` route (See info under Server section below)
        - Note the payload in this route is an example but assume there can be more than 200
- Must save the state of the registration in localstorage so you can pick up where you left off
- Once the information is collected, save the information using api call
    - Use `/account` route (See info under Server section below)
    - Note payload can be any structure, and it will be saved in disk as a json file with the current timestamp
        - `account_{timestamp}.json` file

## Setup

#### NPM
- Version used for repo:
    - `9.2.0`

#### Node
- Version used for repo:
    - `19.3.0`

#### Express
- Version used for repo:
    - `4.18.2`
- Run command:
    - `npm install`

#### Server
- Run command:
    - `npm run server`
    - Call `localhost:5000`
- Available routes
    - GET - `/pos`
        - Returns a list of point of sales with properties:
            - `id`
            - `name`
            - `imageUrl`
    - GET - `/channel`
        - Returns a list of delivery channels with properties:
            - `id`
            - `name`
            - `imageUrl`
    - POST - `/account`
        - Accepts any json payload


## Next Steps
Update package.json's `client` command such that your frontend showcasing the wizard can be ran using command: `npm run client`. Ensure that it is running in port `5001`. The server is running at `localhost:5000`.

You are free to write your code using any JS frameworks, and libraries. But please reuse the existing `package.json`.

Please ensure that you have some documentation left in this README.md about your work.


# Documentation

Here is some documentation regarding how to run the code and some of my decision making while completing this challenge

## Installing dependencies

To install both Server and Client dependencies I created a script to install both with one command insteading of navigating in and out of the client directory.
```
npm run installAll
```

## Running the code

### Server (port: 5000): 
```
npm run server
```

### Client (port: 5001):
```
npm run client
```