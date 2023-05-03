# Applitools ACME demo app
This repo contains HTML/CSS app that's used for the tutorials.

# Deploying it on localhost
Simply download this repo and open any html file in the browser.

## Deploying it on Heroku

We are going to deploy this as a static website. We are using Heroku's `https://github.com/heroku/heroku-buildpack-static.git` buildpack.

Option 1: 
Click the following button and follow the instructions on Heroku

[![Deploy](https://www.herokucdn.com/deploy/button.svg)](https://heroku.com/deploy?template=https://github.com/applitools/acme-demo-app)


Option 2:

    1. The `index.html` is stored in `./` folder.

    2. Create an account and have Heroku CLI installed 

    3. Have a `static.json` on the root folder that points to the folder with `index.html` **(Already exists in this repo)**.
        ```
        {
            "root": "./"
        }
        ```

    4. `heroku login`

    5. `heroku apps:create <example app name>`

    6. `heroku buildpacks:set https://github.com/heroku/heroku-buildpack-static.git`

    7. `git push heroku master`

    8. `heroku open`
