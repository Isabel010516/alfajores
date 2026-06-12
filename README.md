<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Alfajores</title>

<style>
*{
    margin:0;
    padding:0;
    box-sizing:border-box;
    font-family: Arial, Helvetica, sans-serif;
}

body{
    background: linear-gradient(135deg,#ffcc70,#ff8c42,#ff5e78);
    min-height:100vh;
}

.pantalla{
    display:none;
    min-height:100vh;
    justify-content:center;
    align-items:center;
    flex-direction:column;
    text-align:center;
    padding:20px;
}

.activa{
    display:flex;
}

h1{
    color:white;
    font-size:4rem;
    text-shadow:3px 3px 8px rgba(0,0,0,0.3);
    margin-bottom:20px;
}

.imagen-principal{
    width:400px;
    max-width:90%;
    border-radius:20px;
    box-shadow:0 0 20px rgba(0,0,0,0.3);
    margin-bottom:25px;
}

.btn{
    background:#ff006e;
    color:white;
    border:none;
    padding:15px 35px;
    font-size:1.2rem;
    border-radius:30px;
    cursor:pointer;
    margin:10px;
    transition:0.3s;
    box-shadow:0 5px 10px rgba(0,0,0,0.2);
}

.btn:hover{
    transform:scale(1.08);
    background:#d90459;
}

.caja{
    background:white;
    width:90%;
    max-width:800px;
    padding:30px;
    border-radius:25px;
    box-shadow:0 0 20px rgba(0,0,0,0.2);
}

.cerrar{
    background:red;
    color:white;
    width:45px;
    height:45px;
    border:none;
    border-radius:50%;
    font-size:22px;
    cursor:pointer;
    float:right;
}

.info-img{
    width:300px;
    max-width:100%;
    border-radius:20px;
    margin-bottom:20px;
}

.galeria{
    display:flex;
    flex-wrap:wrap;
    justify-content:center;
    gap:15px;
    margin-top:20px;
}

.galeria img{
    width:220px;
    height:220px;
    object-fit:cover;
    border-radius:15px;
    box-shadow:0 0 10px rgba(0,0,0,0.3);
}

h2{
    color:#ff006e;
    margin-bottom:20px;
}

p{
    font-size:1.1rem;
    line-height:1.7;
}
</style>
</head>

<body>

<!-- PÁGINA PRINCIPAL -->
<div id="inicio" class="pantalla activa">

    <h1>ALFAJORES</h1>

    <img class="imagen-principal"
    src="https://www.somewhatsimple.com/wp-content/uploads/2019/08/alfajores_1.jpg">

    <button class="btn" onclick="mostrar('menu')">
        Comenzar
    </button>

</div>

<!-- MENÚ -->
<div id="menu" class="pantalla">

    <div class="caja">

        <h2>Bienvenido</h2>

        <button class="btn" onclick="mostrar('informacion')">
            Información
        </button>

        <button class="btn" onclick="mostrar('contacto')">
            Contáctanos
        </button>

        <button class="btn" onclick="mostrar('fotos')">
            Fotos
        </button>

    </div>

</div>

<!-- INFORMACIÓN -->
<div id="informacion" class="pantalla">

    <div class="caja">

        <button class="cerrar" onclick="mostrar('menu')">
            ✖
        </button>

        <br><br>

        <!-- Reemplaza esta imagen por la tuya -->
        <img src="img/abuela.png" class="info-img">

        <h2>Nuestra Historia</h2>

        <p>
            Los alfajores son un símbolo de identidad cultural y un símbolo de cariño familiar.
            Por varios siglos han sido un motor económico, sin embargo en nuestro emprendimiento
            queremos recordarles su niñez, cuando su abuela cocinaba con ese amor mientras nosotros
            en nuestra pequeñez le robábamos esa comida, queremos que recuerden que la comida también
            es amor y no es necesario ser pequeños para sentir nuevamente ese cariño.
        </p>

    </div>

</div>

<!-- CONTACTO -->
<div id="contacto" class="pantalla">

    <div class="caja">

        <button class="cerrar" onclick="mostrar('menu')">
            ✖
        </button>

        <br><br>

        <h2>Contáctanos</h2>

        <p>
            <strong>Dirección:</strong> Transversal 9 # 57 N 300, Popayán
            <br><br>

            <strong>Número:</strong> 3053812345
            <br><br>

            <strong>Horario:</strong> 9:00 AM - 5:00 PM
            <br><br>

            ¡Te esperamos!
        </p>

    </div>

</div>

<!-- FOTOS -->
<div id="fotos" class="pantalla">

    <div class="caja">

        <button class="cerrar" onclick="mostrar('menu')">
            ✖
        </button>

        <br><br>

        <h2>Formas y figuras divertidas para comer</h2>

        <div class="galeria">

            <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcSQoOHf2DwmuPOsu9jNBBhliRsmHztEavJ48obcpMWwrw&s=10">

            <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcTr3c_fGax5Oc-TeMmwPQah9W8qAiCJ5OKfMa_aA8uBTjHd_DBkUpLiYtZl&s=10">

            <img src="https://www.modernhoney.com/wp-content/uploads/2023/12/Alfajores-3-crop-500x500.jpg">

        </div>

    </div>

</div>

<script>

function mostrar(id){

    let pantallas =
    document.querySelectorAll('.pantalla');

    pantallas.forEach(p=>{
        p.classList.remove('activa');
    });

    document
    .getElementById(id)
    .classList.add('activa');
}

</script>

</body>
</html>
