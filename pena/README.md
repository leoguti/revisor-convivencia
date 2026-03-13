# Abogado Estudiantil IA - Peña

## Tu misión
Crear una página web donde un estudiante pueda describir una situación que le pasó en el colegio y una inteligencia artificial revise el manual de convivencia para decirle qué dice la norma y si es justo.

## Primera tarea: Conseguir el manual
Antes de empezar a programar necesitas el manual de convivencia del Salesiano en digital. Puede ser:
- PDF que te den en coordinación
- Foto de las páginas importantes
- Texto copiado de las normas principales

Guarda el texto de las normas más importantes en un archivo `manual.txt` en esta carpeta.

## Instrucciones

### Paso 1 - Abre GitHub Copilot
1. Ve a **github.com/copilot** en tu navegador
2. Si no lo tienes activado, ve a **github.com/settings/copilot** y actívalo (es gratis)

### Paso 2 - Usa estos 5 mensajes (uno por uno)
Copia cada mensaje, pégalo en el chat de Copilot, y guarda el código que te dé en un archivo `index.html` en esta carpeta.

---

**Mensaje 1 - La página base:**
```
Hazme una página web en HTML con CSS y JavaScript que tenga:
- Un título grande que diga "Abogado Estudiantil IA"
- Un subtítulo que diga "Describe tu situación y te diremos qué dice el manual de convivencia"
- Un formulario con: un campo grande de texto donde el estudiante describe lo que le pasó (placeholder: "Ejemplo: Me quitaron el celular en clase y no me lo devolvieron en todo el día"), y un botón que diga "Consultar mis derechos"
- Un área vacía abajo donde aparecerá la respuesta
- Diseño profesional con colores morados y blancos, que se vea serio como de abogados
- Que sea responsive y se vea bien en celular
```

**Mensaje 2 - Agregar el manual de convivencia:**
```
Agrega al código una variable de JavaScript llamada "manualConvivencia" que sea un texto largo con estas normas del colegio (yo las voy a reemplazar después con las reales):

"CAPÍTULO 1 - DERECHOS DEL ESTUDIANTE
1. Todo estudiante tiene derecho a ser escuchado antes de cualquier sanción.
2. Los objetos decomisados deben ser devueltos al finalizar la jornada escolar.
3. Ningún estudiante puede ser expulsado de clase sin una razón documentada.
4. El estudiante tiene derecho a conocer las pruebas en su contra.
5. Las sanciones deben ser proporcionales a la falta.

CAPÍTULO 2 - DEBERES DEL ESTUDIANTE
1. Respetar a compañeros y profesores.
2. Asistir puntualmente a clases.
3. No usar celular durante las clases sin autorización.
4. Portar el uniforme correctamente.
5. Cuidar las instalaciones del colegio.

CAPÍTULO 3 - FALTAS Y SANCIONES
Falta leve: Llamado de atención verbal.
Falta grave: Anotación en el observador.
Falta muy grave: Citación a acudientes y posible suspensión."

Esto es temporal, después lo reemplazaré con el manual real.
```

**Mensaje 3 - Analizar el caso con el manual:**
```
Modifica el código para que cuando el usuario presione "Consultar mis derechos", el sistema busque en la variable manualConvivencia las palabras clave del caso descrito y muestre:
1. Las normas relacionadas que encontró en el manual
2. Un análisis simple: si la situación descrita parece violar algún derecho del estudiante
3. Una recomendación de qué hacer

Muestra el resultado en el área de respuesta con buen formato: títulos, colores, y separación clara entre cada sección. Usa un icono de balanza de justicia (emoji ⚖️) en el título de la respuesta.
```

**Mensaje 4 - Historial de consultas:**
```
Agrega un historial de consultas debajo del resultado. Cada vez que alguien consulta, se guarda en una lista con: la fecha, el caso descrito (resumido a 50 caracteres), y cuántas normas relacionadas se encontraron. Muestra el historial como una tabla ordenada de más reciente a más antigua.
```

**Mensaje 5 - Casos de ejemplo:**
```
Agrega arriba del formulario una sección que diga "Casos de ejemplo - haz clic para probar:" con 3 botones que tengan estos casos:
- "Me quitaron el celular y no me lo devolvieron"
- "Me sacaron de clase sin explicarme por qué"
- "Me pusieron una sanción sin escuchar mi versión"
Al hacer clic en un botón, se llena automáticamente el campo de texto con ese caso y se ejecuta la consulta.
```

### Paso 3 - Sube tu código
1. Ve a tu carpeta `pena/` en el repo `revisor-convivencia`
2. Crea un archivo `index.html`
3. Pega todo el código que generó Copilot
4. Haz commit
5. **IMPORTANTE:** Después consigue el manual de convivencia real y reemplaza el texto de la variable `manualConvivencia` con las normas reales del Salesiano

### Paso 4 - Verifica
Abre tu página en GitHub Pages, prueba con los casos de ejemplo y verifica que encuentre normas relacionadas.
