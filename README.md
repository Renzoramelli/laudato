<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Calculadora de Equilibrio</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            background-color: #f4f4f4;
        }
        .container {
            background-color: #fff;
            padding: 20px;
            border-radius: 8px;
            box-shadow: 0 0 10px rgba(0,0,0,0.1);
            text-align: center;
        }
        input[type="number"] {
            width: 100%;
            padding: 10px;
            margin: 10px 0;
            border: 1px solid #ccc;
            border-radius: 4px;
        }
        button {
            padding: 10px 20px;
            background-color: #4CAF50;
            color: #fff;
            border: none;
            border-radius: 4px;
            cursor: pointer;
        }
        button:hover {
            background-color: #45a049;
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>Calculadora de Equilibrio</h1>
        <input type="number" id="ambiente" placeholder="Valor para Ambiente" required>
        <input type="number" id="social" placeholder="Valor para Social" required>
        <input type="number" id="economia" placeholder="Valor para Economía" required>
        <button onclick="calcularEquilibrio()">Calcular Equilibrio</button>
        <h2 id="resultado"></h2>
    </div>

    <script>
        function calcularEquilibrio() {
            var ambiente = parseFloat(document.getElementById('ambiente').value);
            var social = parseFloat(document.getElementById('social').value);
            var economia = parseFloat(document.getElementById('economia').value);
            var equilibrio = (ambiente + social + economia) / 3;
            document.getElementById('resultado').innerText = "El equilibrio es: " + equilibrio.toFixed(2);
        }
    </script>
</body>
</html>
