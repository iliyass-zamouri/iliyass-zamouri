# Flutter Web Deployment Docs

### 1- Fist the app should be web friendly.
- Making the app responsive for diffrent view ports.
- Well tested, debuged.

### 2- You should change the url_strategy to remove the hash for the url

### 3- Change the app name from the main.dart Material title

### 4- Change the <title> tag name in the web/index.html
```html
<title>Iliyass Zamouri</title>
```
  
### 5- Change the meta description tag content in the same file (index.html)
```html
  <meta name="description" content="Hi my name is Iliyass Zamouri I'm a Software Developer">
```
  
### 6- Add those favicon tags
```html
    <!-- favicons -->
  <link rel="shortcut icon" href="favicon.ico" type="image/x-icon">
  <link rel="icon" href="favicon.ico" type="image/x-icon">
```
  
### 7- Go to manifest.json file and change the app name,short_name description (you can change color theme and background if you like)
```json
  {
    "name": "Iliyass Zamouri",
    "short_name": "Iliyass Zamouri",
    "background_color": "#0175C2",
    "theme_color": "#0175C2",
    "description": "Hi my name is Iliyass Zamouri I'm a Software Developer",
    ...
  ```
  
  ### 8- Go to [favicon.io](https://https://favicon.io), upload your favicon png file 
  then download the zip file from the website, extract it now change override favicon.png (web/favicon.png) with the favicon.ico
  and go to icons folder (web/icons) and overrride also the 192px icon with its equivalent same thing with the 512px (keep same names).
  
### 9- run this command
  If your app is integrated to null safety
  ```
  flutter build web
  ```
  Or this command if it does not
  ```
  flutter build web --no-sound-null-safety
  ```
  If the build succeed, the flutter sdk will generate a web folder in the build folder.
  
### 10- The app is ready to be deployed
 - Go to .gitignore file comment the line /build/ then commit to the project repo.
 - Push your app to github or gitlab.
 - then you can use a service like [Netlify](https://www.netlify.com) to deploy the app online.
 - when selecting the repo make sure the deployment folder is >>build/web<<
  
