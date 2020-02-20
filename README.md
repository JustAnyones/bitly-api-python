Original at https://github.com/bitly/bitly-api-python seems abandoned.
I tried to aggregate the good pull-requests in this repo.

This lib works againt the old bitly API ( v3 ? )

You should propably have a look at this one if you dont allrady have a lot of old code written againt this one and can accept Python 3.7+ only:

https://github.com/impredicative/bitlyshortener

bitly API python library
========================

## Installation

    pip install git+git://github.com/jimmy927/bitly-api-python
    
    also putting "git+git://github.com/jimmy927/bitly-api-python" in your requirements.txt will work.

## Usage

    import bitly_api
    c = bitly_api.Connection('bitlyapidemo','R_{{apikey}}')
    # or to use oauth2 endpoints
    c = bitly_api.Connection(access_token='...')
    c.shorten('http://www.google.com/')


## Run tests

Your username is the lowercase name shown when you login to bitly, your access token can be fetched using the following ( http://dev.bitly.com/authentication.html ):

    curl -u "username:password" -X POST "https://api-ssl.bitly.com/oauth/access_token"

To run the tests either export the environment variable or set it up inline before calling `nosetests`:

    bitly-api-python $ BITLY_ACCESS_TOKEN=<accesstoken> nosetests

## API Documentation

http://dev.bitly.com/
