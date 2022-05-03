# heroku-docker-nginx-example

Barebones example of deploying
[the official nginx Docker image](https://github.com/docker-library/docs/tree/master/nginx)
to Heroku. Serves an example html file at the root directory.

## Try it now!

Fire up an nginx proxy on [Heroku](https://www.heroku.com/) with a single click:

[![Deploy to Heroku](https://www.herokucdn.com/deploy/button.svg)](https://heroku.com/deploy)

## Manual deployment

You will need to create a Heroku account and install the Heroku CLI, eg.
`brew install heroku`.

```
git clone https://github.com/nik-iedaas/heroku-docker-nginx-example.git
cd heroku-docker-nginx-example

In default.conf.template we need update endpoints in proxy_pass

for example :- location /url {
    proxy_pass endpoint
}

build docker image :- sudo docker build -t checklistreverseproxy .

for check images :- sudo docker images
 
sudo heroku login
sudo heroku container:login
sudo heroku container:push web -a rocky-reaches-66468
sudo heroku container:release web -a rocky-reaches-66468
heroku open
```
