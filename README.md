# elegante-01

<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Catálogo - Calzado Elegante</title>
  <style>
    @import url('https://fonts.googleapis.com/css2?family=Montserrat:wght@400;700&display=swap');
    body {
      font-family: 'Montserrat', sans-serif;
      margin: 0;
      padding: 0;
      background: linear-gradient(to right, #ffffff, #e8f0f8);
    }
    header {
      background: url('https://images.unsplash.com/photo-1600185365483-26a7d016c6e7?auto=format&fit=crop&w=1350&q=80') no-repeat center center/cover;
      color: white;
      padding: 80px 20px;
      text-align: center;
      border-radius: 0 0 30px 30px;
      box-shadow: 0 8px 16px rgba(0,0,0,0.3);
    }
    header h1 {
      font-size: 3em;
      margin-bottom: 10px;
      text-shadow: 2px 2px 4px rgba(0,0,0,0.5);
    }
    header p {
      font-size: 1.2em;
      text-shadow: 1px 1px 3px rgba(0,0,0,0.3);
    }
    nav {
      display: flex;
      justify-content: center;
      flex-wrap: wrap;
      margin-top: 20px;
      gap: 15px;
    }
    nav button {
      background-color: #e67e22;
      color: white;
      border: none;
      padding: 10px 25px;
      font-size: 1em;
      border-radius: 25px;
      cursor: pointer;
      transition: background-color 0.3s;
    }
    nav button:hover {
      background-color: #d35400;
    }
    .catalogo {
      display: flex;
      flex-wrap: wrap;
      justify-content: center;
      gap: 30px;
      margin: 40px auto;
      max-width: 1200px;
    }
    .producto {
      background: white;
      border-radius: 15px;
      box-shadow: 0 6px 12px rgba(0, 0, 0, 0.1);
      width: 280px;
      padding: 20px;
      text-align: center;
      transition: transform 0.3s;
    }
    .producto:hover {
      transform: scale(1.05);
    }
    .producto img {
      width: 100%;
      border-radius: 10px;
      margin-bottom: 15px;
    }
    .producto h3 {
      margin: 10px 0 5px;
      color: #2c3e50;
    }
    .producto p {
      font-size: 0.95em;
      color: #555;
    }
    .producto .precio {
      font-weight: bold;
      color: #e67e22;
      margin: 10px 0;
    }
    .buscador {
      text-align: center;
      margin-top: 30px;
    }
    .buscador input {
      padding: 10px;
      width: 300px;
      font-size: 1em;
      border-radius: 20px;
      border: 1px solid #ccc;
    }
  </style>
</head>
<body>
  <header>
    <h1>Calzado Elegante</h1>
    <p>¡Encuentra tu estilo con nuestro catálogo exclusivo de calzado!</p>
  </header>

  <nav>
    <button onclick="filtrarCategoria('Sandalias')">Sandalias</button>
    <button onclick="filtrarCategoria('Zapatos')">Zapatos</button>
    <button onclick="filtrarCategoria('Chinelas')">Chinelas</button>
    <button onclick="filtrarCategoria('Todos')">Todos</button>
  </nav>

  <div class="buscador">
    <input type="text" id="busqueda" placeholder="Buscar por nombre..." oninput="buscarProducto()">
  </div>

  <section class="catalogo" id="catalogo"></section>

  <script>
    const productos = [
      {
        id: 201,
        nombre: "Sandalias Clásicas",
        categoria: "Sandalias",
        descripcion: "Sandalias cómodas para uso diario, diseño casual y ventilado.",
        precio: 25.00,
        imagen: "https://via.placeholder.com/280x180?text=Sandalias"
      },
      {
        id: 202,
        nombre: "Zapatos Elegantes de Cuero",
        categoria: "Zapatos",
        descripcion: "Zapatos formales ideales para eventos importantes y trabajo.",
        precio: 80.00,
        imagen: "https://via.placeholder.com/280x180?text=Zapatos+Elegantes"
      },
      {
        id: 203,
        nombre: "Chinelas de Hule",
        categoria: "Chinelas",
        descripcion: "Chinelas resistentes, perfectas para la casa y exteriores húmedos.",
        precio: 15.00,
        imagen: "https://via.placeholder.com/280x180?text=Chinelas+de+Hule"
      }
    ];

    const catalogo = document.getElementById("catalogo");
    const inputBusqueda = document.getElementById("busqueda");

    function mostrarProductos(lista) {
      catalogo.innerHTML = "";
      lista.forEach(producto => {
        const card = document.createElement("div");
        card.className = "producto";
        card.innerHTML = `
          <img src="${producto.imagen}" alt="${producto.nombre}">
          <h3>${producto.nombre}</h3>
          <p>${producto.descripcion}</p>
          <div class="precio">$${producto.precio.toFixed(2)}</div>
        `;
        catalogo.appendChild(card);
      });
    }

    function filtrarCategoria(categoria) {
      if (categoria === 'Todos') {
        mostrarProductos(productos);
      } else {
        const filtrados = productos.filter(p => p.categoria === categoria);
        mostrarProductos(filtrados);
      }
    }

    function buscarProducto() {
      const termino = inputBusqueda.value.toLowerCase();
      const resultado = productos.filter(p => p.nombre.toLowerCase().includes(termino));
      mostrarProductos(resultado);
    }

    mostrarProductos(productos);
  </script>
</body>
</html>
