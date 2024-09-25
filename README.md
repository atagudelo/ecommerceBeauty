# ecommerceBeauty
Plataforma Web para venta de productos de belleza 
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>E-commerce Belleza - Inicio</title>
    <link rel="stylesheet" href="css/styles.css">
</head>
<body>
    <header>
        <h1>Bienvenidos a Belleza Natural</h1>
        <nav>
            <ul>
                <li><a href="index.html">Inicio</a></li>
                <li><a href="productos.html">Productos</a></li>
                <li><a href="contacto.html">Contacto</a></li>
                <li><a href="carrito.html">Carrito</a></li>
            </ul>
        </nav>
    </header>
    
    <main>
        <section>
            <h2>Nuestros Productos Destacados</h2>
            <div class="producto">
                <img src="img/producto1.jpg" alt="Producto 1">
                <h3>Producto 1</h3>
                <p>Descripción breve del producto.</p>
                <button onclick="agregarAlCarrito('Producto 1')">Agregar al Carrito</button>
            </div>
            <!-- Agrega más productos aquí -->
        </section>
    </main>
    
    <footer>
        <p>Contacto: contacto@bellezanatural.com | Tel: 123-456-7890</p>
    </footer>
    
    <script src="js/main.js"></script>
</body>
</html>
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>E-commerce Belleza - Productos</title>
    <link rel="stylesheet" href="css/styles.css">
</head>
<body>
    <header>
        <h1>Productos Disponibles</h1>
        <nav>
            <ul>
                <li><a href="index.html">Inicio</a></li>
                <li><a href="productos.html">Productos</a></li>
                <li><a href="contacto.html">Contacto</a></li>
                <li><a href="carrito.html">Carrito</a></li>
            </ul>
        </nav>
    </header>
    
    <main>
        <section>
            <h2>Lista de Productos</h2>
            <div class="producto">
                <img src="img/producto1.jpg" alt="Producto 1">
                <h3>Producto 1</h3>
                <p>Descripción del producto 1.</p>
                <p>Precio: $10.00</p>
                <button onclick="agregarAlCarrito('Producto 1')">Agregar al Carrito</button>
            </div>
            <!-- Agrega más productos aquí -->
        </section>
    </main>
    
    <footer>
        <p>Contacto: contacto@bellezanatural.com | Tel: 123-456-7890</p>
    </footer>
    
    <script src="js/main.js"></script>
</body>
</html>
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>E-commerce Belleza - Contacto</title>
    <link rel="stylesheet" href="css/styles.css">
</head>
<body>
    <header>
        <h1>Contacto</h1>
        <nav>
            <ul>
                <li><a href="index.html">Inicio</a></li>
                <li><a href="productos.html">Productos</a></li>
                <li><a href="contacto.html">Contacto</a></li>
                <li><a href="carrito.html">Carrito</a></li>
            </ul>
        </nav>
    </header>
    
    <main>
        <section>
            <h2>Formulario de Contacto</h2>
            <form id="contactoForm">
                <label for="nombre">Nombre:</label>
                <input type="text" id="nombre" name="nombre" required>
                
                <label for="email">Email:</label>
                <input type="email" id="email" name="email" required>
                
                <label for="mensaje">Mensaje:</label>
                <textarea id="mensaje" name="mensaje" required></textarea>
                
                <button type="submit">Enviar</button>
            </form>
        </section>
    </main>
    
    <footer>
        <p>Contacto: contacto@bellezanatural.com | Tel: 123-456-7890</p>
    </footer>
    
    <script src="js/main.js"></script>
</body>
</html>
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>E-commerce Belleza - Carrito</title>
    <link rel="stylesheet" href="css/styles.css">
</head>
<body>
    <header>
        <h1>Tu Carrito de Compras</h1>
        <nav>
            <ul>
                <li><a href="index.html">Inicio</a></li>
                <li><a href="productos.html">Productos</a></li>
                <li><a href="contacto.html">Contacto</a></li>
                <li><a href="carrito.html">Carrito</a></li>
            </ul>
        </nav>
    </header>
    
    <main>
        <section>
            <h2>Productos en el Carrito</h2>
            <ul id="listaCarrito">
                <!-- Los productos se agregarán aquí dinámicamente -->
            </ul>
            <p>Total: <span id="total">0</span></p>
            <button onclick="finalizarCompra()">Finalizar Compra</button>
        </section>
    </main>
    
    <footer>
        <p>Contacto: contacto@bellezanatural.com | Tel: 123-456-7890</p>
    </footer>
    
    <script src="js/main.js"></script>
</body>
</html>
body {
    font-family: Arial, sans-serif;
    margin: 0;
    padding: 0;
    background-color: #f4f4f4;
}

header {
    background-color: #333;
    color: #fff;
    padding: 10px 0;
    text-align: center;
}

nav ul {
    list-style: none;
    padding: 0;
}

nav ul li {
    display: inline;
    margin: 0 15px;
}

nav ul li a {
    color: #fff;
    text-decoration: none;
}

main {
    padding: 20px;
}

.producto {
    border: 1px solid #ccc;
    background-color: #fff;
    padding: 10px;
    margin: 10px 0;
}

footer {
    background-color: #333;
    color: #fff;
    text-align: center;
    padding: 10px 0;
    position: relative;
    bottom: 0;
    width: 100%;
}
let carrito = [];

function agregarAlCarrito(producto) {
    carrito.push(producto);
    alert(`${producto} ha sido agregado al carrito.`);
    actualizarCarrito();
}

function actualizarCarrito() {
    const listaCarrito = document.getElementById('listaCarrito');
    listaCarrito.innerHTML = '';

    let total = 0;
    carrito.forEach((producto, index) => {
        const li = document.createElement('li');
        li.textContent = producto;
        listaCarrito.appendChild(li);
        total += 10; // Supongamos que todos los productos tienen un precio fijo
    });
    document.getElementById('total').textContent = total;
}

function finalizarCompra() {
    if (carrito.length > 0) {
        alert('Compra finalizada. ¡Gracias por tu compra!');
        carrito = []; // Limpiar carrito
        actualizarCarrito();
    } else {
        alert('Tu carrito está vacío.');
    }
}

document.getElementById('contactoForm').addEventListener('submit', function(event) {
    event.preventDefault();
    alert('Mensaje enviado. Gracias por contactarnos!');
    this.reset(); // Reiniciar el formulario
});
let carrito = [];

function agregarAlCarrito(producto) {
    carrito.push(producto);
    alert(`${producto} ha sido agregado al carrito.`);
    actualizarCarrito();
}

function actualizarCarrito() {
    const listaCarrito = document.getElementById('listaCarrito');
    listaCarrito.innerHTML = '';

    let total = 0;
    carrito.forEach((producto, index) => {
        const li = document.createElement('li');
        li.textContent = producto;
        listaCarrito.appendChild(li);
        total += 10; // Supongamos que todos los productos tienen un precio fijo
    });
    document.getElementById('total').textContent = total;
}

function finalizarCompra() {
    if (carrito.length > 0) {
        alert('Compra finalizada. ¡Gracias por tu compra!');
        carrito = []; // Limpiar carrito
        actualizarCarrito();
    } else {
        alert('Tu carrito está vacío.');
    }
}

document.getElementById('contactoForm').addEventListener('submit', function(event) {
    event.preventDefault();
    alert('Mensaje enviado. Gracias por contactarnos!');
    this.reset(); // Reiniciar el formulario
});
