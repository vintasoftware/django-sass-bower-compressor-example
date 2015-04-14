# django-sass-bower-compressor-example
Example Django 1.8 project using django-libsass, django-bower and django-compressor.

## How to run
```sh
# first activate a virtualenv, then:
pip install -r requirements.txt 
python manage.py bower_install  # with underline!
python manage.py runserver
```

## How to deploy (to Heroku)
```sh
# first create a new heroku dyno or set the heroku remote, then:
# set BUILDPACK_URL, since this project uses Bower (node) and Django (Python):
heroku config:set BUILDPACK_URL=https://github.com/vintasoftware/heroku-buildpack-multi.git
# set django-settings, edit with your own values:
heroku config:set DEBUG=False \
                  ALLOWED_HOSTS=FILL-HERE-WITH-A-*-OR-A-VALUE-OR-A-COMMA-SEPARATED-LIST \
                  AWS_ACCESS_KEY_ID=FILL-HERE \
                  AWS_SECRET_ACCESS_KEY=FILL-HERE \
                  AWS_STORAGE_BUCKET_NAME=FILL-HERE \
                  SECRET_KEY=FILL-HERE
```
