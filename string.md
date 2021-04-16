# Anagrams

```javascript
function anagrams(a, b) {
  let i = 0
  let sumA = 0
  let sumB = 0
  a = a.replace(/[\W]/g, "").toLowerCase()
  b = b.replace(/[\W]/g, "").toLowerCase()
  if (a.length !== b.length) return false
  !(function sumCharCode() {
    if (i < a.length) {
      sumA += a.charCodeAt(i)
      sumB += b.charCodeAt(i)
      i++
      sumCharCode()
    }
  })()
  return sumA === sumB;
}

console.log(anagrams("listen", "silent"))

```
