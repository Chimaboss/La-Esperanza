<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Menú - Lonchería La Esperanza</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #f4f4f4;
            margin: 0;
            padding: 20px;
            text-align: center;
        }
        h1 {
            color: #2e7d32;
        }
        .menu-container {
            max-width: 600px;
            margin: 0 auto;
            background-color: #fff;
            padding: 20px;
            border-radius: 10px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
        }
        .menu-item {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 10px;
            border-bottom: 1px solid #eee;
        }
        .menu-item:last-child {
            border-bottom: none;
        }
        .menu-item span {
            font-size: 18px;
        }
        .menu-item input {
            width: 50px;
            padding: 5px;
            font-size: 16px;
        }
        button {
            background-color: #2e7d32;
            color: white;
            padding: 10px 20px;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            margin-top: 20px;
            font-size: 16px;
        }
        button:hover {
            background-color: #1b5e20;
        }
        #pedido-detalle {
            margin-top: 20px;
            text-align: left;
            max-width: 600px;
            margin-left: auto;
            margin-right: auto;
            background-color: #e8f5e9;
            padding: 15px;
            border-radius: 5px;
            display: none;
        }
    </style>
</head>
<body>
    <h1>Lonchería La Esperanza</h1>
    <div class="menu-container">
        <h2>Menú del Día</h2>
        <div class="menu-item">
            <span>Tacos (3 piezas) - $50</span>
            <input type="number" id="tacos" min="0" value="0">
        </div>
        <div class="menu-item">
            <span>Torta de milanesa - $60</span>
            <input type="number" id="torta" min="0" value="0">
        </div>
        <div class="menu-item">
            <span>Enchiladas verdes (4 piezas) - $70</span>
            <input type="number" id="enchiladas" min="0" value="0">
        </div>
        <div class="menu-item">
            <span>Quesadillas (2 piezas) - $40</span>
            <input type="number" id="quesadillas" min="0" value="0">
        </div>
        <div class="menu-item">
            <span>Refresco - $20</span>
            <input type="number" id="refresco" min="0" value="0">
        </div>
        <button onclick="calcularPedido()">Finalizar Pedido</button>
    </div>
    <div id="pedido-detalle"></div>
    <script>
        function calcularPedido() {
            const precios = {
                tacos: 50,
                torta: 60,
                enchiladas: 70,
                quesadillas: 40,
                refresco: 20
            };
            const pedido = {
                tacos: parseInt(document.getElementById('tacos').value) || 0,
                torta: parseInt(document.getElementById('torta').value) || 0,
                enchiladas: parseInt(document.getElementById('enchiladas').value) || 0,
                quesadillas: parseInt(document.getElementById('quesadillas').value) || 0,
                refresco: parseInt(document.getElementById('refresco').value) || 0
            };
            let total = 0;
            let detalle = '<h3>Tu Pedido</h3>';
            if (pedido.tacos > 0) {
                detalle += `<p>Tacos x${pedido.tacos}: $${pedido.tacos * precios.tacos}</p>`;
                total += pedido.tacos * precios.tacos;
            }
            if (pedido.torta > 0) {
                detalle += `<p>Torta de milanesa x${pedido.torta}: $${pedido.torta * precios.torta}</p>`;
                total += pedido.torta * precios.torta;
            }
            if (pedido.enchiladas > 0) {
                detalle += `<p>Enchiladas verdes x${pedido.enchiladas}: $${pedido.enchiladas * precios.enchiladas}</p>`;
                total += pedido.enchiladas * precios.enchiladas;
            }
            if (pedido.quesadillas > 0) {
                detalle += `<p>Quesadillas x${pedido.quesadillas}: $${pedido.quesadillas * precios.quesadillas}</p>`;
                total += pedido.quesadillas * precios.quesadillas;
            }
            if (pedido.refresco > 0) {
                detalle += `<p>Refresco x${pedido.refresco}: $${pedido.refresco * precios.refresco}</p>`;
                total += pedido.refresco * precios.refresco;
            }
            if (total === 0) {
                detalle = '<p>No seleccionaste ningún platillo.</p>';
            } else {
                detalle += `<h4>Total: $${total}</h4>`;
                detalle += '<p>¡Gracias por tu pedido en La Esperanza!</p>';
            }
            const detalleDiv = document.getElementById('pedido-detalle');
            detalleDiv.innerHTML = detalle;
            detalleDiv.style.display = 'block';
        }
    </script>
</body>
</html>
