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
