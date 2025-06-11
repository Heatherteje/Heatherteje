<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Birthday Greeting</title>
  <style>
    body {
      text-align: center;
      font-family: Arial, sans-serif;
      padding-top: 100px;
      background: #f7e1ff;
    }
    h1 {
      font-size: 3em;
      color: #8e44ad;
    }
    .cake {
      font-size: 4em;
      margin: 20px 0;
    }
  </style>
</head>
<body>
  <div class="cake">🎂</div>
  <h1 id="greeting">Happy Birthday!</h1>
  <script>
    // Get the name from the URL query (?name=Alice)
    const params = new URLSearchParams(window.location.search);
    const name = params.get('name');
    const greeting = document.getElementById('greeting');
    if (name) {
      greeting.textContent = `Happy Birthday, ${decodeURIComponent(name)}!`;
    }
  </script>
</body>
</html>
