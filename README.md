# Day-04


Lodash isEqual() method is the best way to compare two JSON object.

This will not consider the order of the keys in object and check for the equality of object. Example

const object1 = {
  name: 'Person1',
  age: '5'
};
    
const object2 = {
  age: '5',
  name: 'Person1'
};
    
JSON.stringify(object1) === JSON.stringify(object2)
// false
    
_.isEqual(object1, object2)
// true


console.log("file executed");

//create obj which is capable of making an API call
const request = new XMLHttpRequest ();

// Open the connect to API with HTTP mrthod & url
request.open("GET" , "https://raw.githubusercontent.com/rvsp/restcountries-json-data/master/res-countries.json");

// Send the request to the server
request.send();

// Parse the text passed on to the server
request.onload = function () {
  var response = JSON.parse(request.response);
  console.log(response);
  for(var i=0;i<response.length;i++)
  {
  console.log(response[i].name," ",response[i].capital);
}
};

