# config-file-heroku-buildpack
Heroku Buildpack to add a config file to heroku app
This is useful when you don't want to include config file in the github repository as it may contain personal credentials.

Steps to use this Buildpack:
- Add the following config vars in heroku app settings:
    - CONFIG_FILE_NAME containing the name of config file (eg. config.py for python projects)
    - CONFIG_FILE_CONTENT containing the data to store in config file. (Add double quotes (" ") around the content and avoid using double quotes inside it.)

- Now add this buildpack .git link in the buildpack option and keep this buildpack above the default buildpack.