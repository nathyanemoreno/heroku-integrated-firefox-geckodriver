# heroku-integrated-firefox-geckodriver

[![Build Status](https://travis-ci.org/nathyanemoreno/heroku-integrated-firefox-geckodriver.svg?branch=master)](https://travis-ci.org/pyronlaboratory/heroku-integrated-firefox-geckodriver)
[![Requirements Status](https://requires.io/github/nathyanemoreno/heroku-integrated-firefox-geckodriver/requirements.svg?branch=master)](https://requires.io/github/nathyanemoreno/heroku-integrated-firefox-geckodriver/requirements/?branch=master)

Buildpack `heroku-integrated-firefox-geckodriver` enables your application or client code - running in any high-level language such as *Python, Ruby or Node.js* - to access **Firefox** along with **Geckodriver** (the Selenium driver for Firefox) in a Heroku slug and enables the driver objects to perform automated operations defined in the source code.

Installation:
-----

To install and integrate the buildpack with your application running on Heroku's dyno:

```shell
$ heroku create --buildpack https://github.com/pyronlaboratory/heroku-integrated-firefox-geckodriver

# or if your app is already created:
$ heroku buildpacks:add https://github.com/pyronlaboratory/heroku-integrated-firefox-geckodriver

$ git push heroku master
```

Configurations:
-----

Update Heroku's environment variables to store the following path strings. 
                                
  
**FIREFOX_BIN**: */app/vendor/firefox/firefox*

**GECKODRIVER_PATH**: */app/vendor/geckodriver/geckodriver*

**LD_LIBRARY_PATH**: */usr/local/lib:/usr/lib:/lib:/app/vendor*

**PATH**: */usr/local/bin:/usr/bin:/bin:/app/vendor/*
```
