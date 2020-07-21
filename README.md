# Maintenance Ticket Software
## How to use
1. Ensure [Node.js](https://nodejs.org) is installed (node and npm)
1. Clone the repository
    ```bash
    $ git clone https://github.com/AustenBaker/Maintenance-Ticket-Software.git
    ```
1. Navigate to `project/server` directory, create a file named `settings.json`. Or from project root: 
    ```bash
    $ touch ./project/server/settings.json
    ```
   Edit this `settings.json` file to add the following:
    ```json
    {
        "PORT": 3001,
        "secure": false
    }
    ```
1. Install all dependencies
    ```bash
    $ cd ./project
    $ npm i

    ### If you are using windows, also execute the following commands to ensure client dependencies are installed (required for some windows machines) ###
    $ cd client
    $ npm i
    ```
1. Open two terminal windows. In the first window, run:
    ```bash
    $ cd ./project
    $ npm run server  # This runs the backend server, listening to file changes
    ```
    In the second window, run:
    ```bash
    $ cd ./project/client
    $ npm start  # This runs the frontend client (in the browser) listening to changes. Can run the app on mobile devices or run directly in the browser
    ```
    Client app should open in your default browser. You can run the app there directly
1. If running on a mobile device, navigate to `./project/client/fetch`. Open the two files contained in the folder. On the first line for each file, substitute the following:
    ```js
    const PATH = 'http://<LAN_Address_Of_Your_Machine>:3001';  // http://192.168.1.100:3000, for example
    ```
    This ensures proper client/server communication. If simulating locally in a browser, skip this step.

## Running test suites and code coverage
1. Navigate to `./project/client`. Run:
    ```bash
    $ npm run test
    ```
