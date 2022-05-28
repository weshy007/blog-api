## Viewsets and Routers
- Viewsets and routers are tools within Django REST Framework that can speed-up API development. They are an additional layer of abstraction on top of views and URLs. The primary benefit is that a single viewset can replace multiple related views. And a router can automatically generate URLs for the developer.

|Endpoint                               |HTTP Verb|
|---------------------------------------|---------|
|/                                      |GET|
|/:pk/                                  |GET|
|/rest-auth/registration                |POST|
|/rest-auth/login                       |POST|
|/rest-auth/logout                      |GET|
|/rest-auth/password/reset              |POST|
|/rest-auth/password/reset/confirm      |POST|

- The first two endpoints were created by us while django-rest-auth provided the five others.(Before using viewsets and routers)

### Viewsets
- A viewset is a way to combine the logic for multiple related views into a single class. In other words, one viewset can replace multiple views.

### Routers
- Routers work directly with viewsets to automatically generate URL patterns for us.
- Django REST Framework has two default routers: _SimpleRouter_ and _DefaultRouter_.


### <b>NB</b> 
--> It is possible to customize viewsets but an important tradeoff in exchange for writing a bit less code with viewsets is the default settings may require some additional configuration to match exactly what you want. **

--> Viewsets and routers are a powerful abstraction that reduce the amount of code we as developers must write. However this conciseness comes at the cost of an initial learning curve.**

--> Ultimately the decision of when to add viewsets and routers to your project is quite subjective. A good rule of thumb is to start with views and URLs. As your API grows in complexity if you find yourself repeating the same endpoint patterns over and over again, then look to viewsets and routers. **