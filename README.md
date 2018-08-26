# International-Space-Station-ISS
OpenNotify has several API endpoints. An endpoint is a server route that is used to retrieve different data from the API. This endpoint gets the current latitude and longitude of the International Space Station. we'll be querying a simple API to retrieve data about the International Space Station (ISS). 
///
# Set up the parameters we want to pass to the API.
# This is the latitude and longitude of New York City.
parameters = {"lat": 40.71, "lon": -74}

# Make a get request with the parameters.
response = requests.get("http://api.open-notify.org/iss-pass.json", params=parameters)

# Print the content of the response (the data the server returned)
print(response.content)
///
