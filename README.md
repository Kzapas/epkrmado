# Python Flask Heroku Krunker Map API
This web application is based an introduction to background worker processes in Heroku, which can be found at the [Heroku Devcenter](https://devcenter.heroku.com/articles/python-rq).

I've made the 'web' process return a job id instead of the actual job result. The job id can be saved by the client, and used subsequently to long-poll the web process. Once the worker is done, when queried with the job id, the web process returns the result.

Example to start map downloader: https://yoururl.herokuapp.com/?name=nameofmap

Make sure to copy the job id somewhere safe for later use.

Example to retrieve map data generated: https://yoururl.herokuapp.com/?job=jobid

I've also added app.json and this readme so you can:

## Deploy to Heroku
By clicking the button below.

[![Deploy](https://www.herokucdn.com/deploy/button.svg)](https://heroku.com/deploy)