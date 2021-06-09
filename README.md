# Intro:
*Hola API is based on the Django REST Framework and has the features to create Posts and Vote for different posts.
The API accepts JSON data, and the CRUD requests to perform different operations.*

You may use the below test credentials:
username- tester
password- raghu5678

## Below are the examples of using this API:

**Retrieve all Posts-** GET <http://127.0.0.1:8000/api/posts>
Posts output has the following structure-
   	{
        "id": 4,
        "title": "Private Search Engine",
        "url": "https://duckduckgo.com",
        "poster": "superboss",
        "poster_id": 1,
        "created": "2021-06-06T17:39:00.422266Z",
        "votes": 0
    	},

**Create Posts-** POST <http://127.0.0.1:8000/api/posts>
### Body-

{
    "title": "Example Title",
    "url": "https://example.org"
}

**Retrive single post-** GET <http://127.0.0.1:8000/api/posts/"post_id">

**Vote for a Post-** POST <http://127.0.0.1:8000/api/posts/"post_id"/vote>
No Body required

**Delete a vote(unvote)-** DELETE <http://127.0.0.1:8000/api/posts/"post_id"/vote>

**Update a Post-** PUT/PATCH <http://127.0.0.1:8000/api/posts/"post_id">
### Body-

{
    "id": 3,
    "title": "Private Search Engine",
    "url": "https://duckduckgo.com",
    "poster": "superboss",
    "poster_id": 1,
    "created": "2021-06-06T17:38:52.232373Z",
    "votes": 0
}

PUT- to update all fields
PATCH- to update specific fields

**Delete a Post-** DELETE <http://127.0.0.1:8000/api/posts/"post_id">
