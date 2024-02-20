<!DOCTYPE html>
<html lang="ro">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Produse de calitate superioară</title>
    <script type="module" src="https://unpkg.com/@google/model-viewer"></script>
    <style>
        body {
            margin: 0;
            padding: 0;
            font-family: Arial, sans-serif;
            background: linear-gradient(135deg, #6effa3 0%, #00bcd4 100%);
            height: 100vh;
        }
        model-viewer {
            width: 100%;
            height: 300px;
        }
        .navigation {
            display: flex;
            justify-content: space-between;
            margin-top: 20px;
            padding: 0 20px;
        }
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
        }
        .content {
            max-width: 800px;
            margin: auto;
            padding: 20px;
            background: white; /* Optional: pentru a face conținutul mai lizibil pe fundalul gradient */
            border-radius: 8px; /* Optional: adaugă rotunjire la colțurile containerului de conținut */
            box-shadow: 0 4px 8px rgba(0,0,0,0.1); /* Optional: adaugă o umbră ușoară pentru un efect 3D subtil */
        }
    </style>
</head>
<body>

<div class="content">
    <h2 style="text-align: center;"><a id="mainTitle" href="#" target="_blank">Titlu Produs</a></h2>
    <div class="model-and-navigation">
        <h3 id="subtitle">Subtitlu Produs</h3>
        <model-viewer id="modelViewer" src="Avatar4.glb" ios-src="Avatar4.usdz" ar ar-modes="webxr scene-viewer quick-look" camera-controls auto-rotate environment-image="neutral" shadow-intensity="1" alt="Produs">
            <button slot="ar-button" class="ar-button">
                <span class="levitate">👋</span> Activează modul AR
            </button>
        </model-viewer>
        <div class="navigation">
            <button type="button" class="nav-button" onclick="changeModel(-1)">⇦ prev</button>
            <button type="button" class="nav-button" onclick="changeModel(1)">next ⇨</button>
        </div>
    </div>
</div>

<script>
    // Script-ul JavaScript rămâne neschimbat.
</script>

</body>
</html>
