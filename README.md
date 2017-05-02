# Another React Starter App!
This is where I like to start making singe page React apps. If you like it too, please use + feel free to PR.
The goal here is to get in all the pieces that I think I'm quite likely to use in any given app – not necessarily all the bells and whistles.

## Gear
- React
- Redux
- SCSS (built using node-sass)
- Express (ready to go to build additional views, like an API)
- Livereload server (requires plugin to be installed on your browser)
- Hot Module Reloading


## Out of the box

```
npm run dev
```
Find the app at `localhost:3000`
Starts the web server as well as the `webpack-dev-server` and `livereload` because we live in a sick kafka-esque distopia where it take 3 servers to run your dev process.
Starts watchers on javascript and SCSS, pop on livereload and any changes you make anywhere in the `/src` directory should automatically present in the browser.


```
npm run build
```
Builds and minifies the frontend JS and SCSS and builds the server.
You can now fire up `node ./server` and your production app should be ready to go at `localhost:3000`


## File directory
```
├── package.json
├── public/
│   └── build/                    # built app goes here
|                                 # add other static assets here (images, etc)
├── server/
│   ├── index.js
│   └── routes/
│       ├── default.js
│       └── index.js
|                                 # put in an API here
├── server-build/                 # auto-generated by npm run build – ignored by git
├── src/
│   ├── js/
│   │   ├── actions/              # redux actions here
│   │   ├── entry.js              # entrypoint for the whole app
│   │   ├── middleware/           # middlewares here
│   │   ├── reducers/             # reducers here
│   │   ├── selectors/            # selectors here
│   │   ├── shared-components/    # I like to keep 
│   │   ├── store/
│   │   ├── utils/
│   │   └── views/
│   │   │   ├── Hey               # Example of a react view (might be like /login or something)
│   │   │   │   ├── hey.scss      # SCSS for this view – this is opinionated, but I like breaking down SCSS this way
│   │   │   │   └── index.js      # The top-level react element for the view
│   │   │   ├── Layout            # Same as above, here we're spelling out a layout view
│   │   │   │   ├── components    # Components that are just for this view can go here
│   │   │   │   │   └── Header.js
│   │   │   │   ├── index.js
│   │   │   │   └── layout.scss   
│   │   │   └── index.js          # The top level view that contains the router
│   └── shared-style/ 
│       └── app.scss              # shared style throughout the app
|                                 # put things like master SCSS variables here
├── views/                        # server-side views
│   └── default.hbs               # the handlebars view that builds the HTML (remember HTML?)
├── webpack-dev-server.js         # This is all webpack \/
├── webpack.config.js
└── webpack.dev.config.js