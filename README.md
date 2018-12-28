<div align="center">
  <a href="https://nanonets.com/objectdetection/">
    <img src="https://nanonets.com/logo.png" alt="NanoNets Object Detection Python Sample" width="100"/>
    </a>
</div>

<h1 align="center">Nanonets NSFW API</h1>

<a href="https://nanonets.com/content-moderation-api/"> <h3>Live demo</h3> </a>

| [Golang Sample](https://repl.it/@RushabhNagda/go-example-url) | [Python Sample](https://repl.it/@RushabhNagda/go-example-url)| [Node.js Sample](https://repl.it/@RushabhNagda/go-example-url) |
| -------------------------- |--------------------------|--------------------------|
| [![](https://www.hugopicado.com/assets/golang.png)](https://github.com/NanoNets/object-detection-sample-golang) | [![](http://kata.coderdojo.com/images/thumb/e/ea/Python_logo.png/100px-Python_logo.png)](https://github.com/NanoNets/object-detection-sample-python) | [![](https://s3.amazonaws.com/openshift-hub/production/quickstarts/243/nodejs_custom.png?1456926624)](https://github.com/NanoNets/object-detection-sample-nodejs) |

** **

## Usage



We're classifying images into NSFW and SFW categories.

Following are the image categories we classify into NSFW categories.
* Porn
* Explicit Nudity
* Animated Porn
* Suggestive Nudity
* Gore

### Query pretrained model.

* Get your API key by signing up on app.nanonets.com

#### curl

```
curl --request POST --url 'https://app.nanonets.com/api/v2/ImageCategorization/LabelUrls/' --header 'accept: application/x-www-form-urlencoded' -d 'modelId=7390a500-9fe1-483b-8123-750b96fc660c&urls=https://goo.gl/ICoiHc' -u '-REPLCAE_YOUR_API_KEY:'
```

#### python

```
#REPLACE YOUR API KEY
 
import requests
 
url = 'https://app.nanonets.com/api/v2/ImageCategorization/LabelUrls/'
 
headers = {
  'accept': 'application/x-www-form-urlencoded'
}
 
data = {'modelId': '7390a500-9fe1-483b-8123-750b96fc660c', 'urls' : ['https://goo.gl/ICoiHc']}
 
response = requests.request('POST', url, headers=headers, auth=requests.auth.HTTPBasicAuth('REPLACE_YOUR_API_KEY', ''), data=data)
 
print(response.text)

```

#### node

```
var request = require("request");
  
var options = { method: 'POST',
  url: 'http://app.nanonets.com/api/v2/ImageCategorization/LabelUrls/',
  headers:
  { 'cache-control': 'no-cache',
    Authorization: 'Basic ' + new Buffer('REPLACE YOUR API KEY' + ":" + '').toString("base64"),
    'Content-Type': 'application/x-www-form-urlencoded' },
  form:
  { urls: 'https://goo.gl/ICoiHc',
    modelId: '7390a500-9fe1-483b-8123-750b96fc660c' } };

request(options, function (error, response,body) {
  if (error) throw new Error(error);

  console.log(body);
});
```

#### go

```
//REPLACE YOUR API KEY

package main

import (
  "bytes"
  "fmt"
  "io/ioutil"
  "net/http"
  "net/url"
)

func main() {

  labelUrl := "https://app.nanonets.com/api/v2/ImageCategorization/LabelUrls/"

  data := url.Values{}
  data.Set("modelId", "7390a500-9fe1-483b-8123-750b96fc660c")
  data.Add("urls", "https://goo.gl/ICoiHc")

  req, _ := http.NewRequest("POST", labelUrl, bytes.NewBufferString(data.Encode()))

  req.Header.Add("Content-Type", "application/x-www-form-urlencoded")
  req.SetBasicAuth("-REPLACE_YOUR_API_KEY", "")

  res, _ := http.DefaultClient.Do(req)

  defer res.Body.Close()
  body, _ := ioutil.ReadAll(res.Body)

  fmt.Println(res)
  fmt.Println(string(body))

}

```


