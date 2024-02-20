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
        }
    </style>
</head>
<body>

<div class="content">
    <h2 style="text-align: center;"><a id="mainTitle" href="#" target="_blank">Titlu Produs</a></h2>
    <div class="model-and-navigation">
        <h3 id="subtitle">Subtitlu Produs</h3>
        <model-viewer 
            id="modelViewer" 
            src="Avatar4.glb" 
            ios-src="Avatar4.usdz" 
            ar 
            ar-modes="webxr scene-viewer quick-look" 
            camera-controls 
            auto-rotate 
            environment-image="neutral" 
            shadow-intensity="1" 
            alt="Produs"
            min-camera-orbit="auto 45deg 0deg" 
            max-camera-orbit="auto 105deg auto">
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
    const models = [
        { file: "jordan.glb", iosFile: "jordan.usdz", title: "Cumpără acum Air Jordan 4 Retro", url: "https://unfazed.ro/products/air-jordan-4-retro-se-craft-medium-olive", subtitle: "Air Jordan 4 Retro SE Craft \"Medium Olive\"", features: "" },
        { file: "Adidas.glb", iosFile: "Adidas.usdz", title: "Cumpără acum Adidas Samba OG", url: "https://unfazed.ro/products/adidas-samba-og-cloud-white?_pos=1&_sid=6d480c095&_ss=r", subtitle: "Adidas Samba OG \"Cloud White\"", features: "" },
        { file: "nike.glb", iosFile: "nike.usdz", title: "Cumpără acum Nike Air Force 1", url: "https://unfazed.ro/products/nike-air-force-1-low-triple-white", subtitle: "Nike Air Force 1 Low \"Triple White\"", features: "" }
    ];
    let currentIndex = 0;

    function changeModel(step) {
        currentIndex += step;

        if (currentIndex >= models.length) {
            currentIndex = 0;
        } else if (currentIndex < 0) {
            currentIndex = models.length - 1;
        }

        updateModel();
    }

    function updateModel() {
        const model = models[currentIndex];
        const viewer = document.getElementById('modelViewer');
        const titleElement = document.getElementById('mainTitle');
        const subtitleElement = document.getElementById('subtitle');

        viewer.src = model.file;
        viewer.setAttribute('ios-src', model.iosFile);
        viewer.alt = model.subtitle;
        titleElement.href = model.url;
        titleElement.textContent = model.title;
        subtitleElement.textContent = model.subtitle;
    }

    updateModel();
</script>

</body>
</html>
