#### Obtain JWT Token from Cognito using client id and secret

```curl

Request:

~ $ curl -X POST --user 4vv2l64c2n75l8cerdhtlobj9n:1jq2654oqb9u8rhau1oh1a719q91hmr02brf38vak31ds20g6c8o 'https://sppparkingsystem.auth.us-east-2.amazoncognito.com/oauth2/token?grant_type=client_credentials' -H 'Content-Type: application/x-www-form-urlencoded

Response:
{"access_token":"eyJraWQiOiJ0ZEZjNXlrVlZlM1wvNXFSV2JuU01WelJEMlV5MytyWnhOeWVlM2NpS1wvQ2c9IiwiYWxnIjoiUlMyNTYifQ.eyJzdWIiOiI0dnYybDY0YzJuNzVsOGNlcmRodGxvYmo5biIsInRva2VuX3VzZSI6ImFjY2VzcyIsInNjb3BlIjoicGFya2luZy1zeXN0ZW0tYXBpXC9yZWFkIiwiYXV0aF90aW1lIjoxNTcwMDI4NDM1LCJpc3MiOiJodHRwczpcL1wvY29nbml0by1pZHAudXMtZWFzdC0yLmFtYXpvbmF3cy5jb21cL3VzLWVhc3QtMl9OUnY0MmJyN28iLCJleHAiOjE1NzAwMzIwMzUsImlhdCI6MTU3MDAyODQzNSwidmVyc2lvbiI6MiwianRpIjoiZDI5MzNjZDUtODUxYS00NDJmLTg1NDctYzM1NTEwOTFlNDNkIiwiY2xpZW50X2lkIjoiNHZ2Mmw2NGMybjc1bDhjZXJkaHRsb2JqOW4ifQ.eR3YfkcdcLBDj-sOKHdlKm63337OTGGfgHSb8QGlC-0sp56cgM5DcJ_95I3l8iwYNsI1x3f76Qsnq-RXZvJSt_EP2SMMwvdm0uowFbQKoZrtAI6-JFeoKLKMlRU6Xl9VuuUantulbjsHM3k7SqWURTxeSKQE7ipic2ArGmBKIPpsOzR4JUgFY1f7UrM3kRq-34mo7loyxmPAmbVWbNnWKo8oMvIjlhPA6bc0_q1XF9yp3ywXpODq_GOkQJ_4PQWEvqt5rGd3PLkwaw4Pnwy0eqegUVnhDKHX7nh9ZXrWGoRBF4flo3zRjod7waxFKXwquRZQf8IZFy-vZGYnZB3lBg","expires_in":3600,"token_type":"Bearer"}
```

#### Get the list of status of nearby parking spots
```curl

Request:

curl  -X GET 'https://nzrrb10bk2.execute-api.us-east-2.amazonaws.com/prod/parking-spots?lat=-32.8645&long=25.9577&radius=100000' -H 'Content-Type: application/json' -H 'Authorization:eyJraWQiOiJ0ZEZjNXlrVlZlM1wvNXFSV2JuU01WelJEMlV5MytyWnhOeWVlM2NpS1wvQ2c9IiwiYWxnIjoiUlMyNTYifQ.eyJzdWIiOiI0dnYybDY0YzJuNzVsOGNlcmRodGxvYmo5biIsInRva2VuX3VzZSI6ImFjY2VzcyIsInNjb3BlIjoicGFya2luZy1zeXN0ZW0tYXBpXC9yZWFkIiwiYXV0aF90aW1lIjoxNTcwMDI4NDM1LCJpc3MiOiJodHRwczpcL1wvY29nbml0by1pZHAudXMtZWFzdC0yLmFtYXpvbmF3cy5jb21cL3VzLWVhc3QtMl9OUnY0MmJyN28iLCJleHAiOjE1NzAwMzIwMzUsImlhdCI6MTU3MDAyODQzNSwidmVyc2lvbiI6MiwianRpIjoiZDI5MzNjZDUtODUxYS00NDJmLTg1NDctYzM1NTEwOTFlNDNkIiwiY2xpZW50X2lkIjoiNHZ2Mmw2NGMybjc1bDhjZXJkaHRsb2JqOW4ifQ.eR3YfkcdcLBDj-sOKHdlKm63337OTGGfgHSb8QGlC-0sp56cgM5DcJ_95I3l8iwYNsI1x3f76Qsnq-RXZvJSt_EP2SMMwvdm0uowFbQKoZrtAI6-JFeoKLKMlRU6Xl9VuuUantulbjsHM3k7SqWURTxeSKQE7ipic2ArGmBKIPpsOzR4JUgFY1f7UrM3kRq-34mo7loyxmPAmbVWbNnWKo8oMvIjlhPA6bc0_q1XF9yp3ywXpODq_GOkQJ_4PQWEvqt5rGd3PLkwaw4Pnwy0eqegUVnhDKHX7nh9ZXrWGoRBF4flo3zRjod7waxFKXwquRZQf8IZFy-vZGYnZB3lBg'

Response:

[{"isOccupied":false,"timestamp":1519570200,"meter":{"number":2,"location":[-32.8645,25.9577],"address":"093 Harris Parkway, XYZ, AB"}},{"isOccupied":true,"timestamp":1519592400,"meter":{"number":3,"location":[-32.8645,25.9577],"address":"093 Harris Parkway, XYZ, AB"}},{"isOccupied":false,"timestamp":1519590300,"meter":{"number":1,"location":[-32.8645,25.9577],"address":"093 Harris Parkway, XYZ, AB"}}]
```

