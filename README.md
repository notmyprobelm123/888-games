<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <title>Blade Crentral</title>

  <!-- Font Awesome CDN -->
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.0/css/all.min.css">

  <!-- Style -->
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    html, body {
      height: 100%;
      font-family: 'Poppins', sans-serif;
      background-color: #1c1f2b;
      overflow-x: hidden;
      scroll-behavior: smooth;
    }

    body {
      display: flex;
    }

    /* Particles background */
    #particles-js {
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      z-index: 0;
    }

    /* Sidebar */
    .sidebar {
      width: 60px;
      background: rgba(25, 28, 39, 0.95);
      display: flex;
      flex-direction: column;
      align-items: center;
      padding-top: 20px;
      position: fixed;
      height: 100%;
      border-right: 1px solid #2a2d3a;
      z-index: 2;
    }

    .sidebar .icon {
      font-size: 24px;
      margin: 20px 0;
      color: #b0b4d2;
      text-decoration: none;
      transition: transform 0.3s, color 0.3s;
    }

    .sidebar .icon:hover {
      color: #ffffff;
      transform: scale(1.2);
    }

    /* Main content */
    main {
      margin-left: 80px;
      padding: 40px 20px;
      width: 100%;
      min-height: 100vh;
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      position: relative;
      z-index: 1;
      opacity: 0;
      animation: fadeInPage 1s forwards;
    }

    h1 {
      font-size: 48px;
      margin-bottom: 20px;
      animation: fadeDown 1.2s ease;
      color: #b0b4d2;
    }

    .search-bar {
      margin: 20px 0;
      animation: fadeDown 1.5s ease;
    }

    .search-bar input {
      background: none;
      border: 1px solid #b0b4d2;
      border-radius: 25px;
      padding: 10px 20px;
      color: #b0b4d2;
      font-size: 16px;
      width: 300px;
      outline: none;
      transition: border-color 0.3s;
    }

    .search-bar input:focus {
      border-color: #ffffff;
    }

    /* Animations */
    @keyframes fadeInPage {
      to {
        opacity: 1;
      }
    }

    @keyframes fadeDown {
      0% {
        opacity: 0;
        transform: translateY(-20px);
      }
      100% {
        opacity: 1;
        transform: translateY(0);
      }
    }

    /* Responsive */
    @media (max-width: 600px) {
      h1 {
        font-size: 32px;
      }
      .search-bar input {
        width: 80%;
      }
    }
  </style>

</head>

<body>

  <!-- Particles Background -->
  <div id="particles-js"></div>

  <!-- Sidebar -->
  <nav class="sidebar">
    <a href="index.html" class="icon" title="Home"><i class="fas fa-home"></i></a>
    <a href="games.html" class="icon" title="Games"><i class="fas fa-gamepad"></i></a>
    <a href="#" class="icon" title="Settings"><i class="fas fa-cog"></i></a>
  </nav>

  <!-- Main Content -->
  <main>
    <h1>Solo Central</h1>
    <div class="search-bar">
      <input type="text" placeholder="Search or enter an URL...">
    </div>
  </main>

  <!-- Scripts -->
  <!-- Particles.js from CDN -->
  <script src="https://cdn.jsdelivr.net/npm/particles.js@2.0.0/particles.min.js"></script>
  <script>
    particlesJS('particles-js', {
      "particles": {
        "number": {
          "value": 80,
          "density": {
            "enable": true,
            "value_area": 800
          }
        },
        "color": {
          "value": "#b0b4d2"
        },
        "shape": {
          "type": "circle"
        },
        "opacity": {
          "value": 0.5,
          "random": true
        },
        "size": {
          "value": 3,
          "random": true
        },
        "move": {
          "enable": true,
          "speed": 1.5
        }
      },
      "interactivity": {
        "events": {
          "onhover": {
            "enable": true,
            "mode": "grab"
          }
        }
      }
    });
  </script>

</body>
</html>
