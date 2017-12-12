### To use as module in a Node.js / TypeScript project
It is recommended to bundle your dependencies with your application. You can use [Webpack](https://github.com/webpack/webpack) or [Browserify](http://browserify.org/).

Install it as a dependency for your existing project using [npm](https://www.npmjs.com/):
```npm
npm install --save sbtech-sports-api
```

## Usage

After you have obtained your JWT Token from SBTech, insert it in the following manner: 

```js
import {Observable, ApiConfig} from 'sbtech-sports-api'

let getToken = () => { return "JWT_token" }

let onNext = (update) => { /* handle update */}
let onError = (error) => { /* handle error */}

const apiUrl = "http://sportsapi.sbtech.com/sportsapi/api"
const pushApiUrl = "http://sportsapi.sbtech.com/sportsapi/signalr"
//apiUrl and pushApiUrl is optional parameters
const config = ApiConfig.create(getToken, apiUrl, pushApiUrl)

let observer = Observable.fromQuery(config, "odata_query")
                         .subscribe(onNext, onError)
```
If you want to unsubscribe call the following function:
```js
observer.unsubscribe()
```