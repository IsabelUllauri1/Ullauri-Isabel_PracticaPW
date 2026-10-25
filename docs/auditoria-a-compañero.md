# Informe de Auditoría

**Página revisada:** Tienda de Artesanías.  
**Archivos revisados:** archivo HTML y archivo CSS.  
**Ficha revisada:** N.º 22   
**Fecha:** 22/10/2026

## 1. Objetivo

Revisar la ficha de el compañero y desde su repositorio y revisar todo para cada requisito base y personalizado
## 2. Revisión de requisitos

| N.º | Requisito            | Qué espero encontrar                          | Severidad                  |
|-----|----------------------|-----------------------------------------------|----------------------------|
| 1   | Diseño responsive    | Uso de grid en la estructura del proyecto     | No cumple                  |
| 2   | Imágenes             | Atributos `alt` adecuados.                    | No aplica: no hay imágenes |
| 3   | Validación HTML      | Identificadores id válidos, sin espacios      | Meido                      |
| 4   | Validación HTML      | Encabezados de tablabien escritos             | Medio                      |
| 5   | Enlace de navegación | desplazarse con botons a diferentes secciones | No cumple                  |
## 3. Hallazgos de auditoría

### Hallazgo 1: Falta de CSS Grid en la estructura general

**Requisito:** 4 – Diseño responsive.

**Ubicación:** `estilos.css`.

**Qué esperaba encontrar:** uso de CSS Grid para la estructura general y Flexbox para al menos un componente interno, manteniendo un diseño adaptable.

**Hallazgo:** el archivo CSS utiliza `display: flex` en el menú de navegación, pero no implementa `display: grid` para organizar la estructura general.   

**Norma que incumple:** requisito #4 del profesor, relacionado con CSS Grid Layout.

**Evidencia:**  ![Código donde está el error](C:\Users\Usuario\IdeaProjects\Ullauri-Isabel\img\grid.png)


**Severidad:** Alta.


### Hallazgo 2: Ausencia de imágenes en la página

**Requisito:** Base 8 

**Ubicación:** `index.html`, contenido de la página.

**Qué esperaba encontrar:** que las imágenes informativas incluyan un  `alt` descriptivo y que las imágenes decorativas utilicen `alt=""` cuando corresponda.

**Hallazgo:** no se identificaron imagenes en el código HTML revisado. Por lo tanto, no es posible evaluar el uso del atributo `alt`. 

**Norma de referencia:** WCAG 2.2, criterio 1.1.1 

**Evidencia:** En el código no existen elementos `<img>`.

### Hallazgo 3: Identificadores HTML con espacios

**Requisito:** Base 7 

**Ubicación:** `index.html`, líneas 22 y 27.

**Qué esperaba encontrar:** identificadores `id` válidos, sin espacios, que permitan reconocer correctamente las secciones de la página.

**Hallazgo:** el validador W3C detectó dos errores porque los identificadores de las secciones contienen espacios.


`<section id="Productos ">`
`<section id=" Precios ">`


**Norma que incumple:** HTML Living Standard, atributo global `id`.

**Evidencia:** ![Captura de validador](C:\Users\Usuario\IdeaProjects\Ullauri-Isabel\img\validacionID.png)

**Severidad:** Media.



### Hallazgo 4: Valores incorrectos en el atributo `scope`

**Requisito:** Base 3 – Tabla de datos y Base 7 – Validación HTML.

**Ubicación:** `index.html`, líneas 33, 34 y 35.

**Qué esperaba encontrar:** encabezados de tabla que utilicen correctamente `scope="col"`.

**Hallazgo:** el validador W3C identificó tres errores en los encabezados de la tabla debido al espacio adicional en el valor del atributo `scope`.

`<th scope=" col">Talleres</th>`
`<th scope=" col">Duracion</th>`
`<th scope=" col">Precio</th>`

**Norma que incumple:** HTML Living Standard, atributo `scope` del elemento `th`. Relacionado con WCAG 2.2, criterio 1.3.1 (Información y relaciones).

**Evidencia:** ![Captura de validador](C:\Users\Usuario\IdeaProjects\Ullauri-Isabel\img\validacionS.png)

**Severidad:** Media.

### Hallazgo 5: Enlaces de navegación incorrectos

**Requisito:** Base 6 – Navegación.

**Ubicación:** index.html,  etiquetas `<a>` del menú de navegación y atributos id de las secciones.

Qué esperaba encontrar: que los enlaces del menú permitan desplazarse a sus secciones correspondientes.

**Hallazgo:** los enlaces de navegación no llevan a las secciones correspondientes porque los valores

**Norma que incumple:** requisito de navegación del profesor. HTML Living Standard (enlaces internos).

**Severidad:** Media

## 4. Aspectos implementados correctamente

- La página contiene las etiquetas semánticas principales.
- La jerarquía de encabezados utiliza H1 y H2 correctamente.
- El formulario contiene cinco campos con sus respectivas etiquetas.
- Se utilizan los tipos date, time y email.
- El formulario incorpora required, fieldset y legend.
- El menú utiliza Flexbox.
- Los colores están definidos mediante variables CSS.

## 5. Conclusión

La página de la Tienda de Artesanías cumple varios requisitos de estructura HTML, formulario. Sin embargo, se identificaron problemas en la navegación interna, los atributos scope de la tabla y la ausencia de CSS Grid para la estructura general, tambien hay ausencia de imagenes y errores en los encabezados .


Se recomienda corregir los errores confirmados y completar las pruebas pendientes para garantizar el cumplimiento de los estándares web solicitados por el profesor.