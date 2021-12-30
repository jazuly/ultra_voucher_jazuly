#Ultra Voucher Test Jazuly

### Logic Test Anagram Online Script
[JSFiddle](https://jsfiddle.net/dhntumL9/)
```js
const arr = ['cook', 'save', 'taste', 'aves', 'vase', 'state', 'map'];
let final = {};
let cIndex = 0;
let fin2 = [];

arr.forEach((kata, index) => {
  const katass = kata.toLowerCase().split("").sort().join("");
  
  if (final[katass] && final[katass].data.length > 0) {
    final[katass].data.push(arr[index])
  } else {
    final[katass] = { index: cIndex, data: [arr[index]] };
    cIndex++
  }
});

for (const key in final) {
    fin2[final[key].index] = final[key].data
}

console.log(fin2)
```

### Query Test 
[DBFiddle](https://www.db-fiddle.com/f/bHRNN9PXNAZBkCWx7qnQTq/1)
```sql
SELECT u1.id, u1.nama, (
	SELECT nama FROM users WHERE id = u1.parent_id
) AS parent_name
FROM users u1
```
