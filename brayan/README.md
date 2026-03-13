# Abogado Estudiantil IA - Brayan

## Tu misión
Crear una página web donde un estudiante pueda describir una sanción que recibió y el sistema analice si fue justa según el manual de convivencia del colegio.

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
- Un título grande que diga "¿Tu sanción fue justa?"
- Un subtítulo que diga "Analiza si la sanción que recibiste cumple con el manual de convivencia"
- Un formulario con: qué sanción recibiste (anotación en observador, citación a acudientes, suspensión, otra), qué hiciste según el profesor, tu versión de los hechos (campo grande de texto), te escucharon antes de la sanción (sí, no), y un botón que diga "Analizar sanción"
- Un área vacía abajo donde aparecerá el análisis
- Diseño con colores rojo oscuro y dorado, que se vea como un tribunal de justicia
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
6. El estudiante tiene derecho a presentar descargos.

CAPÍTULO 2 - PROCESO DISCIPLINARIO
1. Ante una falta, el profesor debe dialogar primero con el estudiante.
2. Se debe dejar constancia escrita de la falta y la versión del estudiante.
3. La sanción debe corresponder al tipo de falta (leve, grave, muy grave).
4. El acudiente debe ser informado en caso de faltas graves.
5. El estudiante puede apelar cualquier sanción ante el comité de convivencia.

CAPÍTULO 3 - FALTAS Y SANCIONES
Falta leve: Llamado de atención verbal. No genera anotación.
Falta grave: Anotación en el observador. Citación a acudientes.
Falta muy grave: Suspensión temporal. Matrícula condicional."

Esto es temporal, después lo reemplazaré con el manual real.
```

**Mensaje 3 - Analizar si la sanción fue justa:**
```
Modifica el código para que cuando el usuario presione "Analizar sanción", el sistema:
1. Compare la sanción recibida con el tipo de falta según el manual
2. Verifique si se cumplió el debido proceso (¿lo escucharon? ¿le informaron?)
3. Muestre un veredicto con semáforo: verde (sanción justa), amarillo (sanción desproporcionada), rojo (se violaron derechos del estudiante)
4. Liste qué artículos del manual aplican al caso
5. Dé una recomendación de qué puede hacer el estudiante

Muestra todo con buen formato, emojis de justicia (⚖️ ✅ ❌ ⚠️) y colores claros.
```

**Mensaje 4 - Comparador de casos:**
```
Agrega una sección que diga "Casos anteriores similares" que guarde cada consulta y cuando se haga una nueva, busque si hay casos parecidos ya analizados y los muestre. Guarda los casos en una lista en JavaScript con: fecha, falta, sanción, veredicto (justa/injusta).
```

**Mensaje 5 - Estadísticas de justicia:**
```
Agrega arriba del formulario un panel de estadísticas que muestre: total de casos analizados, porcentaje de sanciones justas vs injustas (con una barra de progreso verde/rojo), y cuál es el derecho que más se viola. Que se actualice cada vez que se analiza un nuevo caso.
```

### Paso 3 - Sube tu código
1. Ve a tu carpeta `brayan/` en el repo `revisor-convivencia`
2. Crea un archivo `index.html`
3. Pega todo el código que generó Copilot
4. Haz commit
5. **IMPORTANTE:** Después consigue el manual de convivencia real y reemplaza el texto de la variable `manualConvivencia` con las normas reales del Salesiano

### Paso 4 - Verifica
Abre tu página en GitHub Pages, prueba ingresando un caso y verifica que el semáforo de justicia funcione.
