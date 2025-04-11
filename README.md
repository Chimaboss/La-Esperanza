<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Menú - Lonchería La Esperanza</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 20px;
            background-color: #f4f4f4;
        }
        .container {
            max-width: 800px;
            margin: 0 auto;
            background: white;
            padding: 20px;
            border-radius: 8px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
        }
        h1 {
            text-align: center;
            color: #333;
        }
        h2 {
            color: #e67e22;
            border-bottom: 2px solid #e67e22;
            padding-bottom: 5px;
        }
        .menu-item {
            margin-bottom: 20px;
        }
        .menu-item h3 {
            margin: 0;
            color: #2c3e50;
        }
        .menu-item p {
            margin: 5px 0;
            color: #666;
        }
        .price {
            font-weight: bold;
            color: #27ae60;
        }
        @media (max-width: 600px) {
            .container {
                padding: 10px;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>Lonchería La Esperanza</h1>
        
        <h2>Desayunos</h2>
        <div class="menu-item">
            <h3>Chilaquiles Verdes</h3>
            <p>Tortillas fritas con salsa verde, crema, queso fresco y cebolla. Acompañados de frijoles refritos.</p>
            <p class="price">$85</p>
        </div>
        <div class="menu-item">
            <h3>Huevos Rancheros</h3>
            <p>Huevos estrellados sobre tortilla frita con salsa ranchera y aguacate.</p>
            <p class="price">$75</p>
        </div>

        <h2>Comidas</h2>
        <div class="menu-item">
            <h3>Mole Poblano</h3>
            <p>Pechuga de pollo bañada en mole poblano, servida con arroz rojo y tortillas.</p>
            <p class="price">$120</p>
        </div>
        <div class="menu-item">
            <h3>Enchiladas Suizas</h3>
            <p>Tortillas rellenas de pollo con salsa cremosa de tomatillo y gratinadas con queso.</p>
            <p class="price">$95</p>
        </div>

        <h2>Bebidas</h2>
        <div class="menu-item">
            <h3>Agua de Horchata</h3>
            <p>Refrescante bebida de arroz con canela.</p>
            <p class="price">$25</p>
        </div>
        <div class="menu-item">
            <h3>Café de Olla</h3>
            <p>Café tradicional con piloncillo y canela.</p>
            <p class="price">$30</p>
        </div>
    </div>
</body>
</html>
