<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Connect via NinjaOne ID</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      text-align: center;
      margin-top: 100px;
    }
    input {
      padding: 10px;
      font-size: 16px;
      width: 250px;
    }
    button {
      padding: 10px 20px;
      font-size: 16px;
      margin-left: 10px;
      cursor: pointer;
    }
  </style>
</head>
<body>
  <h2>Enter NinjaOne Connect ID</h2>
  <input type="text" id="ninjaId" placeholder="e.g. 8589921711">
  <button onclick="goToNinja()">Connect</button>

  <script>
    function goToNinja() {
      const id = document.getElementById('ninjaId').value.trim();
      if (/^\d+$/.test(id)) {
        const url = `https://eu.ninjarmm.com/connect/#/${id}`;
        window.location.href = url;
      } else {
        alert("Please enter a valid numeric ID.");
      }
    }
  </script>
</body>
</html>
