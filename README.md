<!DOCTYPE html>
<html lang="uk">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Marker.ua - Маркування електрощитків</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #e6f7ff;
            color: #003366;
            margin: 0;
            padding: 0;
            text-align: center;
        }
        .container {
            width: 80%;
            max-width: 800px;
            margin: 50px auto;
            background-color: white;
            padding: 20px;
            border-radius: 10px;
            box-shadow: 0px 0px 15px rgba(0, 51, 102, 0.5);
        }
        h1 {
            color: #002244;
        }
        select, button {
            width: 100%;
            padding: 10px;
            margin: 10px 0;
            border: 1px solid #003366;
            border-radius: 5px;
        }
        button {
            background-color: #003366;
            color: white;
            font-size: 16px;
            cursor: pointer;
        }
        button:hover {
            background-color: #0055b3;
        }
        .payment-section {
            margin-top: 20px;
        }
        .hidden {
            display: none;
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>Marker.ua - Маркування електрощитків</h1>
        
        <label for="manufacturer">Виберіть виробника автоматики:</label>
        <select id="manufacturer">
            <option value="Schneider">Schneider Electric</option>
            <option value="Siemens">Siemens</option>
            <option value="ABB">ABB</option>
            <option value="Eaton">Eaton</option>
        </select>
        
        <label for="labelColor">Виберіть колір наклейки:</label>
        <select id="labelColor">
            <option value="Червоний">Червоний</option>
            <option value="Синій">Синій</option>
            <option value="Зелений">Зелений</option>
            <option value="Жовтий">Жовтий</option>
        </select>
        
        <button onclick="orderLabel()">Замовити</button>

        <div class="payment-section hidden" id="paymentSection">
            <h2>Оплата</h2>
            <p>Сайт поки що безкоштовний, але в майбутньому тут буде можливість оплатити замовлення.</p>
        </div>
    </div>

    <script>
        function orderLabel() {
            const manufacturer = document.getElementById('manufacturer').value;
            const labelColor = document.getElementById('labelColor').value;
            alert(`Ви обрали: ${manufacturer}, колір наклейки: ${labelColor}`);
            document.getElementById('paymentSection').classList.remove('hidden');
        }
    </script>
</body>
</html>
