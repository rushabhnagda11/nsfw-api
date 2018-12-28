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

`curl --request POST --url 'https://app.nanonets.com/api/v2/ImageCategorization/LabelUrls/' --header 'accept: application/x-www-form-urlencoded' -d 'modelId=7390a500-9fe1-483b-8123-750b96fc660c&urls=https://goo.gl/ICoiHc' -u '-EKLduz8hPIkw3GoVNalgIznrrSHkiMai66KaTWKi-e:'`

Get your API key by signing up on app.nanonets.com
