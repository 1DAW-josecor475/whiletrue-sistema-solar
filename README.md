# Sistema Solar Meme ☀

Esta es una representación del sistema solar utilizando HTML y CSS. Los planetas están animados para girar alrededor del sol.

## Descripción

Este proyecto muestra una simulación simple de un sistema solar con planetas que orbitan alrededor del sol. Utiliza un fondo de espacio y representaciones gráficas de algunos personajes divertidos como planetas.

## Tecnologías

- HTML
- CSS

## Demo

Aquí tienes una vista previa directa de la representación del sistema solar:

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>AAAAAAA</title>
    <style>
        .container {
            display: flex;
            justify-content: center;
            align-items: center;
        }
        body {
            background: url('https://images.pexels.com/photos/3214110/pexels-photo-3214110.jpeg?cs=srgb&dl=pexels-frank-cone-140140-3214110.jpg&fm=jpg');
            color: #FFFA;
            margin: 0;
            width: 100vw;
        }
        ol {
            all: unset;
            aspect-ratio: 1 / 1;
            container-type: inline-size;
            display: grid;
            width: 50%;
            align-items: center;
            justify-content: center;
        }
        li {
            aspect-ratio: 1 / 1;
            border: 1px dashed;
            border-radius: 50%;
            display: grid;
            grid-area: 1 / 1;
            place-self: center;
            width: var(--d, 2cqi);
        }
        li::after {
            aspect-ratio: 1 / 1;
            background: var(--b, hsl(0, 0%, 50%));
            border-radius: 50%;
            box-shadow: 0 0 15px rgba(0, 0, 0, 0.3);
            content: '';
            display: block;
            offset-path: content-box;
            width: var(--w, 2cqi);
        }

        @keyframes spin {
            from {
                rotate: 0deg;
            }
            to {
                rotate: 360deg;
            }
        }
        @keyframes rotate {
            to {
                offset-distance: 100%;
            }
        }

        @keyframes rotate-doraemon {
            to {
                offset-distance: 125%;
            }
        }
        
        @keyframes rotate-webiwabo {
            to {
                offset-distance: 150%;
            }
        }
        @keyframes rotate-gustavo {
            to {
                offset-distance: 175%;
            }
        }

        .sun {
            --b: url('images/proxmox_se_ha_caido.jpg');
            --d: 30cqi;
            --w: 30cqi;
            border: 0;
            
        }
        .sun::after {
            animation: spin 6s linear infinite;
            background-size: cover;
            background-position: center;
            offset-path: none;
            place-self: center;
            box-shadow: 0px 0px 33px 0px #FAB12F, 
                        0px 0px 66px 0px #FCF596,
                        0px 0px 99px 0px #FBFBFB;
        }
        .pikachu {
            --b: url('images/pikachu.webp');
            --d: 75cqi;
            --t: 6315.79ms;
            --w: 10cqi;
        }
        .doraemon {
            --b: url('images/doraemon.jpg');
            --d: 75cqi;
            --t: 6315.79ms;
            --w: 10cqi;
            --offset-start: 25%;
        }
        .webiwabo {
            --b: url('images/webiwabo.webp');
            --d: 75cqi;
            --t: 6315.79ms;
            --w: 10cqi;
            --offset-start: 50%;
        }
        .gustavo {
            --b: url('images/gustavo.jpg');
            --d: 75cqi;
            --t: 6315.79ms;
            --w: 10cqi;
            --offset-start: 75%;
        }
        .pikachu::after {
            animation: rotate var(--t, 3s) linear infinite;
            background-size: cover;
            background-position: center;
            place-self: center;
            offset-distance: 0%;
        }
        .doraemon::after {
            animation: rotate-doraemon var(--t, 3s) linear infinite;
            background-size: cover;
            background-position: center;
            place-self: center;
            offset-distance: 25%;
        }
        .webiwabo::after {
            animation: rotate-webiwabo var(--t, 3s) linear infinite;
            background-size: cover;
            background-position: center;
            place-self: center;
            offset-distance: 50%;
        }
        .gustavo::after {
            animation: rotate-gustavo var(--t, 3s) linear infinite;
            background-size: cover;
            background-position: center;
            place-self: center;
            offset-distance: 75%;
        }
    </style>
</head>
<body>
    <div class="container">
        <ol>
            <li class="sun"></li>
            <li class="pikachu"></li>
            <li class="doraemon"></li>
            <li class="webiwabo"></li>
            <li class="gustavo"></li>
        </ol>
    </div>
</body>
</html>

## Cómo usar

1. Clona el repositorio en tu máquina local.
2. Abre el archivo `index.html` en tu navegador web para ver la simulación.

```bash
git clone https://github.com/tu-usuario/tu-repositorio.git
cd tu-repositorio
open index.html