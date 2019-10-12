# steam-dashboard
A flexdashboard in R looking at Steam games

### Heroku hosting

In order to host this app on Heroku, it is necessary to downgrade the standard Heroku stack (from 18 to 16), and to use a buildpack. 

Run the following commands:

```
$ heroku login
$ heroku apps:create steam-dashboard
$ heroku stack:set heroku-16
$ heroku buildpacks:add http://github.com/virtualstaticvoid/heroku-buildpack-r.git#heroku-16
$ git push heroku master
```