# Web fetch request

## fetch general forms

### 
```javascript
// fetch form 1 (using then)
fetch(url, {
headers: {},
method: “POST”,

})
.then(res => res.json())
.then(data => console.log(data))
.catch()

// fetch form 2 (using async await)
try{
const res = await fetch()

// json() converts a json string to JS object
const data = await res.json()

// process data

} catch (error) {
// Do error handling
}
```

fetch can take `string`, `url` or `request` object as first parameter.

If `response.ok` is truthy then `response.status` is in the range 200-299.

request can take `string` or `url` as the first parameter.

## Response object

To get access to body of a response use one of the following as applicable.

1. response.text()  : Applicable when request object has a body with text content. 
2. response.json()  : Applicable when request object has a body with JSON data/content.
3. `content-type` header is `application/json`JSON.stringify(JS-Object) content.
4. response.text()  : Applicable when request object has a body with text content. 
