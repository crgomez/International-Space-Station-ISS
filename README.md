# International-Space-Station-ISS
OpenNotify has several API endpoints. An endpoint is a server route that is used to retrieve different data from the API. This endpoint gets the current latitude and longitude of the International Space Station. we'll be querying a simple API to retrieve data about the International Space Station (ISS). 

```
# Set up the parameters we want to pass to the API.
# This is the latitude and longitude of Verizon Digital Media Services (Los Angeles).
# You can find the lat & lon using My Nasa Data: https://mynasadata.larc.nasa.gov/latitudelongitude-finder/
parameters = {"lat": 40.71, "lon": -74}

# Make a get request with the parameters.
response = requests.get("http://api.open-notify.org/iss-pass.json", params=parameters)

# Print the content of the response (the data the server returned)
print(response.content)
```

```
# OUTPUT
{
  "message": "success", 
  "request": {
    "altitude": 100, 
    "datetime": 1535266621, 
    "latitude": 33.975141, 
    "longitude": -118.425985, 
    "passes": 5
  }, 
  "response": [
    {
      "duration": 396, 
      "risetime": 1535284309
    }, 
    {
      "duration": 638, 
      "risetime": 1535289944
    }, 
    {
      "duration": 539, 
      "risetime": 1535295805
    }, 
    {
      "duration": 330, 
      "risetime": 1535301780
    }, 
    {
      "duration": 376, 
      "risetime": 1535307652
    }
  ]
}
```
