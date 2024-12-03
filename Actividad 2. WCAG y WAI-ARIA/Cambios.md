Actividad 2. WCAG y WAI-ARIA

Ejercicio 1: Imagen sin texto alternativo

- Cambios realizados:

    Se añadió el atributo alt con descripciones breves y claras para cada imagen.

Ejercicio 2: Formulario sin etiquetas y mensajes de error

- Cambios realizados:

    Se añadieron etiquetas label con el atributo for que se asocia con el id de cada campo.
    Se incluyó el atributo required en los campos para indicar que son obligatorios.

Ejercicio 3: Botón que no es accesible para lectores de pantalla

- Cambios realizados:

    Se sustituyó el div por un botón <button>, ya que es un elemento más semántico para acciones de este tipo.
    Se añadió el atributo aria-label para describir la acción del botón para los lectores de pantalla.

Ejercicio 4: Navegación sin estructura semántica

- Cambios realizados:

    Se añadió el elemento <nav> para denotar la sección de navegación.
    Se estructuró la navegación con una lista no ordenada <ul> y elementos de lista <li>, dentro de la cual cada opción es un enlace <a>.

Ejercicio 5: Tabla sin encabezados

- Cambios realizados:

    Se añadió el elemento <thead> para los encabezados de la tabla, con las celdas <th> correspondientes.
    El contenido de la tabla se incluyó dentro del <tbody>.

Ejercicio 6: Contenido dinámico sin notificación

- Cambios realizados:

    Se añadió el atributo role="alert" al div que muestra la notificación, lo que indica a los lectores de pantalla que se trata de un mensaje importante.

Ejercicio 7: Contraste bajo

- Cambios realizados:

    Se cambió el color del texto a un gris oscuro (#333333) sobre un fondo blanco (#ffffff) para mejorar el contraste y la legibilidad.

Ejercicio 8: Lista desplegable sin indicar su estado

- Cambios realizados:

    Se añadió aria-haspopup="true" y aria-expanded="false" al contenedor del menú para indicar que contiene un submenú y su estado.
    Se añadió role="menu" al contenedor del submenú y role="menuitem" a las opciones, para definir su función semántica.

Ejercicio 9: Página con contenido multimedia

- Cambios realizados:

    Se añadió un subtítulo (<track>) para mejorar la accesibilidad del contenido de video.

Ejercicio 10: Página dinámica sin accesibilidad

- Cambios realizados:

    Se añadió el atributo role="alert" al div de notificación para alertar a los lectores de pantalla.

Ejercicio 11: Página web de un producto

- Cambios realizados:

    Se añadió el atributo alt en la imagen con una descripción adecuada.
    Se cambió el div del botón por un <button> y se añadió el atributo aria-label.

Ejercicio 12: Blog con múltiples secciones

- Cambios realizados:

    Se añadió un <header> para la navegación principal y un <main> para el contenido principal.
    Se utilizaron <section> para separar los artículos y proporcionar una estructura semántica.

Ejercicio 13: Formulario de inscripción

- Cambios realizados:

    Se añadió el atributo for en las etiquetas <label> para asociarlas con sus respectivos campos de formulario.

Ejercicio 14: Tabla de datos compleja

- Cambios realizados:

    Se añadió una sección <thead> para los encabezados de la tabla, mejorando su estructura y accesibilidad.

Ejercicio 15: Menú interactivo

- Cambios realizados:

    Se añadió aria-haspopup="true" y aria-expanded="false" para indicar que hay un submenú y su estado.
    Se añadieron roles role="menu" y role="menuitem" para los elementos interactivos del menú.
