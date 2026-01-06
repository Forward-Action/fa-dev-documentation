# fa-dev-documentation

## Requirements

* Node.js (20+)
* NPM (11+)
* Honkit (6+)

## Project

The documentation uses [Honkit](https://honkit.netlify.app/) in order to create the structure and navigation.

This repository has a GitHub Pages site which can be found at [documentation.forwardaction.uk](https://documentation.forwardaction.uk).

GitHub Pages uses the `docs` directory as it's root. Do not delete this directory. 

## Development

All documentation is found in the `files` directory. Edit the .md files here or add new ones using the [Honkit](https://honkit.netlify.app/pages) documentation as a guide.

When first setting up the project. Run the following commands:
````
yarn install
yarn add honkit --dev
yarn start
````

To see a local version of the site, run:
````
yarn serve
````

## Deployment

### Step 1
Before deploying, run:

```
yarn build
```

This will build the site structure using Honkit and output it to a directory named `_book`. It will then delete the older `docs` directory and rename the new `_book` directory to `docs`. This is necessary for the GitHub Pages site to function properly.

### Step 2
Commit all changes and push to the `main` branch. This will trigger an Action in GitHub to deploy to the Pages site. You can see deployment process and any errors [here](https://github.com/Forward-Action/fa-dev-documentation/actions).

### Step 3
Go to [documentation.forwardaction.uk](https://documentation.forwardaction.uk) to see changes.
