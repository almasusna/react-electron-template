# react-electron-template

npx create-react-app react-electron

yarn add electron concurrently wait-on cross-env


### Package json: under scripts
   "electron:serve": "concurrently -k \"cross-env BROWSER=none yarn start\" \"yarn electron:start\"",
   
    "electron:build": "yarn build && electron-builder -c.extraMetadata.main=build/main.js",
    
    "electron:start": "wait-on tcp:3000 && electron ."


### Above scripts:
 "main": "public/main.js",
  "homepage": "./",
  
### Adding public/main.js
See public/main.js
  
### To make React communicate with Electron through IPC
yarn add @electron/remote
See at main.js -> enableRemoteModule: true


### To run
yarn electron:serve

### Extra
yarn add bootstrap@next

### For build add in package.json
"build": {
    "extends": null,
    "appId": "com.example.electron-cra",
    "files": [
      "dist/**/*",
      "build/**/*",
      "node_modules/**/*",
      "package.json"
    ],
    "directories": {
      "buildResources": "assets"
    }
    

