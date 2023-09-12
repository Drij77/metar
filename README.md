# metar

## install requirements mentioned in requirements.txt

## Install redis in windows 
### Download zip file from https://github.com/tporadowski/redis/releases and run exe file and cli.exe file once connected to in cli it will show like 127.0.0.1:6379>

## For mac os 
### Follow this https://redis.io/docs/getting-started/installation/install-redis-on-mac-os/ once it will connected to port 6379 we are ready to go

## API endpoint and response 
### Endpoint   GET http://127.0.0.1:8000/metar/info?scode=ANYN&&nocache=1
### Response { "station": "ASEZ",
###    "last_observation": "2011/07/04 at 06:00 GMT",
###    "temperature": "-11 C (12.2 F)",
###    "wind": "NW at 7 mph (06 knots)"
### }
### Endpoint   GET http://127.0.0.1:8000/metar/ping
### Response{
###    "data": "pong"
### }
## To check data in redis 
### Command to execute in redis cli : GET <KEY> here key os scode which we are passing in url 
### Suppose in above url scode is ANYN so in redis cli our command will be 
### GET "ANYN"
### Response :-  "{\"station\": \"BAAB\", \"last_observation\": \"2015/05/06 at 00:00 GMT\", \"temperature\": \"-15 C (5.0 F)\", \"wind\": \"SE at 5 mph (04 knots)\"}"
