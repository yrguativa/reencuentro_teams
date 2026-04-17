# reencuentro_teams

## Descripción del Proyecto

Este proyecto es una aplicación web de marcador de equipos diseñada para gestionar puntuaciones acumuladas en pruebas o rondas. Está optimizada para 4 equipos y permite registrar puntos por ronda, visualizar el historial y analizar los resultados mediante gráficos.

## Características

- **Puntuación**: Interfaz para ingresar puntos por equipo en cada ronda, con confirmación y limpieza de campos.
- **Historial**: Tabla que muestra todas las rondas confirmadas, con totales acumulados y opción de eliminar rondas.
- **Gráfica**: Visualización de datos mediante gráficos de barras (totales), líneas (evolución) y pastel (distribución porcentual).
- **Persistencia**: Los datos se guardan automáticamente en el almacenamiento local del navegador.
- **Responsive**: Diseño adaptable a diferentes tamaños de pantalla.

## Descripción del HTML

El archivo `index.html` contiene toda la aplicación en un solo archivo HTML con estilos CSS embebidos y JavaScript para la funcionalidad.

### Estructura General

- **DOCTYPE y Meta**: Declaración HTML5 con meta tags para charset UTF-8, viewport responsive y título "Marcador de Equipos".
- **Enlaces Externos**: Fuentes de Google Fonts (DM Sans y Space Mono) y Chart.js para gráficos.
- **Estilos CSS**: Variables CSS para colores y tipografía, estilos para layout, tarjetas, botones, tablas y gráficos.
- **Cuerpo HTML**:
  - **Header**: Título "MARCADOR" y subtítulo descriptivo.
  - **Tabs**: Navegación entre las tres secciones principales.
  - **Paneles**: Contenido dinámico para cada tab.

### Secciones Principales

#### Panel de Puntuación (`panel-puntuacion`)
- Muestra el número de la ronda actual.
- Grid de 4 tarjetas, una por equipo (Azul, Amarillo, Verde, Naranja).
- Cada tarjeta incluye:
  - Input para nombre del equipo (editable).
  - Total acumulado.
  - Input para puntos de la ronda actual.
  - Indicador de ranking.
- Botones de acción: Confirmar ronda, Limpiar campos, Reiniciar todo.

#### Panel de Historial (`panel-historial`)
- Tabla con historial de rondas.
- Columnas por equipo con colores distintivos.
- Fila de totales acumulados.
- Botón para eliminar rondas individuales.

#### Panel de Resultados (`panel-resultados`)
- Tres bloques de gráficos usando Chart.js:
  - Gráfico de barras para totales acumulados.
  - Gráfico de líneas para evolución por ronda.
  - Gráfico de pastel para distribución porcentual.
- Leyendas con colores por equipo.

### JavaScript

El código JavaScript maneja:
- Carga y guardado de estado en localStorage.
- Renderizado dinámico de la interfaz.
- Lógica de puntuación y cálculos de totales.
- Inicialización y actualización de gráficos.
- Eventos de usuario (cambio de tabs, confirmación de rondas, etc.).

### Estilos y Diseño

- Tema oscuro con gradientes sutiles de fondo.
- Colores temáticos por equipo.
- Tipografía monospace para números y sans-serif para texto.
- Animaciones suaves y transiciones.
- Diseño mobile-friendly con media queries.

## Uso

1. Abre `index.html` en un navegador web.
2. En la pestaña "Puntuación", ingresa los puntos para cada equipo en la ronda actual.
3. Haz clic en "Confirmar prueba" para guardar la ronda.
4. Usa las otras pestañas para ver el historial y gráficos.
5. Los datos se mantienen entre sesiones gracias al localStorage.
