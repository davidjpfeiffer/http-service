# Javascript HTTP Service

A lightweight Javascript service for making HTTP requests

### About

A simple and lightweight JavaScript service for making asynchronous http requests to a web server. The service has built in support for GET, PUT, POST, and DELETE requests. Each of these request types are exposed as methods on the service, all of which return a promise.

To simplify the requests, default headers are specified in the service and are automatically added to each request. If you would like to specify unique headers for each request, you can modify the service to take in a headers object as an extra parameter.

### Usage

If the request is successful, the code below will print a list of people. If it is not successful, an error message will be logged to the console.

```javascript
window.httpService.get('api/v1/people')
.then(onSuccess)
.catch(onError);

function onSuccess(response) {
  response.forEach(person => {
    console.log(person + ' ');
  });
}

function onError(response) {
  console.log('Something went wrong.');
}
```
