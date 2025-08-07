# html-expp-1.1

<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Student Registration Form</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      background: linear-gradient(to right, #74ebd5, #acb6e5);
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
      margin: 0;
    }

    .form-container {
      background-color: #ffffff;
      padding: 30px 40px;
      border-radius: 15px;
      box-shadow: 0 8px 16px rgba(0, 0, 0, 0.2);
      max-width: 400px;
      width: 100%;
    }

    .form-container h2 {
      text-align: center;
      margin-bottom: 20px;
      color: #333;
    }

    .form-group {
      margin-bottom: 15px;
    }

    .form-group label {
      display: block;
      margin-bottom: 5px;
      color: #555;
      font-weight: bold;
    }

    .form-group input {
      width: 100%;
      padding: 10px;
      border: 2px solid #ccc;
      border-radius: 8px;
      font-size: 16px;
    }

    .form-group input:focus {
      border-color: #4a90e2;
      outline: none;
    }

    .submit-btn {
      width: 100%;
      padding: 12px;
      background-color: #4a90e2;
      color: white;
      border: none;
      border-radius: 8px;
      font-size: 18px;
      cursor: pointer;
      transition: background-color 0.3s ease;
    }

    .submit-btn:hover {
      background-color: #357abd;
    }
  </style>
</head>
<body>

  <div class="form-container">
    <h2>Student Registration</h2>
    <form>
      <div class="form-group">
        <label for="name">Full Name:</label>
        <input type="text" id="name" name="name" required pattern="[A-Za-z\s]{3,}" title="Please enter at least 3 alphabetic characters">
      </div>

      <div class="form-group">
        <label for="email">Email Address:</label>
        <input type="email" id="email" name="email" required placeholder="example@domain.com">
      </div>

      <div class="form-group">
        <label for="age">Age:</label>
        <input type="number" id="age" name="age" required min="5" max="100" title="Enter a valid age between 5 and 100">
      </div>

      <button type="submit" class="submit-btn">Register</button>
    </form>
  </div>

</body>
</html>


# expp1.2

<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Banking UI</title>
  <style>
    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
    }

    body {
      height: 100vh;
      display: flex;
      justify-content: center;
      align-items: center;
      background-color: #f4f4f4;
      font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    }

    .card {
      background: #fff;
      padding: 30px 40px;
      border-radius: 15px;
      box-shadow: 0 5px 20px rgba(0, 0, 0, 0.1);
      text-align: center;
      width: 90%;
      max-width: 350px;
    }

    .balance {
      font-size: 2rem;
      color: green;
      margin-bottom: 30px;
    }

    .btn {
      display: block;
      width: 100%;
      padding: 12px;
      margin-bottom: 15px;
      font-size: 1rem;
      border: none;
      border-radius: 8px;
      cursor: pointer;
      transition: transform 0.2s ease;
    }

    .btn:active {
      transform: scale(0.98);
    }

    .deposit {
      background-color: #28a745;
      color: white;
    }

    .withdraw {
      background-color: #dc3545;
      color: white;
    }
    
  </style>
</head>
<body>

  <div class="card">
    <div class="balance">$0</div>
    <button class="btn deposit">Deposit</button>
    <button class="btn withdraw">Withdraw</button>
  </div>

</body>
</html>

# expp3

<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Admin Dashboard</title>
  <style>
    :root {
      --bg-color: #ffffff;
      --text-color: #000000;
      --header-footer-bg: #4CAF50;
      --sidebar-bg: #f2f2f2;
      --link-color: purple;
    }

    body.dark-mode {
      --bg-color: #121212;
      --text-color: #f0f0f0;
      --header-footer-bg: #222;
      --sidebar-bg: #333;
      --link-color: #8888ff;
    }

    body {
      margin: 0;
      font-family: Arial, sans-serif;
      background-color: var(--bg-color);
      color: var(--text-color);
      display: grid;
      grid-template-areas: 
        "header header"
        "sidebar main"
        "footer footer";
      grid-template-columns: 200px 1fr;
      grid-template-rows: 60px 1fr 40px;
      height: 100vh;
    }

    header {
      grid-area: header;
      background-color: var(--header-footer-bg);
      color: white;
      display: flex;
      justify-content: space-between;
      align-items: center;
      padding: 0 20px;
    }

    header h1 {
      font-size: 20px;
    }

    .theme-toggle {
      display: flex;
      align-items: center;
      gap: 5px;
      color: white;
    }

    aside {
      grid-area: sidebar;
      background-color: var(--sidebar-bg);
      padding: 20px;
    }

    aside ul {
      list-style-type: disc;
      padding-left: 20px;
    }

    aside ul li a {
      text-decoration: none;
      color: var(--link-color);
    }

    main {
      grid-area: main;
      padding: 20px;
    }

    footer {
      grid-area: footer;
      background-color: var(--header-footer-bg);
      color: white;
      text-align: center;
      line-height: 40px;
    }
  </style>
</head>
<body>

  <header>
    <h1>Admin Dashboard</h1>
    <div class="theme-toggle">
      <label for="toggle">Dark Mode</label>
      <input type="checkbox" id="toggle">
    </div>
  </header>

  <aside>
    <ul>
      <li><a href="#">Home</a></li>
      <li><a href="#">Users</a></li>
      <li><a href="#">Settings</a></li>
    </ul>
  </aside>

  <main>
    <h2>Welcome, Admin!</h2>
    <p>This is the main content area. Add charts, tables, or reports here.</p>
  </main>

  <footer>
    © 2025 Admin Panel
  </footer>

  <script>
    const toggle = document.getElementById('toggle');
    toggle.addEventListener('change', () => {
      document.body.classList.toggle('dark-mode');
    });
  </script>

</body>
</html>
