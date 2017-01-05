# Geocoding-testing
##Overview
Geocoding is the process of converting addresses like "1600 Amphitheatre Parkway, Mountain View, CA" into geographic coordinates like latitude 37.423021 and longitude -122.083739, which you can use to place markers on a map, or position the map.
Reverse geocoding is the process of converting geographic coordinates into a human-readable address. 

In this repository you can find developed test plan for the service. 
```Test plan.xlsx```
###Testing
For the purpose of testing``` postman_collection``` and ```postman_environment``` json files are uploaded. Before you start testing, you should install Postman tool.
```
Download it from : https://www.getpostman.com/ (Windows)
```
After the tool is installed and you are logged in, import attached collection and environment files. To be able to run any of those tests, you should change the value of ```key``` parameter.
```
Get your KEY from : https://developers.google.com/maps/documentation/geocoding/get-api-key
```
###Automated Testing
One of Postman's most powerful features is its ability to run automated tests on your requests. Automated tests for this feature are under folder ```automatedTest``` inside postman_collection. Go to the ```Test``` tab to see script.

There is ability to run whole folder of tests from ```console```. To be able to do that, you should install Newman tool. Here are the steps:
```
Download node.js for your machine from :  https://nodejs.org/en/download/ and install it 
```
```
Add PATH variable : C:\Program Files\Nodejs
```
```
Install Newman globaly: npm install -g newman
```
Open ```cmd``` and move to the folder where you have saved json files. Run automated tests using command :
```
newman -c GoogleGeocoding.postman_collection.json -e GoogleMapTest.postman_environment.json -f automatedTests
```
While tests are running, all information are provided in console in form :

![alt tag](https://github.com/alma1234/Geocoding-testing/blob/master/testDetails.png)

After all tests are rund, summary results are presented.

![alt tag](https://github.com/alma1234/Geocoding-testing/blob/master/summary.png)

User is able to save all results as html file. Add next command at the end of the previous one.
```
-H results.html
```
