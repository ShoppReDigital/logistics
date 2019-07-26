# ShoppRe Logistics
Shipping API for Indians

If you are facing any issues. [please create here](https://github.com/shoppre/logistics/issues)


Method:  get request

Url: https://courier.shoppre.com/api/pricing

Parameters: 
All = true
Country = US (country code ISO2) 
Type = nondoc / doc
Weight = 0.5 

Optional parameters:
Length = 
Width =
Height =
Scale =  cm / in
Unit = kg / lb

Note: 
Price you can get upto 70kg
    2. Type you can send “doc” and “nondoc” both have different rates
	Doc    -> means Documents
	NonDoc -> Means Non Documents
    3. Optional parameters is for volumetric weights
	

Example with out volumetric weights:

https://logistics.shoppre.com/api/pricing?all=true&country=US&type=nondoc&weight=0.5


Example with volumetric weights:

https://logistics.shoppre.com/api/pricing?all=true&country=US&type=nondoc&weight=0.5&length=0.5&width=0.5&height=0.5&scale=cm&unit=kg


