# ShoppRe Logistics
Shipping API for Indians

If you are facing any issues. [please create here](https://github.com/shoppre/logistics/issues)


### Usage HTTP:

URL: : `https://logistics.shoppre.com/api/pricing`

METHOD: `GET`

Query Parameters: `all=true&country=US&type=nondoc&weight=0.5`


### Usage PHP:
```php
function getPricing(){
  // Set Logistics endpoint
  $url = 'https://logistics.shoppre.com/api/pricing?all=true&country=US&type=nondoc&weight=0.5';
  
  $ch = curl_init();

  // Set the url, number of POST vars, POST data
  curl_setopt($ch, CURLOPT_URL, $url);
  curl_setopt($ch, CURLOPT_GET, true);
  curl_setopt($ch, CURLOPT_RETURNTRANSFER, true);

  curl_setopt($ch, CURLOPT_SSL_VERIFYPEER, false);                                    

  // Execute post
  $result = curl_exec($ch);
  if ($result === FALSE) {
      die('pricing get failed in curl: ' . curl_error($ch));
  } else {
	  
  }

  // Close connection
  curl_close($ch);
}
```

### Usage in NodeJS

`npm install --save request`

 ```js
   var request = require('request');
   var options = {
           url: "https://logistics.shoppre.com/api/pricing?all=true&country=US&type=nondoc&weight=0.5",
           json:true,
         };
    // Sending GET Request to Logistics API
    request(options, function (error, response, body) {
      if (error) { return handleError(res, err); }
      res.json({
        message: 'success',
        data: body
      });
    });     
 
 ```
 



