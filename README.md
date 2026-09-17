# Siboney--hotel--honda-3d
Página web 
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Hotel Oasis Honda - Naturaleza y Confort</title>
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600;800&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    
    <style>
        /* --- VARIABLES Y RESET --- */
        :root {
            --primary: #007BFF; /* Azul piscina */
            --secondary: #28a745; /* Verde naturaleza */
            --dark: #333;
            --light: #f4f7f6;
            --white: #ffffff;
            --shadow: 10px 10px 30px rgba(0,0,0,0.15), -10px -10px 30px rgba(255,255,255,0.8);
            --shadow-hover: 15px 15px 40px rgba(0,0,0,0.2), -15px -15px 40px rgba(255,255,255,0.9);
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Poppins', sans-serif;
            scroll-behavior: smooth;
        }

        body {
            background-color: var(--light);
            color: var(--dark);
        }

        /* --- HERO SECTION (Portada) --- */
        .hero {
            height: 100vh;
            background: linear-gradient(rgba(0,0,0,0.3), rgba(0,0,0,0.6)), url('https://images.unsplash.com/photo-1540541338287-41700207dee6?ixlib=rb-4.0.3&auto=format&fit=crop&w=1920&q=80') center/cover fixed;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            text-align: center;
            color: var(--white);
            padding: 0 20px;
        }

        .hero h1 {
            font-size: 4rem;
            text-shadow: 2px 4px 10px rgba(0,0,0,0.5);
            margin-bottom: 15px;
            animation: fadeInDown 1s ease;
        }

        .hero p {
            font-size: 1.5rem;
            margin-bottom: 30px;
            text-shadow: 1px 2px 5px rgba(0,0,0,0.5);
            animation: fadeInUp 1s ease;
        }

        .btn-main {
            padding: 15px 40px;
            font-size: 1.2rem;
            font-weight: 600;
            color: var(--white);
            background: linear-gradient(45deg, var(--primary), #00d2ff);
            border: none;
            border-radius: 50px;
            cursor: pointer;
            text-decoration: none;
            box-shadow: 0 10px 20px rgba(0, 123, 255, 0.4);
            transition: all 0.3s ease;
            animation: pulseBtn 2s infinite;
        }

        .btn-main:hover {
            transform: scale(1.05) translateY(-5px);
            box-shadow: 0 15px 25px rgba(0, 123, 255, 0.6);
        }

        /* --- SECCIÓN ACERCA DE Y HABITACIONES (Efecto 3D) --- */
        .container {
            max-width: 1200px;
            margin: 80px auto;
            padding: 0 20px;
        }

        .section-title {
            text-align: center;
            font-size: 2.5rem;
            margin-bottom: 50px;
            color: var(--dark);
        }

        .grid-3d {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 40px;
        }

        .card-3d {
            background: var(--light);
            border-radius: 20px;
            padding: 20px;
            box-shadow: var(--shadow);
            transition: all 0.4s ease;
            text-align: center;
            transform-style: preserve-3d;
            perspective: 1000px;
        }

        .card-3d:hover {
            transform: translateY(-15px);
            box-shadow: var(--shadow-hover);
        }

        .card-3d img {
            width: 100%;
            height: 250px;
            object-fit: cover;
            border-radius: 15px;
            margin-bottom: 20px;
            box-shadow: inset 0 0 10px rgba(0,0,0,0.1);
        }

        .card-3d h3 {
            font-size: 1.5rem;
            margin-bottom: 10px;
            color: var(--primary);
        }

        /* --- FORMULARIO DE RESERVAS (Glassmorphism) --- */
        .booking-section {
            background: url('https://images.unsplash.com/photo-1571896349842-33c89424de2d?ixlib=rb-4.0.3&auto=format&fit=crop&w=1920&q=80') center/cover fixed;
            padding: 100px 20px;
            position: relative;
        }

        .glass-form {
            max-width: 600px;
            margin: 0 auto;
            background: rgba(255, 255, 255, 0.2);
            backdrop-filter: blur(15px);
            -webkit-backdrop-filter: blur(15px);
            border: 1px solid rgba(255, 255, 255, 0.3);
            border-radius: 20px;
            padding: 40px;
            box-shadow: 0 8px 32px 0 rgba(0, 0, 0, 0.3);
            color: var(--white);
        }

        .glass-form h2 {
            text-align: center;
            margin-bottom: 20px;
            font-size: 2rem;
            text-shadow: 1px 1px 2px rgba(0,0,0,0.5);
        }

        .form-group {
            margin-bottom: 20px;
        }

        .form-group label {
            display: block;
            margin-bottom: 5px;
            font-weight: 600;
        }

        .form-group input, .form-group select {
            width: 100%;
            padding: 12px;
            border: none;
            border-radius: 10px;
            background: rgba(255, 255, 255, 0.8);
            color: var(--dark);
            font-size: 1rem;
            outline: none;
            box-shadow: inset 0 2px 5px rgba(0,0,0,0.1);
        }

        .btn-submit {
            width: 100%;
            padding: 15px;
            font-size: 1.2rem;
            font-weight: bold;
            background: linear-gradient(45deg, #25D366, #128C7E); /* Colores WhatsApp */
            color: white;
            border: none;
            border-radius: 10px;
            cursor: pointer;
            box-shadow: 0 10px 20px rgba(37, 211, 102, 0.4);
            transition: 0.3s;
        }

        .btn-submit:hover {
            transform: translateY(-3px);
            box-shadow: 0 15px 25px rgba(37, 211, 102, 0.6);
        }

        /* --- BOTÓN WHATSAPP FLOTANTE --- */
        .whatsapp-float {
            position: fixed;
            width: 60px;
            height: 60px;
            bottom: 40px;
            right: 40px;
            background-color: #25d366;
            color: #FFF;
            border-radius: 50px;
            text-align: center;
            font-size: 35px;
            box-shadow: 2px 2px 15px rgba(0,0,0,0.3);
            z-index: 100;
            display: flex;
            justify-content: center;
            align-items: center;
            text-decoration: none;
            animation: pulseWpp 2s infinite;
        }

        .whatsapp-float:hover {
            background-color: #128C7E;
        }

        /* --- ANIMACIONES --- */
        @keyframes fadeInDown {
            from { opacity: 0; transform: translateY(-30px); }
            to { opacity: 1; transform: translateY(0); }
        }
        @keyframes fadeInUp {
            from { opacity: 0; transform: translateY(30px); }
            to { opacity: 1; transform: translateY(0); }
        }
        @keyframes pulseBtn {
            0% { box-shadow: 0 0 0 0 rgba(0, 123, 255, 0.7); }
            70% { box-shadow: 0 0 0 15px rgba(0, 123, 255, 0); }
            100% { box-shadow: 0 0 0 0 rgba(0, 123, 255, 0); }
        }
        @keyframes pulseWpp {
            0% { box-shadow: 0 0 0 0 rgba(37, 211, 102, 0.7); }
            70% { box-shadow: 0 0 0 20px rgba(37, 211, 102, 0); }
            100% { box-shadow: 0 0 0 0 rgba(37, 211, 102, 0); }
        }
        
        /* Footer */
        footer {
            background: var(--dark);
            color: white;
            text-align: center;
            padding: 20px;
        }

    </style>
</head>
<body>

    <!-- PORTADA PRINCIPAL -->
    <header class="hero">
        <h1>Tu Oasis en Honda, Tolima</h1>
        <p>Arquitectura en cristal, piscinas de ensueño y conexión total con la naturaleza.</p>
        <a href="#reservar" class="btn-main">¡Reserva Ahora!</a>
    </header>

    <!-- SECCIÓN DE INSTALACIONES (Efecto 3D) -->
    <section class="container">
        <h2 class="section-title">Nuestras Instalaciones</h2>
        <div class="grid-3d">
            
            <!-- TARJETA 1 (Reemplazar imagen con la foto de la habitación) -->
            <div class="card-3d">
                <img src="https://images.unsplash.com/photo-1590490360182-c33d57733427?ixlib=rb-4.0.3&auto=format&fit=crop&w=600&q=80" alt="Habitación">
                <h3>Habitaciones Panorámicas</h3>
                <p>Despierta rodeado de verde. Habitaciones con ventanales de piso a techo, aire acondicionado y máximo confort.</p>
            </div>

            <!-- TARJETA 2 (Reemplazar imagen con la foto de la piscina) -->
            <div class="card-3d">
                <img src="https://images.unsplash.com/photo-1576013551627-11936b10852d?ixlib=rb-4.0.3&auto=format&fit=crop&w=600&q=80" alt="Piscina">
                <h3>Zonas Húmedas</h3>
                <p>Relájate en nuestras amplias piscinas bajo el sol de Honda. Contamos con zonas de sombra y servicio de bar.</p>
            </div>

            <!-- TARJETA 3 (Reemplazar imagen con la foto de la familia) -->
            <div class="card-3d">
                <img src="https://images.unsplash.com/photo-1544837546-5ba93b763ec4?ixlib=rb-4.0.3&auto=format&fit=crop&w=600&q=80" alt="Ambiente Familiar">
                <h3>Ambiente Familiar</h3>
                <p>El lugar perfecto para crear recuerdos inolvidables con los que más amas. Espacios seguros y divertidos.</p>
            </div>

        </div>
    </section>

    <!-- SECCIÓN DE RESERVAS QUE ENVÍA A WHATSAPP -->
    <section id="reservar" class="booking-section">
        <div class="glass-form">
            <h2>Solicitar Reserva</h2>
            <p style="text-align: center; margin-bottom: 20px;">Completa tus datos y te confirmaremos disponibilidad al instante.</p>
            
            <form id="reservaForm">
                <div class="form-group">
                    <label>Nombre Completo</label>
                    <input type="text" id="nombre" required placeholder="Ej: Juan Pérez">
                </div>
                <div class="form-group">
                    <label>Fecha de Llegada</label>
                    <input type="date" id="llegada" required>
                </div>
                <div class="form-group">
                    <label>Número de Personas</label>
                    <select id="personas">
                        <option value="1 a 2">1 a 2 Personas (Pareja)</option>
                        <option value="3 a 4">3 a 4 Personas (Familia)</option>
                        <option value="5 o más">5 o más (Grupo)</option>
                    </select>
                </div>
                <!-- Botón que activa el JavaScript para enviar a WhatsApp -->
                <button type="button" class="btn-submit" onclick="enviarWhatsApp()">
                    <i class="fab fa-whatsapp"></i> Enviar Solicitud por WhatsApp
                </button>
            </form>
        </div>
    </section>

    <!-- BOTÓN FLOTANTE WHATSAPP (Chat directo) -->
    <!-- Cambia el "573001234567" por tu número real -->
    <a href="https://wa.me/573001234567?text=Hola,%20vengo%20de%20la%20página%20web%20y%20quiero%20información%20del%20hotel." class="whatsapp-float" target="_blank">
        <i class="fab fa-whatsapp"></i>
    </a>

    <footer>
        <p>© 2023 Hotel Oasis Honda - Todos los derechos reservados.</p>
    </footer>

    <!-- SCRIPT PARA PROCESAR LA RESERVA Y ENVIARLA A WHATSAPP -->
    <script>
        function enviarWhatsApp() {
            // 1. REEMPLAZA ESTE NÚMERO POR EL TUYO (Incluye código de país, sin el "+")
            const numeroHotel = "573001234567"; 
            
            // 2. Capturar los datos del formulario
            const nombre = document.getElementById('nombre').value;
            const llegada = document.getElementById('llegada').value;
            const personas = document.getElementById('personas').value;

            // Validación simple
            if(nombre === "" || llegada === "") {
                alert("Por favor, completa tu nombre y la fecha de llegada.");
                return;
            }

            // 3. Construir el mensaje
            const mensaje = `*¡Hola! Quiero hacer una reserva en el Hotel.*%0A%0A*Mis Datos:*%0A👤 Nombre: ${nombre}%0A📅 Fecha de llegada: ${llegada}%0A👨‍👩‍👧‍👦 Personas: ${personas}%0A%0A¿Me podrían confirmar disponibilidad y tarifas?`;

            // 4. Redirigir a WhatsApp
            const urlWhatsApp = `https://wa.me/${numeroHotel}?text=${mensaje}`;
            window.open(urlWhatsApp, '_blank');
        }
    </script>

</body>
</html>
