# HTTP Service
### A simple Javascript HTTP service

This service uses the new Javascript fetch API to expose a simple api for http requests. This allows developers to make simple requsts to a web API and has built in support for GET, PUT, POST, and DELETE requests.

To simplify the service, default headers are specified in the service and automatically added to the requests. If you would like to specify unique headers for each request, you could simply add a third parameter to the exposed methods on the service.
