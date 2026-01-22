<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <title>Maravillas del Mundo</title>
    <style>
        body {
            margin: 0;
            font-family: 'Georgia', serif;
            background-color: #000;
            color: white;
            text-align: center;
        }

        header {
            display: flex;
            justify-content: space-between;
            padding: 20px 40px;
        }

        header a {
            color: white;
            text-decoration: none;
            margin-left: 20px;
        }

        h1 {
            margin: 40px 0;
        }

        .gallery {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 40px;
            padding: 0 80px 80px;
        }

        .gallery img {
            width: 100%;
            border-radius: 8px;
            cursor: pointer;
            transition: transform 0.3s;
        }

        .gallery img:hover {
            transform: scale(1.05);
        }

        /* Modal */
        .modal {
            display: none;
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(0, 0, 0, 0.85);
            justify-content: center;
            align-items: center;
        }

        .modal-content {
            background: #111;
            padding: 30px;
            border-radius: 10px;
            width: 60%;
        }

        .modal-content h2 {
            margin-top: 0;
        }

        .close {
            color: #fff;
            float: right;
            font-size: 24px;
            cursor: pointer;
        }
    </style>
</head>
<body>

<header>
    <div>Jessi y Brii</div>
    <nav>
        <a href="#">Trabajo</a>
        <a href="#">Acerca de</a>
    </nav>
</header>

<h1>Maravillas del Mundo</h1>

<div class="gallery">
    <img src="https://upload.wikimedia.org/wikipedia/commons/d/da/Taj-Mahal.jpg"
         onclick="showInfo('Taj Mahal', 'Ubicado en India, es un mausoleo de mármol blanco construido en el siglo XVII como símbolo del amor eterno.')">

    <img src="https://upload.wikimedia.org/wikipedia/commons/d/de/Colosseo_2020.jpg"
         onclick="showInfo('Coliseo Romano', 'Situado en Roma, Italia, fue un anfiteatro usado para espectáculos públicos en la antigua Roma.')">

    <img src="https://cobasunset.info/wp-content/uploads/2022/02/Chichen-1.jpg"
         onclick="showInfo('Chichén Itzá', 'Antigua ciudad maya en México, famosa por la pirámide de Kukulkán.')">

    <img src="https://dynamic-media.tacdn.com/media/photo-o/30/33/90/d9/caption.jpg?w=700&h=500&s=1"
         onclick="showInfo('Cristo Redentor', 'Estatua de Jesús ubicada en Río de Janeiro, Brasil, símbolo de paz y fe.')">

    <img src="https://static.nationalgeographicla.com/files/styles/image_3200/public/nationalgeographic2709904-copia.jpg?w=1600"
         onclick="showInfo('Gran Muralla China', 'Extensa fortificación construida para proteger China de invasiones.')">

    <img src="https://farm3.staticflickr.com/2106/5748356313_e3d389c8d4_z.jpg"
         onclick="showInfo('Petra', 'Ciudad arqueológica en Jordania, famosa por sus construcciones talladas en roca.')">
    
    <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/c/ca/Machu_Picchu%2C_Peru_%282018%29.jpg/500px-Machu_Picchu%2C_Peru_%282018%29.jpg"
         onclick="showInfo('Machu Picchu' , 'Machu Picchu es una ciudadela inca ubicada en las alturas de las montañas de los Andes en Perú, sobre el valle del río Urubamba.')">
</div>

<!-- Modal -->
<div id="modal" class="modal">
    <div class="modal-content">
        <span class="close" onclick="closeModal()">&times;</span>
        <h2 id="title"></h2>
        <p id="description"></p>
    </div>
</div>

<script>
    function showInfo(title, description) {
        document.getElementById("title").innerText = title;
        document.getElementById("description").innerText = description;
        document.getElementById("modal").style.display = "flex";
    }

    function closeModal() {
        document.getElementById("modal").style.display = "none";
    }
</script>

</body>
</html>
