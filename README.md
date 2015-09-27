# wiremock-heroku
A simple way to deploy WireMock on to Heroku

- Clone this repository
```
git clone git@github.com:Mahoney/wiremock-heroku.git
cd wiremock-heroku
```
- Add a heroku remote
```
heroku create <unique_app_name>
```
- Add the [Energized Work](http://www.energizedwork.com) downloadable jar buildpack
```
heroku config:set 'NO_PRE_DEPLOY=true'
heroku buildpacks:set https://github.com/energizedwork/heroku-buildpack-runnable-jar
```
- Start the app
```
git push heroku master
```
- Check it
```
curl http://<unique_app_name>.herokuapp.com/__admin/
```
