# Contact Manager

## Features to implement

- List Contacts
- View Contact
- Add Contact
- Delete Contact
- Edit Contact
- Clean routing i.e '/contact/:id'
- Use material-ui for components

### Bonuses

- Use [xstate](https://xstate.js.org/docs) to manage app state.
- Connect to the graphql endpoint http://localhost:3001 by using create-react-app proxy feature
- Use the graphql endpoint to get/create/update/delete

### Contact
fetch contacts from api "https://jsonplaceholder.typicode.com/users" and put it into state of contacts

## Available Scripts

In the project directory, you can run:

### `npm start`

Runs the app in the development mode.

Open [http://localhost:3000](http://localhost:3000) to view it in the browser.

The page will reload if you make edits.
You will also see any lint errors in the console.

### `npm run gql`

Runs the graphql server.

Open [http://localhost:3001](http://localhost:3001) to view it in the browser.

### `npm test`

Launches the test runner in the interactive watch mode.

See the section about [running tests](https://facebook.github.io/create-react-app/docs/running-tests) for more information.

### `to host into git hub`
1. Install and Configure Github Pages
Install the Github Pages library.

npm install gh-pages --save-dev

Next, open up package.json and paste in the homepage property at the top of the object.

"homepage": "https://yourusername.github.io/yourrepositoryname",

You will need to locate your username and repository name to modify the URL accordingly.

Next, add the following properties to the script object.

"scripts": {
  // ... other commands
  "predeploy": "npm run build",
  "deploy": "gh-pages -d build"
},
2. Deploy to Github Pages
Push your changes to your repository.

$ git add package.json package-lock.json
$ git commit -m "deploy setup for Github Pages"
$ git push
In a terminal located at the root of the project (where you installed gh-pages in the previous step), run the command npm run deploy.

This creates a new branch that hosts your React app named gh-pages.

3. Confirm Deployment on Github
Open a browser and navigate to your Github repository.

Click on the Settings tab and scroll down to the Github Pages section.

github pages setting
The Source attribute needs to be set to the gh-pages branch. You can also find your site URL and customize the domain name.

If you visit the page the API call for weather data will not work. There is not a function set up to fetch the data because we cannot secure our API key on the front end.

error message on website
The Axios API call URL in App.js could be modified to call a serverless function set up on a cloud provider. Check out one of the other deployment options for setting up serverless functions.