#### Get the list of nearby parking locations
```curl

Request:

curl  -X GET 'https://nzrrb10bk2.execute-api.us-east-2.amazonaws.com/prod/parking-locations?lat=-32.8645&long=25.9577' -H 'Content-Type: application/json' -H 'Authorization:eyJraWQiOiJ0ZEZjNXlrVlZlM1wvNXFSV2JuU01WelJEMlV5MytyWnhOeWVlM2NpS1wvQ2c9IiwiYWxnIjoiUlMyNTYifQ.eyJzdWIiOiI0dnYybDY0YzJuNzVsOGNlcmRodGxvYmo5biIsInRva2VuX3VzZSI6ImFjY2VzcyIsInNjb3BlIjoicGFya2luZy1zeXN0ZW0tYXBpXC9yZWFkIiwiYXV0aF90aW1lIjoxNTcwMDI4NDM1LCJpc3MiOiJodHRwczpcL1wvY29nbml0by1pZHAudXMtZWFzdC0yLmFtYXpvbmF3cy5jb21cL3VzLWVhc3QtMl9OUnY0MmJyN28iLCJleHAiOjE1NzAwMzIwMzUsImlhdCI6MTU3MDAyODQzNSwidmVyc2lvbiI6MiwianRpIjoiZDI5MzNjZDUtODUxYS00NDJmLTg1NDctYzM1NTEwOTFlNDNkIiwiY2xpZW50X2lkIjoiNHZ2Mmw2NGMybjc1bDhjZXJkaHRsb2JqOW4ifQ.eR3YfkcdcLBDj-sOKHdlKm63337OTGGfgHSb8QGlC-0sp56cgM5DcJ_95I3l8iwYNsI1x3f76Qsnq-RXZvJSt_EP2SMMwvdm0uowFbQKoZrtAI6-JFeoKLKMlRU6Xl9VuuUantulbjsHM3k7SqWURTxeSKQE7ipic2ArGmBKIPpsOzR4JUgFY1f7UrM3kRq-34mo7loyxmPAmbVWbNnWKo8oMvIjlhPA6bc0_q1XF9yp3ywXpODq_GOkQJ_4PQWEvqt5rGd3PLkwaw4Pnwy0eqegUVnhDKHX7nh9ZXrWGoRBF4flo3zRjod7waxFKXwquRZQf8IZFy-vZGYnZB3lBg'

Response:

[{"location":[-32.8645,25.9577],"address":"093 Harris Parkway, XYZ, AB"}]
```

