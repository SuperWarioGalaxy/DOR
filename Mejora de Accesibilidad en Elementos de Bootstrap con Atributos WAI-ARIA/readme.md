## Explicacion mejora boton

Explicación:

    role="button": Define el propósito del elemento como un botón, aunque el elemento button ya tiene este comportamiento, el atributo role refuerza su función.
    aria-label="Enviar formulario": Proporciona una descripción accesible del botón, útil para usuarios de lectores de pantalla.

## Modal

Explicación:

    role="dialog": Especifica que el modal es un cuadro de diálogo interactivo.
    aria-labelledby="modalTitle": Relaciona el título del modal con el contenido del modal, mejorando la navegación y comprensión del contenido.
    aria-describedby="modalDescription": Descripción adicional del modal para proporcionar contexto sobre el contenido.

## menun desplegable

Explicación:

    role="menubar": Indica que el contenedor es un menú.
    aria-haspopup="true": Informa a los usuarios de que el botón abre un menú.
    role="menu" y role="menuitem": Definen los elementos dentro del menú para mejorar la navegación.

## alertas

Explicación:

    aria-live="assertive": Asegura que el mensaje se anuncie inmediatamente a los usuarios de lectores de pantalla.
    aria-atomic="true": Indica que el mensaje completo debe ser leído cuando se actualice, no solo la parte modificada.

## pestañas

Explicación:

    aria-label="Pestañas de navegación": Proporciona un nombre accesible para el conjunto de pestañas.
    aria-labelledby="home-tab", "profile-tab", "contact-tab": Asocia cada pestaña con su etiqueta, mejorando la navegación y comprensión del contenido.