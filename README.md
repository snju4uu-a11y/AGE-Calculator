# AGE-Calculator
Free AGE Calculator to check you age right now


<div class="comment-link">
  Want to check ipl ticket price? <a href="https://iplmatchticketsprice.in/" target="_blank" rel="noopener">Click here</a> to join now!
</div>

https://thewhatspgrouplinks.com/

<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Age Calculator</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      background: linear-gradient(120deg, #74ebd5, #acb6e5);
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      height: 100vh;
      margin: 0;
    }

    .container {
      background: white;
      padding: 2em;
      border-radius: 10px;
      box-shadow: 0 4px 20px rgba(0, 0, 0, 0.1);
      text-align: center;
      max-width: 350px;
      width: 90%;
    }

    input[type="date"] {
      padding: 0.5em;
      margin: 1em 0;
      border: 1px solid #ccc;
      border-radius: 5px;
      width: 100%;
    }

    button {
      background-color: #4caf50;
      color: white;
      border: none;
      padding: 0.7em 1.5em;
      border-radius: 5px;
      cursor: pointer;
      width: 100%;
    }

    button:hover {
      background-color: #45a049;
    }

    #result {
      margin-top: 1.5em;
      font-size: 1.2em;
      color: #333;
    }

    footer {
      margin-top: 2em;
      font-size: 0.9em;
      color: #444;
      text-align: center;
    }

    footer a {
      color: #0077cc;
      text-decoration: none;
      font-weight: bold;
    }

    footer a:hover {
      text-decoration: underline;
    }
  </style>
</head>
<body>
  <div class="container">
    <h1>Age Calculator</h1>
    <p>Enter your date of birth:</p>
    <input type="date" id="dob" />
    <button onclick="calculateAge()">Calculate Age</button>

    <div id="result"></div>

    <footer>
      <p>
        <a href="https://thewhatspgrouplinks.com/" target="_blank" rel="dofollow">
          Join Group
        </a>
      </p>
    </footer>
  </div>

  <script>
    function calculateAge() {
      const dobInput = document.getElementById("dob").value;
      const result = document.getElementById("result");

      if (!dobInput) {
        result.textContent = "Please select your date of birth.";
        return;
      }

      const dob = new Date(dobInput);
      const today = new Date();

      let ageYears = today.getFullYear() - dob.getFullYear();
      let ageMonths = today.getMonth() - dob.getMonth();
      let ageDays = today.getDate() - dob.getDate();

      if (ageDays < 0) {
        ageMonths--;
        const prevMonth = new Date(today.getFullYear(), today.getMonth(), 0);
        ageDays += prevMonth.getDate();
      }

      if (ageMonths < 0) {
        ageYears--;
        ageMonths += 12;
      }

      result.innerHTML = `
        You are <strong>${ageYears}</strong> years,
        <strong>${ageMonths}</strong> months, and
        <strong>${ageDays}</strong> days old.
      `;
    }
  </script>
</body>
</html>
