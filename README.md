# static-web-service-template
A simple web server written using node.js and expressjs framework to host static content in pure html/css/javascript

# Dependencies
    sudo apt-get update
    sudo apt-get install nodejs    // npm should be installed automatically
    sudo apt-get inslall npm       // if it isn't installed

# Start new project
    npm init -y                    // creates package.json file
    npm install express --save     // installs express framework locally
    npm install nodemon            // handy tool to automatically restart server

    modify package.json file like so:

        "scripts": {
          "start": "node server.js",
          "dev": "nodemon server.js"
        },

    npm run start                  // starts server in production mode
    npm run dev                    // starts server in debug mode

# Server side code

    // Import packages
    const express = require('express');
    const path = require('path');

    // create app instance
    const app = express();

    // Set static folder
    app.use(express.static(path.join(__dirname, 'public')));

    // Set port variable
    const PORT = process.env.PORT || 5000;
    app.listen(PORT, () => console.log(`Server started on port ${PORT}`));

# YouTube tutorial
[![IMAGE ALT TEXT HERE](https://img.youtube.com/vi/uK36MuzpKkE/0.jpg)](https://youtu.be/uK36MuzpKkE)