#### Get the time-series based history of all parking status events near a location
```curl

Request:

curl  -X GET 'https://nzrrb10bk2.execute-api.us-east-2.amazonaws.com/prod/parking-history?lat=-32.8645&long=25.9577' -H 'Content-Type: application/json' -H 'Authorization:eyJraWQiOiJ0ZEZjNXlrVlZlM1wvNXFSV2JuU01WelJEMlV5MytyWnhOeWVlM2NpS1wvQ2c9IiwiYWxnIjoiUlMyNTYifQ.eyJzdWIiOiI0dnYybDY0YzJuNzVsOGNlcmRodGxvYmo5biIsInRva2VuX3VzZSI6ImFjY2VzcyIsInNjb3BlIjoicGFya2luZy1zeXN0ZW0tYXBpXC9yZWFkIiwiYXV0aF90aW1lIjoxNTcwMDI4NDM1LCJpc3MiOiJodHRwczpcL1wvY29nbml0by1pZHAudXMtZWFzdC0yLmFtYXpvbmF3cy5jb21cL3VzLWVhc3QtMl9OUnY0MmJyN28iLCJleHAiOjE1NzAwMzIwMzUsImlhdCI6MTU3MDAyODQzNSwidmVyc2lvbiI6MiwianRpIjoiZDI5MzNjZDUtODUxYS00NDJmLTg1NDctYzM1NTEwOTFlNDNkIiwiY2xpZW50X2lkIjoiNHZ2Mmw2NGMybjc1bDhjZXJkaHRsb2JqOW4ifQ.eR3YfkcdcLBDj-sOKHdlKm63337OTGGfgHSb8QGlC-0sp56cgM5DcJ_95I3l8iwYNsI1x3f76Qsnq-RXZvJSt_EP2SMMwvdm0uowFbQKoZrtAI6-JFeoKLKMlRU6Xl9VuuUantulbjsHM3k7SqWURTxeSKQE7ipic2ArGmBKIPpsOzR4JUgFY1f7UrM3kRq-34mo7loyxmPAmbVWbNnWKo8oMvIjlhPA6bc0_q1XF9yp3ywXpODq_GOkQJ_4PQWEvqt5rGd3PLkwaw4Pnwy0eqegUVnhDKHX7nh9ZXrWGoRBF4flo3zRjod7waxFKXwquRZQf8IZFy-vZGYnZB3lBg'

Response:

[{"isOccupied":true,"timestamp":1519569600,"meter":{"number":2,"location":[-32.8645,25.9577],"address":"093 Harris Parkway, XYZ, AB"}},{"isOccupied":false,"timestamp":1519550100,"meter":{"number":3,"location":[-32.8645,25.9577],"address":"093 Harris Parkway, XYZ, AB"}},{"isOccupied":true,"timestamp":1519528800,"meter":{"number":2,"location":[-32.8645,25.9577],"address":"093 Harris Parkway, XYZ, AB"}},{"isOccupied":false,"timestamp":1519559700,"meter":{"number":2,"location":[-32.8645,25.9577],"address":"093 Harris Parkway, XYZ, AB"}},{"isOccupied":true,"timestamp":1519545300,"meter":{"number":3,"location":[-32.8645,25.9577],"address":"093 Harris Parkway, XYZ, AB"}},{"isOccupied":false,"timestamp":1519585500,"meter":{"number":3,"location":[-32.8645,25.9577],"address":"093 Harris Parkway, XYZ, AB"}},{"isOccupied":false,"timestamp":1519551000,"meter":{"number":3,"location":[-32.8645,25.9577],"address":"093 Harris Parkway, XYZ, AB"}},{"isOccupied":false,"timestamp":1519569900,"meter":{"number":2,"location":[-32.8645,25.9577],"address":"093 Harris Parkway, XYZ, AB"}},{"isOccupied":false,"timestamp":1519570200,"meter":{"number":2,"location":[-32.8645,25.9577],"address":"093 Harris Parkway, XYZ, AB"}},{"isOccupied":true,"timestamp":1519551300,"meter":{"number":1,"location":[-32.8645,25.9577],"address":"093 Harris Parkway, XYZ, AB"}},{"isOccupied":false,"timestamp":1519525200,"meter":{"number":1,"location":[-32.8645,25.9577],"address":"093 Harris Parkway, XYZ, AB"}},{"isOccupied":false,"timestamp":1519590300,"meter":{"number":1,"location":[-32.8645,25.9577],"address":"093 Harris Parkway, XYZ, AB"}},{"isOccupied":true,"timestamp":1519592400,"meter":{"number":3,"location":[-32.8645,25.9577],"address":"093 Harris Parkway, XYZ, AB"}},{"isOccupied":false,"timestamp":1519547700,"meter":{"number":2,"location":[-32.8645,25.9577],"address":"093 Harris Parkway, XYZ, AB"}},{"isOccupied":true,"timestamp":1519589400,"meter":{"number":3,"location":[-32.8645,25.9577],"address":"093 Harris Parkway, XYZ, AB"}},{"isOccupied":false,"timestamp":1519539300,"meter":{"number":2,"location":[-32.8645,25.9577],"address":"093 Harris Parkway, XYZ, AB"}},{"isOccupied":true,"timestamp":1519545000,"meter":{"number":3,"location":[-32.8645,25.9577],"address":"093 Harris Parkway, XYZ, AB"}},{"isOccupied":false,"timestamp":1519584900,"meter":{"number":3,"location":[-32.8645,25.9577],"address":"093 Harris Parkway, XYZ, AB"}},{"isOccupied":false,"timestamp":1519538700,"meter":{"number":2,"location":[-32.8645,25.9577],"address":"093 Harris Parkway, XYZ, AB"}},{"isOccupied":true,"timestamp":1519536000,"meter":{"number":2,"location":[-32.8645,25.9577],"address":"093 Harris Parkway, XYZ, AB"}},{"isOccupied":true,"timestamp":1519551900,"meter":{"number":2,"location":[-32.8645,25.9577],"address":"093 Harris Parkway, XYZ, AB"}},{"isOccupied":false,"timestamp":1519547100,"meter":{"number":2,"location":[-32.8645,25.9577],"address":"093 Harris Parkway, XYZ, AB"}},{"isOccupied":false,"timestamp":1519563600,"meter":{"number":2,"location":[-32.8645,25.9577],"address":"093 Harris Parkway, XYZ, AB"}}]
```
