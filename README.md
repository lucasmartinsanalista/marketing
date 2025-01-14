<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Landing Page</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
        }

        .container {
            width: 100%;
            max-width: 1200px;
            margin: 0 auto;
            padding: 20px;
        }

        .layer {
            margin-bottom: 40px;
        }

        .layer img {
            max-width: 100%;
            height: auto;
            display: block;
        }

        .header {
            text-align: center;
            background-color: #f4f4f4;
            padding: 20px;
        }

        .header h1 {
            margin: 0;
            color: #333;
        }

        .client-feedback {
            display: flex;
            gap: 20px;
            justify-content: space-between;
        }

        .feedback-item {
            text-align: center;
            flex: 1;
        }

        iframe {
            width: 100%;
            height: 500px;
            border: none;
        }

        form {
            display: flex;
            flex-direction: column;
            gap: 15px;
        }

        form input, form textarea, form button {
            width: 100%;
            padding: 10px;
            border: 1px solid #ccc;
            border-radius: 5px;
            font-size: 16px;
        }

        form button {
            background-color: #28a745;
            color: white;
            cursor: pointer;
            border: none;
        }

        form button:hover {
            background-color: #218838;
        }

        #map {
            width: 100%;
            height: 400px;
        }
    </style>
</head>
<body>

    <div class="container">

        <!-- 1ª Camada -->
        <div class="layer header">
            <h1>Tenha Resultados Imediatos com Gestão de Tráfego</h1>
            <img src="foto1.png" alt="Imagem de Gestão de Tráfego">
        </div>

        <!-- 2ª Camada -->
        <div class="layer client-feedback">
            <div class="feedback-item">
                <img src="foto2.png" alt="Foto Cliente 1">
                <p>"Ótimo serviço! Tivemos um crescimento incrível."</p>
            </div>
            <div class="feedback-item">
                <img src="foto3.png" alt="Foto Cliente 2">
                <p>"Resultados acima do esperado. Recomendo!"</p>
            </div>
            <div class="feedback-item">
                <img src="foto4.png" alt="Foto Cliente 3">
                <p>"Estratégias que realmente funcionam. Muito obrigado!"</p>
            </div>
        </div>

        <!-- 3ª Camada -->
        <div class="layer">
            <iframe src="https://www.youtube.com/embed/bJoi2G15QpA?autoplay=1&mute=0" allow="autoplay"></iframe>
        </div>

        <!-- 4ª Camada -->
        <div class="layer">
            <form>
                <input type="text" name="name" placeholder="Seu Nome" required>
                <input type="email" name="email" placeholder="Seu Email" required>
                <textarea name="message" placeholder="Sua Mensagem" rows="5" required></textarea>
                <button type="submit">Enviar</button>
            </form>
        </div>

        <!-- 5ª Camada -->
        <div class="layer">
            <div id="map"></div>
        </div>

    </div>

    <script>
        function initMap() {
            const location = { lat: -19.9766, lng: -44.1986 }; // Coordenadas do Parque das Cachoeiras Cristais
            const map = new google.maps.Map(document.getElementById("map"), {
                zoom: 15,
                center: location,
            });
            const marker = new google.maps.Marker({
                position: location,
                map: map,
            });
        }
    </script>
    <script src="https://maps.googleapis.com/maps/api/js?key=YOUR_API_KEY&callback=initMap" async defer></script>

</body>
</html>
