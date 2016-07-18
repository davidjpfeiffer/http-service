# Javascript HTTP Service

### About

This simple JavaScript service exposes a simple api for http requests. The requests are made using the new JavaScript fetch API. This allows developers to easily make requsts to a web API and has built in support for GET, PUT, POST, and DELETE requests.

To simplify the requests, default headers are specified in the service and are automatically added to each request. If you would like to specify unique headers for each request, you can modify the service to take in a headers object as a third parameter.

### Usage

If the request is successful, the code below will print a list of people. If it is not successful, an error message will be logged to the console.

```javascript
app.httpService.get('api/v2/people')
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
