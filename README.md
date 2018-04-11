# Polymer App Toolbox - Starter Kit

### Setup

##### Prerequisites

First, install [Polymer CLI](https://github.com/Polymer/polymer-cli) using
[npm](https://www.npmjs.com) (we assume you have pre-installed [node.js](https://nodejs.org)).

    npm install -g polymer-cli

Second, install [Bower](https://bower.io/) using [npm](https://www.npmjs.com)

    npm install -g bower

### Start the development server

This command serves the app at `http://127.0.0.1:8081` and provides basic URL
routing for the app:

    polymer serve

### Build

The `polymer build` command builds your Polymer application for production, using build configuration options provided by the command line or in your project's `polymer.json` file.

You can configure your `polymer.json` file to create multiple builds. This is necessary if you will be serving different builds optimized for different browsers. You can define your own named builds, or use presets. See the documentation on [building your project for production](https://www.polymer-project.org/2.0/toolbox/build-for-production) for more information.

The Polymer Starter Kit is configured to create three builds using [the three supported presets](https://www.polymer-project.org/2.0/toolbox/build-for-production#build-presets):

```
"builds": [
  {
    "preset": "es5-bundled"
  },
  {
    "preset": "es6-bundled"
  },
  {
    "preset": "es6-unbundled"
  }
]
```

Builds will be output to a subdirectory under the `build/` directory as follows:

```
build/
  es5-bundled/
  es6-bundled/
  es6-unbundled/
```

* `es5-bundled` is a bundled, minified build with a service worker. ES6 code is compiled to ES5 for compatibility with older browsers.
* `es6-bundled` is a bundled, minified build with a service worker. ES6 code is served as-is. This build is for browsers that can handle ES6 code - see [building your project for production](https://www.polymer-project.org/2.0/toolbox/build-for-production#compiling) for a list.
* `es6-unbundled` is an unbundled, minified build with a service worker. ES6 code is served as-is. This build is for browsers that support HTTP/2 push.

Run `polymer help build` for the full list of available options and optimizations. Also, see the documentation on the [polymer.json specification](https://www.polymer-project.org/2.0/docs/tools/polymer-json) and [building your Polymer application for production](https://www.polymer-project.org/2.0/toolbox/build-for-production).

### Preview the build

This command serves your app. Replace `build-folder-name` with the folder name of the build you want to serve.

    polymer serve build/build-folder-name/

If running Windows you will need to set the following environment variables:

- LAUNCHPAD_BROWSERS
- LAUNCHPAD_CHROME

Read More here [daffl/launchpad](https://github.com/daffl/launchpad#environment-variables-impacting-local-browsers-detection)

### Work in progress

At the present state, I have worked on profile and feed page in mobile view but the same view is supported in various resolutions. This works good in Chrome, Mozilla and Edge(Not tested yet and so as lower versions of IE is not supported).
This facebook assignment is developed to support following view ports:

- 320 px
- 375 px - best view
- 480 px
- 768 px
- 1024 px
- 1440 px

Once server started you can access using following url

By default it loads profile view
- `http://localhost:8081`

I have created following files to acccess
- `http://localhost:8081/feed.html`
- `http://localhost:8081/profile.html`

### Concepts used to implement
- Basic Polymer
- Polymer Redux - Assignment does not need extensive usage but just to keep in touch, I have used this to store in one place. Ofcourse this reduces the usage of much code for user interaction.
- Shared styles.
- Simple CSS3 variables.
- Separation of concern of elements.
- Reuse of the elements.
- CSS Flex box concept, grid did not work as expected.
- Semantic HTML elements, i can expect some comments too.

### Pending work
- User interaction in profile and feed pages.
- Desktop view layout.
- Desktop view user interaction.

I have plan to work on above points as a practice even after the submission of this assignment.

### Difficulties faced
- While working in CSS i faced difficult to handle the notification, friends list + icon and direct message icon. Those are created/positioned using css and in different layout it changes alot and i had to make a fixed points to handle within the layout. May be it will be nice to have comments and suggestions about it.
- Difficult to align elements in the middle of component using grid css. I had to work in flex layout. May be it is more suitable for the desktop layout view.

### Want to learn
- grid layout, using actual grid css parameters.
- More in-depth of CSS functionalities and available functions like Calc() and pseudo functions etc.
- Handle fixed positioined elements like notifications in easy way.

### Out of scope
- Testing