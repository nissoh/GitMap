# GitMap
**A location based job board powered only by GitHub.**

This demo explores the possibility of building a location based app by using *only* [GitHub's cool ability to render GeoJSON files](https://help.github.com/articles/mapping-geojson-files-on-github/) as - interactive, browsable, annotated maps, and the powerful GitHub API (Nicely wrapped by [Github.js](https://github.com/michael/github)). You can think of it as a "serverless" GitHub architecture.

![gitmap](https://cloud.githubusercontent.com/assets/5776439/12868306/39998b0e-cd0c-11e5-9e0f-77670fed4eeb.png)

#### How GitMap works?
- The site is served by GitHub pages.
- The main page loads a `render.githubusercontent` iframe which renders the [map.geojson](map.geojson) as a full screen map.
- When publishing a new entry, your browser will execute the calls to GitHub API by using [Github.js](https://github.com/michael/github)
- A request will be sent by you to fork this repository.
- The [map.geojson](map.geojson) file in the forked repository will be edited to contain the new published data.
- A pull request will be created in your behalf, to merge the new data to the main repository.
- I manully merge and approve pull requests. (For now)

#### GitHub authentication 
Although your GitHub credentials are not stored or being sent to any unauthorized party, using your GitHub password in any site other than GitHub is problematic. I want to replace the authentication with [GitHub OAuth](https://developer.github.com/v3/oauth/), but I'm not sure how to do it without exposing the client_secret in the web client. 

#### My first project with react
![Me working with react](http://i1.kym-cdn.com/photos/images/original/000/234/765/b7e.jpg)

