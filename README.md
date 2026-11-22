<!DOCTYPE html>
<html>
<head>
  <title>Release Readiness</title>
  <style>
    body { font-family: Arial; background: #f8fafc; padding: 40px; }
    .card { background: white; padding: 20px; border-radius: 8px; max-width: 300px; margin: auto; }
    label { display: block; margin: 8px 0; cursor: pointer; }
  </style>
</head>
<body class="card">
  <h3>Status: <span id="status">In Progress</span></h3>
  <progress id="bar" value="0" max="4"></progress>
  <label><input type="checkbox" onclick="check()"> Code Reviewed</label>
  <label><input type="checkbox" onclick="check()"> Tests Passing</label>
  <label><input type="checkbox" onclick="check()"> Security Clear</label>
  <label><input type="checkbox" onclick="check()"> Docs Updated</label>
  <script>
    function check() { let done = document.querySelectorAll('input:checked').length; document.getElementById('bar').value = done; document.getElementById('status').innerText = done === 4 ? 'Ready' : 'In Progress'; }
  </script>
</body>
</html>
