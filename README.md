# Sepagar-Mockup
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>QR Code for Table</title>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/qrcodejs/1.0.0/qrcode.min.js"></script>
    <style>
        body {
            font-family: Arial, sans-serif;
            text-align: center;
            margin-top: 50px;
        }
        #qrcode {
            margin: 20px;
        }
    </style>
</head>
<body>
    <h1>Escanea el código QR para ver la orden de la mesa</h1>
    <div id="qrcode"></div>

    <script>
        // Aquí generarás el QR dinámicamente, por ejemplo, con un link único por mesa.
        let tableId = 1;  // Este será el ID de la mesa, puedes cambiarlo dinámicamente.
        let orderURL = `https://tuservidor.com/order?table=${tableId}`;

        // Crear el QR usando la librería
        var qrcode = new QRCode(document.getElementById("qrcode"), {
            text: orderURL,
            width: 256,
            height: 256
        });

        console.log("QR generado para la URL: " + orderURL);
    </script>
</body>
</html>
