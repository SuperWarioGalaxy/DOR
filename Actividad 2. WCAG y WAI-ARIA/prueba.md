Actividad 2. WCAG y WAI-ARIA

A continuación te ofrezco las modificaciones necesarias en el código de cada ejercicio para que cumplan con los estándares de accesibilidad de WCAG y WAI-ARIA. He agregado las etiquetas y atributos que mejoran la accesibilidad de los contenidos para usuarios con discapacidades.
Ejercicio 1: Imagen sin texto alternativo

<!DOCTYPE html>
<html lang="es">
<head>
  <title>Galería de Fotos</title>
</head>
<body>
  <h1>Galería de Fotos</h1>
  <img src="playa.jpg" alt="Vista de la playa al atardecer">
  <img src="montana.jpg" alt="Montaña cubierta de nieve bajo un cielo claro">
</body>
</html>

Cambios realizados:

    Se añadió el atributo alt con descripciones breves y claras para cada imagen.

Ejercicio 2: Formulario sin etiquetas y mensajes de error

<!DOCTYPE html>
<html lang="es">
<head>
  <title>Registro</title>
</head>
<body>
  <h1>Formulario de Registro</h1>
  <form>
    <div>
      <label for="nombre">Nombre</label>
      <input type="text" id="nombre" name="nombre" placeholder="Nombre" required>
    </div>
    <div>
      <label for="email">Correo electrónico</label>
      <input type="email" id="email" name="email" placeholder="Correo electrónico" required>
    </div>
    <div>
      <button type="submit">Enviar</button>
    </div>
  </form>
</body>
</html>

Cambios realizados:

    Se añadieron etiquetas label con el atributo for que se asocia con el id de cada campo.
    Se incluyó el atributo required en los campos para indicar que son obligatorios.

Ejercicio 3: Botón que no es accesible para lectores de pantalla

<!DOCTYPE html>
<html lang="es">
<head>
  <title>Botón</title>
</head>
<body>
  <h1>Interacción</h1>
  <button onclick="alert('¡Botón presionado!')" aria-label="Presionar el botón para mostrar mensaje">
    Presionar
  </button>
</body>
</html>

Cambios realizados:

    Se sustituyó el div por un botón <button>, ya que es un elemento más semántico para acciones de este tipo.
    Se añadió el atributo aria-label para describir la acción del botón para los lectores de pantalla.

Ejercicio 4: Navegación sin estructura semántica

<!DOCTYPE html>
<html lang="es">
<head>
  <title>Navegación</title>
</head>
<body>
  <nav>
    <ul>
      <li><a href="#">Inicio</a></li>
      <li><a href="#">Servicios</a></li>
      <li><a href="#">Contacto</a></li>
    </ul>
  </nav>
</body>
</html>

Cambios realizados:

    Se añadió el elemento <nav> para denotar la sección de navegación.
    Se estructuró la navegación con una lista no ordenada <ul> y elementos de lista <li>, dentro de la cual cada opción es un enlace <a>.

Ejercicio 5: Tabla sin encabezados

<!DOCTYPE html>
<html lang="es">
<head>
  <title>Tabla</title>
</head>
<body>
  <h1>Lista de Precios</h1>
  <table>
    <thead>
      <tr>
        <th>Producto</th>
        <th>Precio</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td>Producto 1</td>
        <td>10 USD</td>
      </tr>
      <tr>
        <td>Producto 2</td>
        <td>20 USD</td>
      </tr>
    </tbody>
  </table>
</body>
</html>

Cambios realizados:

    Se añadió el elemento <thead> para los encabezados de la tabla, con las celdas <th> correspondientes.
    El contenido de la tabla se incluyó dentro del <tbody>.

Ejercicio 6: Contenido dinámico sin notificación

