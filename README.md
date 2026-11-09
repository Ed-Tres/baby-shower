# baby-shower
Baby shower website DEV

# Baby Shower de Bellum 🍼

Mesa de regalos digital para el baby shower de Bellum. Los invitados eligen un artículo, lo compran en Amazon y lo reservan en la página para que nadie más lo elija.

🔗 **Sitio:** https://ed-tres.github.io/baby-shower/

## Funciones

**Para invitados**
- Ver la lista de regalos con foto, descripción y precio.
- Filtrar por categoría o buscar un artículo.
- Ordenar por imprescindibles, precio, nombre o disponibilidad.
- Ver los regalos ya reservados con el botón **Reservados**.
- Tocar **Regalar** para ver el artículo en grande, abrir el enlace de Amazon y reservarlo con su nombre.
- Escribir un mensaje opcional de cariño.
- Contactar por WhatsApp con el botón flotante.

**Para la organizadora**
- Entrar al modo organizador con el acceso discreto (círculo en la esquina superior derecha) e iniciar sesión con Google.
- Añadir, editar, duplicar y eliminar artículos.
- Agregar la foto, el enlace de Amazon y el precio de cada artículo.
- Liberar un regalo reservado.
- Editar los datos del evento: título, mensaje, fecha y lugar.
- Restaurar la lista inicial.
- Recibir un correo cada domingo con los regalos que faltan por reservar.

## Tecnologías

- **HTML, CSS y JavaScript** en un solo archivo (`index.html`), sin servidor propio.
- **Tailwind CSS** y **Font Awesome** por CDN.
- **Firebase** (Firestore y Authentication) para guardar las reservas en tiempo real.
- **GitHub Pages** para publicar el sitio gratis.
- **Google Apps Script** para el recordatorio semanal por correo.

## Estructura

baby-shower/
├── index.html # Página completa: diseño, lógica y conexión con Firebase
├── forest.jpg # Imagen del encabezado
└── README.md # Este archivo


## Configuración

La página ya está conectada a un proyecto de Firebase. Si necesitas cambiarlo:

1. Abre `index.html` y busca `const firebaseConfig`.
2. Reemplaza los valores con los de tu proyecto (en Firebase: **Configuración del proyecto → Tus apps → Configuración**).
3. Cambia `ADMIN_EMAIL` por el correo que administrará la lista.
4. Actualiza las reglas de seguridad de Firestore con el mismo correo.

## Actualizar la página

1. Edita `index.html` en GitHub (ícono de lápiz ✏️).
2. Haz clic en **Commit changes**.
3. Espera uno o dos minutos y recarga con **Ctrl + Shift + R**.

## Seguridad

- Cualquier visitante puede reservar un regalo libre, pero no puede cambiar nombres, precios ni eliminar artículos. Esto lo controlan las reglas de Firestore, no el código de la página.
- Solo la cuenta de la organizadora puede editar la lista.
- Las reservas se guardan con el nombre que escribe el invitado. No se pide correo ni teléfono.

## Licencia

Uso personal para el evento. Las imágenes y fotos de productos pertenecen a sus respectivos dueños (Amazon y otras tiendas).
