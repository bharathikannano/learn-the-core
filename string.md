# Anagrams

```javascript
function anagrams(a, b) {
  let i = 0;
  let sumA = 0;
  let sumB = 0;
  //Convert given string to lowercase
  a = a.replace(/[\W]/g, "").toLowerCase();
  b = b.replace(/[\W]/g, "").toLowerCase();
  
  if (a.length !== b.length) return false;    // Check the length as base condition 
  
  !(function sumCharCode() {
  
    if (i < a.length) {                 // iteration based on string length.
      sumA += a.charCodeAt(i);          // char code number addition  of each character 
      sumB += b.charCodeAt(i);
      i++;
      sumCharCode();        //recursive function call
    }
  })()
  return sumA === sumB;
}

console.log(anagrams("listen", "silent"));   // true

```
