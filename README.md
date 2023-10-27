# Angular build Github Pages

1. Install the following packages

      ```bash
      npm i del-cli --save-devs
      npm i copyfiles --save-devs
      ```

2. Add on package.json

      ```js
      "scripts": {
      	...
      	"delete:docs": "del /Q docs",
      	"copy:dist": "copyfiles dist/NAME_APP/* ./docs -f",
      	"build:href": "ng build --base-href ./",
      	
      	"build:github": "npm run delete:docs && npm run build:href && npm run copy:dist"
      }
      ```

3. Execute

      ```bash
      npm run build:github
      ```

4. GithubPages
    * Open Github
    * Select project repository
    * Select Settings
    * Select Pages
    * In Build and deployments, select branch and directory /docs 
    * Click in Save
    * Select tab Actions to verify the progress
