# Pass.inn · Paquetes de marca

Landing de **ICI.lab** (Laboratorio de Innovación y Emprendimiento Agroempresarial, SENA) donde cada emprendedor del programa **Pass.inn, Pasaporte a la innovación** encuentra su logo y abre en Google Drive su paquete de redes sociales.

Es una página estática (HTML, CSS y JavaScript sin dependencias) publicada con GitHub Pages.

## Agregar o editar un emprendimiento

1. Abre `index.html` y busca `const EMPRENDIMIENTOS`.
2. Agrega una línea por emprendimiento:

   ```js
   { nombre:"Café La Montaña", sector:"Café de origen",
     drive:"https://drive.google.com/drive/folders/XXXX",
     logo:"img/logos/cafe-la-montana.png",
     color:"#6b3f1f",
     piezas:["Logo PNG/PDF","12 posts","4 historias"] },
   ```

   | Campo    | Qué es |
   |----------|--------|
   | `nombre` | Nombre del emprendimiento |
   | `sector` | A qué se dedica |
   | `drive`  | Enlace a su carpeta de Drive. Vacío (`""`) muestra "En preparación" |
   | `logo`   | Opcional. Ruta al logo dentro de `img/logos/`. Si falta, se muestran las iniciales |
   | `color`  | Color del círculo de iniciales cuando no hay logo |
   | `piezas` | Lo que incluye el paquete |

3. Sube el logo a `img/logos/` (PNG o JPG cuadrado, unos 300×300 px).
4. Guarda el cambio (commit). La página se actualiza en uno o dos minutos.

## Contacto de ayuda

En `index.html`, busca `const CONTACTO` y llena el WhatsApp (con indicativo, ej. `573001234567`) y/o el correo del laboratorio.

## Privacidad

- Este repositorio es **público**. Nunca agregues correos, teléfonos ni datos personales de los emprendedores.
- Cada carpeta de Drive debe estar en **acceso restringido** y compartida solo con el correo del emprendedor, con rol *Lector*.
- Publica nombres y logos solo con autorización de cada emprendedor (Ley 1581 de 2012).

## Estructura

```
index.html            Página completa (estilos, datos y animaciones)
img/                  Logos de ICI.lab y Pass.inn y poses de la mascota
img/logos/            Logos de los emprendimientos
og-image.jpg          Imagen de vista previa al compartir el enlace
favicon.png           Ícono de la pestaña
apple-touch-icon.png  Ícono al guardar la página en el celular
```

## Probar en el computador

```bash
ruby -run -e httpd . -p 8765
```

Luego abre http://localhost:8765.
