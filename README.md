<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <title>Dashboard - Lácteos Andinos</title>
    <style>
        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background-color: #fff8f0;
            margin: 0;
            padding: 20px;
            display: flex;
        }

        * {
            box-sizing: border-box;
        }

        .sidebar {
            width: 240px;
            background-color: #ffcf75;
            color: #4b3d1f;
            height: 100vh;
            padding: 20px;
            position: fixed;
        }

        .sidebar h2 {
            margin-top: 0;
            text-align: center;
        }

        .sidebar ul {
            list-style-type: none;
            padding: 0;
        }

        .sidebar ul li {
            padding: 10px;
            border-bottom: 1px solid #e1a948;
        }

        .sidebar ul li:hover {
            background-color: #ffd98f;
            cursor: pointer;
        }

        .main-content {
            margin-left: 260px;
            padding: 20px;
            width: 100%;
        }

        h1 {
            text-align: center;
            color: #4b3d1f;
        }

        .dashboard {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 20px;
            margin-top: 30px;
        }

        .card {
            background-color: #fff;
            border-radius: 10px;
            padding: 20px;
            box-shadow: 0 4px 8px rgba(255, 190, 90, 0.6);
            text-align: left;
        }

        .card h2 {
            color: #e29800;
        }

        .card p {
            font-size: 16px;
            color: #5a3f0e;
        }

        img {
            max-width: 100%;
            border-radius: 8px;
            margin: 10px 0;
        }

        form input, form textarea {
            width: 100%;
            padding: 10px;
            margin: 10px 0;
            border-radius: 5px;
            border: 1px solid #ccc;
        }

        form button {
            background-color: #e29800;
            color: white;
            padding: 10px 20px;
            border: none;
            border-radius: 5px;
            cursor: pointer;
        }
    </style>
</head>
<body>
    <div class="sidebar">
        <h2>Menú de opciones</h2>
        <ul>
            <li onclick="mostrar('inicio')">Inicio</li>
            <li onclick="mostrar('resumen')">Resumen</li>
            <li onclick="mostrar('productos')">Productos</li>
            <li onclick="mostrar('contacto')">Contacto</li>
        </ul>
    </div>

    <div class="main-content">
        <div id="inicio" class="seccion">
            <h1>Historia de Lácteos Andinos</h1>
            <p>Lácteos Andinos nació en el corazón del Valle del Mantaro, con la misión de ofrecer productos lácteos frescos, naturales y de alta calidad. Desde nuestros humildes inicios en una pequeña planta familiar, hemos crecido gracias a la confianza de nuestros clientes y el compromiso con la excelencia.</p>
            <img src="https://via.placeholder.com/600x300?text=Fábrica+de+Lácteos" alt="Fábrica">
        </div>

        <div id="resumen" class="seccion" style="display:none">
            <h1>Equipo Directivo</h1>
            <div class="card">
                <h2>Gerente General</h2>
                <p>María Elena Huamán - Con más de 15 años en la industria alimentaria, lidera nuestra empresa con visión e innovación.</p>
                <img src="https://via.placeholder.com/300x200?text=Gerente+General" alt="Gerente">
            </div>
            <div class="card">
                <h2>Director de Producción</h2>
                <p>José Luis Ramos - Encargado de asegurar que cada producto cumpla con los más altos estándares.</p>
            </div>
        </div>

        <div id="productos" class="seccion" style="display:none">
            <h1>Productos de Lácteos Andinos</h1>
            <div class="card">
                <h2>Leche Entera Pasteurizada</h2>
                <p>Leche fresca proveniente de vacas saludables, pasteurizada para garantizar su inocuidad y sabor.</p>
            </div>
            <div class="card">
                <h2>Queso Andino</h2>
                <p>Elaborado de forma artesanal, nuestro queso es perfecto para acompañar cualquier comida.</p>
            </div>
            <div class="card">
                <h2>Yogurt Natural</h2>
                <p>Yogurt cremoso, sin conservantes, con cultivos vivos que favorecen la digestión.</p>
            </div>
        </div>

        <div id="contacto" class="seccion" style="display:none">
            <h1>Contáctanos</h1>
            <form>
                <input type="text" placeholder="Nombre completo">
                <input type="email" placeholder="Correo electrónico">
                <textarea rows="4" placeholder="Mensaje"></textarea>
                <button type="submit">Enviar</button>
            </form>
        </div>

        <div id="dashboard" class="seccion">
            <h1>Dashboard de Ventas</h1>
            <div class="dashboard">
                <div class="card">
                    <h2>Personal Administrativo Destacado</h2>
                    <p>Rocío Salazar - Alcanzó un récord de ventas en el mes de abril, liderando la campaña "Leche para Todos".</p>
                </div>
                <div class="card">
                    <h2>Producto Más Vendido</h2>
                    <p>Yogurt Natural - 12,350 unidades vendidas en el último trimestre. Popular entre jóvenes y adultos por su sabor y calidad.</p>
                </div>
                <div class="card">
                    <h2>Top 5 Productos</h2>
                    <p>
                        1. Yogurt Natural - 12,350 unidades<br>
                        2. Queso Andino - 10,200 unidades<br>
                        3. Leche Entera - 8,750 unidades<br>
                        4. Yogurt de Fresa - 7,680 unidades<br>
                        5. Mantequilla Artesanal - 5,420 unidades
                    </p>
                </div>
            </div>
        </div>

    </div>

    <script>
        function mostrar(seccion) {
            document.querySelectorAll('.seccion').forEach(s => s.style.display = 'none');
            document.getElementById(seccion).style.display = 'block';
        }
    </script>
</body>
</html>
