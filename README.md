# React App Deployment Steps

1. Create an empty repository

2. Install the gh-pages package as a "dev-dependency" of the app.
```
$ cd "Your react app"
$ npm install gh-pages --save-dev
```

3. Add these properties to the app's package.json file.

- At the top level, add a homepage property
```
"homepage": "https://pages.git.generalassemb.ly/<GitHub Username>/<Repo Name>/"
```
- In the existing scripts property, add a predeploy property and a deploy property, each having the values shown below:
```
"scripts": {
  //...
  "predeploy": "npm run build",
  "deploy": "gh-pages -d build"
}
```
4. Create a git repository in the app's folder.
```
$ git init
```

5. Add "git remote add origin" in your local git repository.

6. Generate a production build of your app, and deploy it to GitHub Pages.
```
$ npm run deploy
```
7. That's it! Your app is now accessible at the URL you specified in step 3.
