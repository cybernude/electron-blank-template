#copy folder config
electron-blank-template\config

#copy entry.js, entry.live.js, package.json.txt from 
electron-blank-template\src

#edit package.json from electron-blank-template\

#change
  "scripts": {
    "ng": "ng",
    "start": "concurrently \"cpx config/common.js node_modules/@angular/cli/models/webpack-configs\" \"ng serve\" \"electron src/entry.live.js\"",
    "run": "electron .",
    "build": "concurrently \"cpx config/common.js node_modules/@angular/cli/models/webpack-configs\" \"ng build --base-href=./\" \"cpx ./src/entry.js ./dist/\"",
    "test": "ng test",
    "lint": "ng lint",
    "e2e": "ng e2e"
  },
  
  #and insert this config to "devDependencies": {
  "@types/electron": "^1.4.35",
  
    "concurrently": "^3.4.0",
    "cpx": "^1.5.0",
    "electron": "^1.6.11",