<!DOCTYPE html>
<html lang="es">
<head>
  <title>Notificaciones</title>
  <script>
    function mostrarNotificacion() {
      document.getElementById('notificacion').innerText = 'Cambio guardado';
      document.getElementById('notificacion').setAttribute('role', 'alert');
    }
  </script>
</head>
<body>
  <button onclick="mostrarNotificacion()">Guardar</button>
  <div id="notificacion"></div>
</body>
</html>

Cambios realizados:

    Se añadió el atributo role="alert" al div que muestra la notificación, lo que indica a los lectores de pantalla que se trata de un mensaje importante.

Ejercicio 7: Contraste bajo

<!DOCTYPE html>
<html lang="es">
<head>
  <title>Texto</title>
  <style>
    body {
      background-color: #ffffff;
      color: #333333;
    }
  </style>
</head>
<body>
  <h1>Texto fácil de leer</h1>
  <p>Este texto ahora tiene un buen contraste con el fondo para mejorar la legibilidad.</p>
</body>
</html>

Cambios realizados:

    Se cambió el color del texto a un gris oscuro (#333333) sobre un fondo blanco (#ffffff) para mejorar el contraste y la legibilidad.

Ejercicio 8: Lista desplegable sin indicar su estado

<!DOCTYPE html>
<html lang="es">
<head>
  <title>Menú</title>
  <style>
    .submenu {
      display: none;
    }
    .menu:hover .submenu {
      display: block;
    }
  </style>
</head>
<body>
  <h1>Menú</h1>
  <div class="menu" aria-haspopup="true" aria-expanded="false">
    Opciones
    <div class="submenu" role="menu">
      <p role="menuitem">Opción 1</p>
      <p role="menuitem">Opción 2</p>
    </div>
  </div>
</body>
</html>

Cambios realizados:

    Se añadió aria-haspopup="true" y aria-expanded="false" al contenedor del menú para indicar que contiene un submenú y su estado.
    Se añadió role="menu" al contenedor del submenú y role="menuitem" a las opciones, para definir su función semántica.

Ejercicio 9: Página con contenido multimedia

<!DOCTYPE html>
<html lang="es">
<head>
  <title>Video Educativo</title>
</head>
<body>
  <h1>Cómo cocinar pasta</h1>
  <video controls>
    <source src="video.mp4" type="video/mp4">
    <track kind="subtitles" src="subtitulos_es.vtt" srclang="es" label="Español">
  </video>
</body>
</html>

Cambios realizados:

    Se añadió un subtítulo (<track>) para mejorar la accesibilidad del contenido de video.

Ejercicio 10: Página dinámica sin accesibilidad

<!DOCTYPE html>
<html lang="es">
<head>
  <title>Notificaciones</title>
  <script>
    function mostrarMensaje() {
      document.getElementById('mensaje').innerText = '¡Nueva notificación!';
      document.getElementById('mensaje').setAttribute('role', 'alert');
    }
  </script>
</head>
<body>
  <h1>Página de Notificaciones</h1>
  <button onclick="mostrarMensaje()">Mostrar Notificación</button>
  <div id="mensaje"></div>
</body>
</html>

Cambios realizados:

    Se añadió el atributo role="alert" al div de notificación para alertar a los lectores de pantalla.

Ejercicio 11: Página web de un producto

<!DOCTYPE html>
<html lang="es">
<head>
  <title>Zapatos Deportivos</title>
  <style>
    body {
      font-family: Arial, sans-serif;
    }
    .precio {
      font-size: 20px;
      color: red;
    }
    .boton {
      background-color: blue;
      color: white;
      padding: 10px;
      cursor: pointer;
    }
  </style>
</head>
<body>
  <div>
    <h1>Zapatos Deportivos</h1>
    <div>
      <img src="zapatos.jpg" alt="Zapatos deportivos de color azul">
      <p>Los mejores zapatos para correr.</p>
      <p class="precio">Precio: $50</p>
    </div>
    <button class="boton" onclick="alert('Producto añadido al carrito')" aria-label="Añadir al carrito">Añadir al carrito</button>
  </div>
</body>
</html>

Cambios realizados:

    Se añadió el atributo alt en la imagen con una descripción adecuada.
    Se cambió el div del botón por un <button> y se añadió el atributo aria-label.

Ejercicio 12: Blog con múltiples secciones

<!DOCTYPE html>
<html lang="es">
<head>
  <title>Mi Blog</title>
</head>
<body>
  <header>
    <nav>
      <ul>
        <li><a href="#">Inicio</a></li>
        <li><a href="#">Sobre mí</a></li>
        <li><a href="#">Contacto</a></li>
      </ul>
    </nav>
  </header>
  <main>
    <section>
      <h2>Artículo Reciente</h2>
      <p>Este es el contenido del artículo. Lorem ipsum dolor sit amet, consectetur adipiscing elit.</p>
      <a href="#">Leer más</a>
    </section>
    <section>
      <h2>Otro Artículo</h2>
      <p>Contenido del segundo artículo. Lorem ipsum dolor sit amet.</p>
      <a href="#">Leer más</a>
    </section>
  </main>
</body>
</html>

Cambios realizados:

    Se añadió un <header> para la navegación principal y un <main> para el contenido principal.
    Se utilizaron <section> para separar los artículos y proporcionar una estructura semántica.

Ejercicio 13: Formulario de inscripción

<!DOCTYPE html>
<html lang="es">
<head>
  <title>Formulario de Inscripción</title>
</head>
<body>
  <h1>Formulario de Inscripción</h1>
  <form>
    <div>
      <label for="nombre">Nombre completo</label>
      <input type="text" id="nombre" placeholder="Nombre completo">
    </div>
    <div>
      <label for="correo">Correo electrónico</label>
      <input type="email" id="correo" placeholder="Correo electrónico">
    </div>
    <div>
      <label for="pais">Seleccionar país</label>
      <select id="pais">
        <option>México</option>
        <option>España</option>
        <option>Colombia</option>
      </select>
    </div>
    <div>
      <button type="submit">Enviar</button>
    </div>
  </form>
</body>
</html>

Cambios realizados:

    Se añadió el atributo for en las etiquetas <label> para asociarlas con sus respectivos campos de formulario.

Ejercicio 14: Tabla de datos compleja

<!DOCTYPE html>
<html lang="es">
<head>
  <title>Reporte de Ventas</title>
</head>
<body>
  <h1>Reporte Mensual de Ventas</h1>
  <table>
    <thead>
      <tr>
        <th>Producto</th>
        <th>Enero</th>
        <th>Febrero</th>
        <th>Marzo</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td>Zapatos</td>
        <td>100</td>
        <td>150</td>
        <td>200</td>
      </tr>
      <tr>
        <td>Camisas</td>
        <td>200</td>
        <td>250</td>
        <td>300</td>
      </tr>
    </tbody>
  </table>
</body>
</html>

Cambios realizados:

    Se añadió una sección <thead> para los encabezados de la tabla, mejorando su estructura y accesibilidad.

Ejercicio 15: Menú interactivo

<!DOCTYPE html>
<html lang="es">
<head>
  <title>Menú Interactivo</title>
  <style>
    .submenu {
      display: none;
    }
    .menu:hover .submenu {
      display: block;
    }
  </style>
</head>
<body>
  <h1>Menú de Opciones</h1>
  <div class="menu" aria-haspopup="true" aria-expanded="false">
    Opciones
    <div class="submenu" role="menu">
      <p role="menuitem">Opción 1</p>
      <p role="menuitem">Opción 2</p>
      <p role="menuitem">Opción 3</p>
    </div>
  </div>
</body>
</html>

Cambios realizados:

    Se añadió aria-haspopup="true" y aria-expanded="false" para indicar que hay un submenú y su estado.
    Se añadieron roles role="menu" y role="menuitem" para los elementos interactivos del menú.