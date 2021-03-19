# config-file-heroku-buildpack
Heroku Buildpack to add a config file to heroku app.
This is useful when you don't want to include config file in the github repository as it may contain personal credentials.

Steps to use this Buildpack:
- Add the following config vars in heroku app settings:
    - `CONFIG_FILE_NAME` containing the name of config file (eg. config.py for python projects). config files inside subdirectories are also supported, e.g- app/config.py, provided app/ directory already exists.
    - `CONFIG_FILE_CONTENT` containing the data to store in config file.

- Now add this buildpack using `anshit01/config-file` or the .git link of this repo in the buildpack option and keep this buildpack above the default buildpack.

Buildpack registered at `anshit01/config-file` in Heroku buildpacks registery.
