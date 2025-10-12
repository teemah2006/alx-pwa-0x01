## API overview
Collection of information for movies, tv-shows, actors. Includes youtube trailer url, awards, full biography, and many other usefull informations. 
This api provides complete and updated data for over 9 million titles ( movies, series and episodes) and 11 million actors / crew and cast members. 

## Version
Recent titles are updated weekley - Ratings / episodes light are updated daily

## Available Endpoints
- Titles: description: returns array of titles according to filters / sorting query parameters provided
query parameters: multiple, unique query parameter 'list' that sets the collection you want to query - options available in Utils - Titles Lists
model: title
- Titles by Keyword:  returns array of titles according to filters / sorting query parameters provided and the keyword provided in path
- Actors: eturns array of actors according to filters provided
- Title Type: returs array of title types

## Request and Response Format
Example request:

const res = await fetch(/titles, {
method: "GET",
headers: {X-Rapidapi-Key: API_KEY

X-Rapidapi-Host: moviesdatabase.p.rapidapi.com

Host: moviesdatabase.p.rapidapi.com
}
})

Example response:
{
  "page": 1,
  "next": null,
  "entries": 0,
  "results": []
}

## Authentication
An API key is required (gotten from rapidapi)
the headers required are: rapidapi key, host, content type.
method used it "GET"

## Error Handling
error 404 means no data found
the request should be in a try-catch block e.g
try{ .....}
catch(err){
if (err.status == 404) throw new error 'No data found'
}
and so on

## Usage Limits and Best Practices 
Rate limit is 1000 requests per hour
Request limit it 500,000 per month




