# Write a method that creates an array of unique values that are included in all given arrays
Expected Result: ([1, 2], [2, 3]) => [2]

```
const arr1 = [1, 2, 1, 2, 1, 2];
const arr2 = [2, 3];
const arr3 = ["a", "b"];
const arr4 = ["b", "c"];
const arr5 = ["b", "e", "c"];
const arr6 = ["b", "b", "e"];
const arr7 = ["b", "c", "e"];
const arr8 = ["b", "e", "c"];

const intersection = (...arrays) => {
  var data = [...arrays];
  var result = data.reduce((a, b) => a.filter((c) => b.includes(c)));
  return [...new Set(result)];
};

console.log(intersection(arr1, arr2)); // [2]
console.log(intersection(arr3, arr4, arr5)); // ['b']
console.log(intersection(arr5, arr6, arr7, arr8)); // ['b', 'e']
```
