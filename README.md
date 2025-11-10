ARQUITECTURA DE SOFTWARE - CATALINA ANGARITA AREVALO
# ⚡ Pokédex - TALLER REST API

Una aplicación web moderna e interactiva para buscar y visualizar información de Pokémon utilizando la [PokéAPI](https://pokeapi.co/). Incluye modo claro/oscuro, historial de búsquedas y diseño responsive.

## 🚀 Cómo Levantar el Proyecto

### Opción 1: Abrir directamente en el navegador
La forma más sencilla es abrir el archivo `index.html` directamente en tu navegador:
```
1. Navega a la carpeta del proyecto
2. Haz doble clic en index.html
3. El proyecto se abrirá en tu navegador predeterminado
```

### Opción 2: Usar Python (Recomendado)
Si tienes Python instalado, puedes usar el servidor HTTP integrado:

```bash
# Python 3.x
python -m http.server 8000

# O si tienes Python 2.x
python -m SimpleHTTPServer 8000
```

Luego abre tu navegador en: `http://localhost:8000`

### Opción 3: Usar Node.js
Si tienes Node.js instalado, puedes usar `http-server`:

```bash
# Instalar http-server globalmente (solo la primera vez)
npm install -g http-server

# Ejecutar el servidor
http-server -p 8000
```

Luego abre tu navegador en: `http://localhost:8000`

### Opción 4: Usar Visual Studio Code (Live Server)
Si usas VS Code, la forma más fácil es:

1. Instala la extensión "Live Server" en VS Code
2. Haz clic derecho en `index.html`
3. Selecciona "Open with Live Server"
4. El proyecto se abrirá automáticamente en tu navegador

### Opción 5: Usar otros servidores estáticos
- **PHP**: `php -S localhost:8000`
- **Ruby**: `ruby -run -e httpd . -p 8000`

---

## 📋 Descripción del Proyecto

Este proyecto es una aplicación web que consume la PokéAPI para mostrar información detallada de Pokémon. Permite a los usuarios buscar Pokémon por nombre o ID, visualizar sus características, y mantener un historial de búsquedas recientes.

## ✨ Características

- 🔍 **Búsqueda de Pokémon**: Busca por nombre o ID
- 🌓 **Modo Claro/Oscuro**: Toggle entre temas con un solo clic
- 📜 **Historial de Búsquedas**: Mantiene un registro de las últimas 5 búsquedas
- 🎨 **Diseño Moderno**: Interfaz atractiva con animaciones y efectos visuales
- 📱 **Responsive**: Se adapta a diferentes tamaños de pantalla
- ⚡ **Información Detallada**: Muestra altura, peso, tipo, habilidades, experiencia base y movimientos
- 🎯 **Manejo de Errores**: Mensajes de error personalizados y amigables
- 🎭 **Animaciones Suaves**: Transiciones y efectos visuales fluidos

## 🛠️ Tecnologías Utilizadas

- **HTML5**: Estructura de la aplicación
- **CSS3**: Estilos y animaciones (modo claro/oscuro, gradientes, transiciones)
- **JavaScript (Vanilla)**: Lógica de la aplicación y consumo de API
- **PokéAPI**: API REST para obtener datos de Pokémon
- **Google Fonts**: Tipografías (Press Start 2P, Poppins)

## 📁 Estructura del Proyecto

```
taller-rest-api/
│
├── index.html      # Estructura HTML principal
├── style.css       # Estilos y temas (claro/oscuro)
├── script.js       # Lógica de la aplicación y consumo de API
└── README.md       # Documentación del proyecto
```

## 🎮 Uso

1. **Buscar un Pokémon**:
   - Ingresa el nombre o ID del Pokémon en el campo de búsqueda
   - Haz clic en "Buscar" o presiona Enter
   - La información del Pokémon se mostrará en la tarjeta

2. **Cambiar de Tema**:
   - Haz clic en el botón de sol/luna (☀️/🌙) en la esquina superior derecha
   - Alterna entre modo claro y oscuro

3. **Usar el Historial**:
   - Las búsquedas recientes aparecen automáticamente en la sección de historial
   - Haz clic en cualquier Pokémon del historial para buscarlo nuevamente
   - El historial muestra hasta 5 Pokémon recientes

4. **Información Mostrada**:
   - Nombre del Pokémon
   - Imagen del sprite
   - Altura
   - Peso
   - Tipo(s)
   - Habilidades
   - Experiencia base
   - Movimientos (primeros 3)

## 🔧 Funcionalidades Técnicas

### Consumo de API
- Utiliza `fetch()` para realizar peticiones HTTP a la PokéAPI
- Manejo de errores con try-catch y mensajes personalizados
- Validación de entrada antes de realizar búsquedas

### Almacenamiento Local
- El historial de búsquedas se mantiene en memoria durante la sesión
- Se limita a 5 elementos para mantener la interfaz limpia

### Temas
- Sistema de temas usando clases CSS (`.dark` y `.light`)
- Variables CSS para colores y estilos consistentes
- Transiciones suaves entre temas

### Responsive Design
- Diseño adaptable usando Flexbox y Grid
- Scroll horizontal para el historial en pantallas pequeñas
- Media queries para diferentes tamaños de pantalla

## 🎨 Personalización

### Colores
Los colores pueden modificarse en las variables CSS al inicio de `style.css`:

```css
:root {
  --primary: #00ffff; /* Cian neón */
  --secondary: #007bff; /* Azul brillante */
  --cream: #f5f1e6; /* Fondo claro cálido */
  --dark-bg: #0a0f2c; /* Fondo azul oscuro */
  --dark-card: #132347; /* Tarjetas azul-gris */
  --text-light: #1a1a1a;
  --text-dark: #eaeaea;
}
```

## 📝 Notas

- La aplicación requiere conexión a internet para acceder a la PokéAPI
- Los datos se obtienen en tiempo real desde la API
- El historial se reinicia al recargar la página (almacenamiento en memoria)
- La API de Pokémon tiene límites de rate, pero son generosos para uso personal

## 🐛 Manejo de Errores

La aplicación maneja los siguientes casos de error:
- **Campo vacío**: Muestra mensaje pidiendo ingresar un nombre o ID
- **Pokémon no encontrado**: Muestra mensaje indicando que el Pokémon no existe
- **Errores de red**: Muestra mensaje de error con sugerencias

## 👩‍💻 Autor

**Catalina Angarita**

## 📄 Licencia

Este proyecto es de código abierto y está disponible para fines educativos.

## 🔗 Enlaces Útiles

- [PokéAPI Documentación](https://pokeapi.co/docs/v2)
- [PokéAPI](https://pokeapi.co/)

---

**¡Disfruta explorando el mundo de los Pokémon! ⚡**

