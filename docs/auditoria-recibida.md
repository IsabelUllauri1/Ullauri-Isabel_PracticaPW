# Informe de auditoría – Parte 2

## 1. Datos generales

Auditor: Andres Villalta Pardo

Compañero auditado: Isabel Ullauri

Repositorio: https://github.com/IsabelUllauri1/Ullauri-Isabel_PracticaPW

Página auditada: AutoServicio – Taller mecánico

## 2. Método de revisión

Se revisó el código HTML y CSS proporcionado. Se analizaron la estructura semántica, el formulario, la tabla de precios, el diseño adaptable, las variables CSS y los estilos de foco. Para completar la auditoría, también se deben verificar los resultados de los validadores W3C, la navegación con teclado y los requisitos de la ficha personalizada.

## 3. Hallazgos

| N.º | Requisito | Ubicación (archivo y selector) | Hallazgo | Norma que incumple | Evidencia | Severidad |
|---|---|---|---|---|---|---|
| 1 | Base 1: estructura HTML | `index.html`, sección `#servicios` | El párrafo introductorio de los servicios adicionales está dentro de `<ul>`, cuando debe colocarse fuera de la lista. | WHATWG HTML | Fragmento de código de la lista de servicios adicionales. | Media |

### Hallazgo 1: estructura incorrecta de la lista

En la sección de servicios adicionales, el párrafo que introduce los servicios se encuentra dentro del elemento `<ul>`. Una lista debe contener sus elementos de lista `<li>` y no ese párrafo como hijo directo.

Código observado:

```html
<ul>
    <p>Tambien ofrecemos sevicios adicionales como:</p>
    <li>Lavado del vehículo</li>
    <li>Revisión de batería</li>
    <li>Revisión de neumáticos</li>
</ul>
```

La estructura puede corregirse colocando el párrafo antes de la lista:

```html
<p>También ofrecemos servicios adicionales como:</p>
<ul>
    <li>Lavado del vehículo</li>
    <li>Revisión de batería</li>
    <li>Revisión de neumáticos</li>
</ul>
```

## 4. Revisión de los requisitos base

### Base 1. Estructura semántica

La página utiliza `header`, `nav`, `main`, `section`, `aside` y `footer`. También contiene encabezados para las secciones principales. Se identificó el problema de estructura dentro de la lista de servicios adicionales. La jerarquía completa de encabezados debe revisarse según la organización del contenido.

### Base 2. Formulario

El formulario contiene campos para nombre, correo electrónico, placa del vehículo, kilometraje y fecha de preferencia. Los campos principales tienen etiquetas asociadas y se utilizan atributos como `required`, `pattern`, `min`, `max` y `step`. Además, los controles de selección se agrupan mediante `fieldset` y `legend`.

### Base 3. Tabla

La tabla de precios incluye `caption`, `thead`, `tbody` y encabezados con `scope` para identificar los servicios y sus datos. Estos elementos corresponden a los requisitos de estructura de una tabla de datos.

### Base 4. Diseño adaptable

La hoja de estilos utiliza CSS Grid para organizar el contenido principal y Flexbox para distribuir los enlaces de navegación. También se utiliza una regla `@media` para cambiar la distribución a una columna cuando el ancho de pantalla es de 1024 píxeles o menos. Es necesario probar la página a 360 píxeles para comprobar si existe desplazamiento horizontal.

### Base 5. Variables CSS y contraste

Se utilizan variables CSS para los colores y el espaciado, por ejemplo `--color-principal`, `--color-texto` y `--espaciado`. Sin embargo, el contraste mínimo de 4.5:1 debe comprobarse con una herramienta de contraste antes de confirmar su cumplimiento.

### Base 6. Navegación con teclado

El CSS define estilos de foco mediante `:focus-visible` para los enlaces de navegación, los botones y los campos de entrada. Se debe recorrer toda la página usando `Tab` y `Shift + Tab` para comprobar que todos los elementos interactivos puedan utilizarse con teclado y que el foco sea visible.

### Base 7. Validación HTML y CSS

El código debe verificarse con los validadores oficiales de W3C. No se puede confirmar que existan cero errores hasta ejecutar ambas validaciones y guardar sus resultados como evidencia.

### Base 8. Texto alternativo de imágenes

La imagen del taller incluye un atributo `alt` que describe el contenido de la imagen. Debe comprobarse que esa descripción sea adecuada para la imagen que realmente se muestra.

## 5. Revisión de los requisitos personalizados

La ficha personalizada del compañero debe consultarse para verificar el campo especial del formulario, el punto de ruptura principal y la restricción adicional. Estos requisitos no pueden confirmarse únicamente con el código proporcionado.

## 6. Evidencias

Las evidencias de la auditoría deben guardarse en la carpeta `docs/evidencias/` e incluir:

1. Captura del código HTML que muestra el problema de la lista.
2. Captura del resultado del validador HTML de W3C.
3. Captura del resultado del validador CSS de W3C.
4. Captura de la página en un ancho de 360 píxeles.
5. Captura de la navegación con teclado o del foco de un elemento interactivo.
6. Evidencia adicional de los requisitos personalizados, si corresponde.

## 7. Conclusión

La revisión del código de AutoServicio permitió identificar un problema en la estructura HTML de la lista de servicios adicionales. También se observó el uso de elementos semánticos, un formulario con validaciones nativas, una tabla estructurada y técnicas de diseño adaptable.

Para determinar el cumplimiento completo de los requisitos, es necesario finalizar las pruebas con los validadores, comprobar la accesibilidad mediante teclado, medir el contraste de colores y revisar la ficha personalizada del compañero. Las conclusiones finales deben basarse en los resultados y las evidencias obtenidas durante esas pruebas.