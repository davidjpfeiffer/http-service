# Javascript HTTP Service

A simple JavaScript service that exposes an api for making http requests. The requests are made using the new JavaScript fetch api. This allows developers to easily make requsts to a web api and has built in support for GET, PUT, POST, and DELETE requests.

To simplify the requests, default headers are specified in the service and are automatically added. If you would like to specify unique headers for each request, you can modify the service to take in a headers object as an extra parameter.

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
