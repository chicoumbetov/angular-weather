# WeatherApp

Deployment on chicoumbetov.github.io/angular-weather

This project was generated with [Angular CLI](https://github.com/angular/angular-cli) version 13.1.2.

## Development server

Run `ng serve` for a dev server. Navigate to `http://localhost:4200/`. The app will automatically reload if you change any of the source files.

## Code scaffolding

Run `ng generate component component-name` to generate a new component. You can also use `ng generate directive|pipe|service|class|guard|interface|enum|module`.

## Build

Run `ng build` to build the project. The build artifacts will be stored in the `dist/` directory.

Deployement to netlify

1. Run npm install netlify netlify-cli -g && netlify login
   npm install -g netlify-cli

Refresh with Redirects
To make sure that your routes work (refreshes, etc. handled by the Angular router) you’ll want to add some redirect logic. One of the most straightforward ways to do this is by setting redirects in your Netlify configuration file, netlify.toml, mentioned above. This is what that file will be like:

2. create netlify.toml file;
3. Paste text which exists now in this file;

[build]
publish = "dist/anglify"
command = "ng build --prod"
[[redirects]]
from = "/\*"
to = "/index.html"
status = 200

4. netlify build
5. netlify deploy

DEPLOY TO GITHUB PAGES:

https://www.syncfusion.com/blogs/post/easy-steps-to-host-an-angular-app-in-github-pages.aspx

ng add angular-cli-ghpages

ng build --output-path docs --base-href /angular-weather/

ng deploy --base-href=/angular-weather/

docs folder is like build folder to deploy
