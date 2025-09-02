
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>BIENVENIDO</title>
    <style>
        body {
            font-family: sans-serif;
            margin: 0;
            padding: 20px;
            background-color: #f0f0f0;
            text-align: center;
        }
        .blue-box {
            background-color: #1976d2; /* azul fuerte */
            border-radius: 16px;
            box-shadow: 0 6px 18px rgba(0,0,0,0.18);
            max-width: 600px;
            margin: 40px auto;
            padding: 32px 18px 36px 18px;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
        }
        h1, h2 {
            margin: 10px 0;
            color: #fff;
        }
        h1 {
            font-size: 2.5em;
            letter-spacing: 1px;
        }
        h2 {
            font-size: 1.5em;
            color: #cde6ff;
            font-weight: 400;
        }
        .image-container {
            width: 100%;
            max-width: 320px;
            margin-top: 20px;
        }
        img {
            max-width: 100%;
            height: auto;
            border-radius: 10px;
            box-shadow: 0 4px 16px rgba(0,0,0,0.14);
        }
        .button-group {
            margin-top: 28px;
            display: flex;
            gap: 18px;
            flex-wrap: wrap;
        }
        .orange-btn {
            background-color: #ff9800;
            color: #fff;
            border: none;
            border-radius: 6px;
            padding: 12px 28px;
            font-size: 1.06em;
            font-weight: 600;
            text-decoration: none;
            transition: background 0.2s, transform 0.1s;
            cursor: pointer;
            box-shadow: 0 2px 8px rgba(0,0,0,0.10);
            outline: none;
            display: inline-block;
        }
        .orange-btn:hover, .orange-btn:focus {
            background-color: #ffb74d;
            color: #fff;
            transform: translateY(-2px) scale(1.03);
        }
        @media (max-width: 480px) {
            .blue-box {
                padding: 18px 4vw 20px 4vw;
                max-width: 98vw;
            }
            h1 {
                font-size: 2em;
            }
            h2 {
                font-size: 1.1em;
            }
            .button-group {
                flex-direction: column;
                gap: 10px;
            }
        }
    </style>
</head>
<body>
    <div class="blue-box">
        <h1>CALZADO ELEGANTE</h1>
        <h2>Encuentra tu mejor estilo de calzado con nuestro catálogo exclusivo</h2>
        <div class="image-container">
            <img src="01.jpg" alt="Descripción de la imagen">
        </div>
        <div class="button-group">
            <a href="catalogo.html" class="orange-btn">Catálogo</a>
            <a href="ofertas.html" class="orange-btn">Ofertas</a>
            <a href="contacto.html" class="orange-btn">Contacto</a>
        </div>
    </div>
</body>
</html>












<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title></title>
    <style>
        body {
            /* Ruta de tu imagen de fondo */
            background-image: url('fondo.jpg');  
            /* Ajusta la imagen para que cubra todo el cuerpo */
            background-size: cover; 
            /* Fija la imagen para que no se mueva al hacer scroll */
            background-attachment: fixed;
            /* Centra la imagen en la pantalla */
            background-position: center; 
            /* Evita que se repita la imagen */
            background-repeat: no-repeat;
            /* Establece una altura mínima para que se vea el fondo */
            min-height: 100vh;
            /* Elimina los márgenes predeterminados del body */
            margin: 0
            /* Opcional: Estilo de texto para que contraste con el fondo */
            color: #fff;
            text-shadow: 2px 2px 4px rgba(0,0,0,0.5);
            font-family: sans-serif;
            display: flex;
            justify-content: center;
            align-items: center;
            text-align: center;
    }
        h1 {
            font-size: 3em;
        }
    </style>
</head>
<body>
    <h1></h1>
</body>
</html>








