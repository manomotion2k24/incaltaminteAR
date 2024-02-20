<!DOCTYPE html>
<html lang="ro">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Produse de calitate superioară</title>
  <script type="module" src="https://unpkg.com/@google/model-viewer"></script>
  <style>
    body {
      background: linear-gradient(to right, #f2f5f7, #fff);
      height: 100vh;
      width: 100vw;
      margin: 0;
      padding: 0;
      font-family: Arial, sans-serif;
    }

    /* Font mai decorativ pentru titlu */
    h2 {
      font-family: "Lora", serif;
      font-size: 24px;
      margin-bottom: 10px;
    }

    /* Margini si padding ajustate */
    .content {
      max-width: 800px;
      margin: auto;
      padding: 40px 20px;
    }

    /* Butoane de navigare cu hover si bordura */
    .nav-button {
      cursor: pointer;
      background-color: #007BFF;
      border: none;
      border-radius: 20px;
      padding: 10px 20px;
      font-size: 16px;
      color: white;
      box-shadow: 0 2px 4px rgba(0, 0, 0, 0.2);
      transition: background-color 0.3s, box-shadow 0.3s;
    }

    .nav-button:hover {
      background-color: #0056b3;
      box-shadow: 0 4px 8px rgba(0, 0, 0, 0.3);
      border: 1px solid #0056b3;
    }

    /* Preloader */
    .loader {
      position: absolute;
      top: 50%;
      left: 50%;
      transform: translate(-50%, -50%);
      width: 100px;
      height: 100px;
      border: 10px solid #f3f3f3;
      border-radius: 50%;
      border-top-color: #3498db;
      animation: rotate 2s linear infinite;
    }

    @keyframes rotate {
      100% {
        transform: translate(-50%, -50%) rotate(360deg);
      }
    }

    /* Media queries pentru responsive design */
    @media only screen and (max-width: 768px) {
      .content {
        padding: 20px;
      }

      .model-and-navigation {
        flex-direction: column;
        align-items: center;
      }
    }
  </style>
</head>
<body>

<div class="content">
  <h2><a id="mainTitle" href="#" target="_blank">Titlu Produs</a></h2>

  <div class="loader"></div>

  <div class="model-and-navigation">
    <h3>Subtitlu Produs</h3>
    <model-viewer id="modelViewer" src="Avatar4.glb" ios-src="Avatar4.usdz" ar ar-modes="webxr scene-viewer quick-look" camera-controls auto-rotate environment-image="neutral" shadow-intensity="1" alt="Produs">
      <button slot="ar-button" class="ar-button">
        <span class="levitate"></span> Activează modul AR
      </button>
    </model-viewer>
    <div class="navigation">
      <button type="button" class="nav-button" onclick="changeModel(-1)">⇦ prev</button>
      <button type="button" class="nav-button" onclick="changeModel(1)">next ⇨</button>
    </div>
  </div>

</div>

<script>
  const models = [
    { file: "jordan.glb", iosFile: "
