
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






<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Validación de Correo</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #f0f2f5;
            display: flex;
            justify-content: center;
            align-items: center;
            min-height: 100vh;
            margin: 0;
            text-align: center;
        }
        .container {
            background-color: #fff;
            padding: 40px;
            border-radius: 10px;
            box-shadow: 0 4px 15px rgba(0, 0, 0, 0.1);
            max-width: 400px;
            width: 100%;
            box-sizing: border-box;
        }
        h1 {
            color: #333;
            margin-bottom: 20px;
        }
        .input-group {
            margin-bottom: 20px;
        }
        .input-group input {
            width: 100%;
            padding: 12px;
            border: 1px solid #ccc;
            border-radius: 5px;
            font-size: 1em;
            box-sizing: border-box;
        }
        .btn {
            width: 100%;
            padding: 12px;
            background-color: #007bff;
            color: white;
            border: none;
            border-radius: 5px;
            font-size: 1.1em;
            cursor: pointer;
            transition: background-color 0.3s ease;
        }
        .btn:hover {
            background-color: #0056b3;
        }
        .error-message {
            color: red;
            font-size: 0.9em;
            margin-top: -10px;
            margin-bottom: 10px;
            display: none; /* Oculto por defecto */
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>Ingresa tu Correo</h1>
        <div class="input-group">
            <input type="email" id="emailInput" placeholder="correo@ejemplo.com">
        </div>
        <p class="error-message" id="errorMessage">Por favor, introduce un correo electrónico válido.</p>
        <button class="btn" onclick="validateEmail()">Acceder</button>
    </div>
    <script>
        function validateEmail() {
            const emailInput = document.getElementById('emailInput');
            const errorMessage = document.getElementById('errorMessage');
            const emailValue = emailInput.value.trim();
            // Expresión regular para validar el formato del correo
            const emailRegex = /^[^\s@]+@[^\s@]+\.[^\s@]+$/;
            if (emailRegex.test(emailValue)) {
                // Si el correo es válido, oculta el mensaje de error y redirige
                errorMessage.style.display = 'none';
                window.location.href = 'https://ice2606.github.io/elegante-02/'; // Reemplaza con la URL de tu página de destino
            } else {
                // Si el correo no es válido, muestra el mensaje de error
                errorMessage.style.display = 'block';
            }
        }
    </script>
</body>
</html>

