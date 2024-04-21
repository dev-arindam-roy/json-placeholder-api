# JSON Placeholder APIS

[API DOCUMENTATION](https://jsonplaceholder.typicode.com/)

### CODES

```js
const postApiUrl = "https://jsonplaceholder.typicode.com/posts";
fetch(postApiUrl).then((responsestream) => {
    return responsestream.json();
}).then((jsonArrObj) => {
    if (jsonArrObj.length) {
        jsonArrObj.map((value, index) => {
            document.getElementById('postApiOutput').innerHTML += `<div>Post Number - ${index + 1} <br/> <strong>POST ID:</strong> ${value.id} <br/> <strong>TITLE:</strong> ${value.title} <br/> <strong>BODY:</strong> ${value.body}</div><hr/>`;
        })
    } else {
        document.getElementById('postApiOutput').innerHTML = "<h4>No Records Found</h4>";
    }
});


const photoApiUrl = "https://jsonplaceholder.typicode.com/photos";
fetch(photoApiUrl).then((responsestream) => {
    return responsestream.json();
}).then((jsonArrObj) => {
    if (jsonArrObj.length) {
        jsonArrObj.forEach((value, index) => {
            if (index < 100) {
                let photoCard = `<div class="col-md-4 mb-2">
                        <div class="card">
                            <div class="card-header">
                                <strong>PHOTO ID: ${value.id}</strong>
                            </div>
                            <div class="card-body">
                                <img src="${value.thumbnailUrl}" class="img-thumbnail" />
                            </div>
                            <div class="card-footer">
                                <span style="font-size: 10px;">${value.title}</span>
                            </div>
                        <div>
                </div>`;
                
                document.getElementById('photoApiOutput').innerHTML += photoCard
            }
        })
    } else {
        document.getElementById('photoApiOutput').innerHTML = "<h4>No Photos Found</h4>";
    }
});
```

[Check the Apllication](https://dev-arindam-roy.github.io/json-placeholder-api/)

## Thanks!
