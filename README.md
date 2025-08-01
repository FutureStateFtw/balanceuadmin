<div style="display: flex; align-items: center;">
  <img src="https://apps.ufs.arizona.edu/buildingmanager/assets/BlockA_w_line-290716d5.png" alt="Block A" style="margin-right: 10px;"/>
  <h1 style="margin: 0;">BalanceU Admin</h1>
</div>

BalanceU Admin 

## Table of Contents

- [Features](#features)
- [Requirements](#requirements)
- [Getting Started](#getting-started)
  - [Installation](#installation)
  - [Running the Application](#running-the-application)
- [Project Structure](#project-structure)
- [Available Scripts](#available-scripts)


## Features

- Vue.js framework
- Basic project structure and components
- Pinia for state management
- Vue Router for client-side routing
- UofA Branding, Styling
- Webauth authentication
- API calls to get employee Profile information
- Employee Search
- Building Search
- Other example components

## Requirements

Ensure you have the following installed on your development environment:

- [Node.js](https://nodejs.org/) (version 18.x or later)
- [npm](https://www.npmjs.com/) (version 6.x or later)

## Getting Started

### Installation

1. Clone the repository:

    ```git clone https://KyloDren74@bitbucket.org/kylo_dren/balanceuadmin.git
    ```

2. Navigate to the project directory:

    ```cd BalanceUAdmin
    ```

3. Install the dependencies:

    ```npm install
    ```

### Running the Application

To start the application in development mode, run the following command:
```npm run dev```

## Project Structure

Here's a quick overview of the project's structure:

```plaintext
BalanceUAdmin/
├── public/             # Static files
│   └── index.html      # Main HTML file
├── src/
│   ├── assets/         # Asset files
│   ├── components/     # Vue.js components
│   ├── router/         # Vue Router setup
│   ├── store/          # Pinia store setup
│   ├── views/          # View components
│   ├── App.vue         # Main app component
│   └── main.js         # Entry point
├── package.json        # Project metadata and dependencies
└── README.md           # Project documentation
```

## Available Scripts

Below are the scripts available for this project:

- **`npm run dev`**: Launches the development server with hot-reloading.
- **`npm run build`**: Builds the application for production.

### Script Details

- **`npm run dev`**
    - Launches the development server with hot-reloading, allowing you to see changes in real-time. The application will be available at [http://localhost:3000](http://localhost:3000) by default.

- **`npm run build`**
    - Builds the application for production. The output files will be located in the `dist` folder and optimized for performance.

- **`npm deploy:beta || deploy:prod`**
    - Robocopys the build files to the destination.  This requires editing to remove the underscore and replace 'balanceuadmin' with correct path.
 
- **`npm build:deploy:beta || build:deploy:prod`**
    - Combines the build and deploy in one step.  This requires editing to remove the underscore and replace 'balanceuadmin' with correct path.
     
## Roles and Permissions
- JWT is generated in common API
- Roles are store in the "Cerberus" system
- An app-id in .env will match up to the Cerberus roles encoded into token

## Store Design
- store/app.js  - main store for this apps logic and state
- store/api.js  - holds all external apis, no business logic
- store/user.js - related to this users role, token, login
- store/ui.js   - holds state for all ui, show/hide, loading, etc.

## Starting a new app from BalanceU Admin

- Clone
- Install Node, npm install, npm run dev.  Make sure it runs
- Do global search on 'BalanceU Admin', and address each instance.
- Start new EMPTY repository on remote, no readme, no .gitignore.
- Copy remote address
- Edit local app's remote address with new remote address
- Push
