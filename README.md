# 🍋 Lemoncode · Layout LAB extra

Este repositorio contiene la resolución del laboratorio extra de layout, en el que se propone maquetar una aplicación responsive con cabecera, navegación, contenido principal y pie de página. Para esta entrega he mantenido la comunidad de Lemoncoders del HTML de ejemplo y he personalizado su diseño con tonos lima y verde oscuro, tarjetas redondeadas y sombras suaves.

La maquetación está realizada con **HTML, CSS, Sass y Vite**, utilizando **CSS Grid**, **Flexbox**, **media queries** y **position: sticky**. El trabajo se centra en la estructura del proyecto y los estilos, sin JavaScript de aplicación.

---

## 📁 Estructura del proyecto

```text
styles/
├── _variables.scss         # Colores, ancho del menú y breakpoints
├── _base.scss              # Reset, tipografía y foco de teclado
├── _layout.scss            # Estructura global y distribución de tarjetas
├── _components.scss        # Toolbar, título, navegación y tarjetas
├── _responsive.scss        # Adaptación a móvil y tablet
└── main.scss               # Entrada de estilos con módulos @use

index.html                  # Cabecera, navegación, miembros y pie
package.json                # Dependencias y scripts de Vite
package-lock.json           # Versiones resueltas de las dependencias
.gitignore                  # Exclusión de dependencias, caché y compilación
```

---

## 🧪 Componentes

### 1️⃣ Cabecera y toolbar

La cabecera incluye un campo de búsqueda, el texto **Usuario Lemoncode** y una barra con el título **Welcome Lemoncoders!**.

- En escritorio se muestran el buscador y el nombre de usuario.
- Hasta **768 px**, ambos se ocultan y se conserva la barra del título.
- El buscador es un elemento de maqueta: permite escribir, pero no filtra el contenido.
- El nombre de usuario es texto fijo; no hay autenticación.

📂 `index.html`  
📂 `styles/_components.scss`

---

### 2️⃣ Navegación responsive

El menú incluye las opciones **React**, **Svelte**, **Vue** y **Angular**.

- Por encima de **768 px**, ocupa una barra lateral de **190 px**, con el título Frameworks.
- Hasta **768 px**, aparece en una fila horizontal bajo la cabecera y se oculta el título del menú.
- La navegación permanece visible durante el scroll mediante **position: sticky**.
- Los enlaces incluyen estados de hover y foco para la navegación por teclado.
- Las opciones llevan al listado de miembros; no hay páginas independientes por framework.

📂 `styles/_layout.scss`  
📂 `styles/_components.scss`  
📂 `styles/_responsive.scss`

---

### 3️⃣ Listado de miembros

El contenido principal muestra **10 tarjetas** con retratos y nombres de la comunidad sobre un fondo gris claro, diferente del blanco de las tarjetas.

En escritorio, **Flexbox** distribuye las tarjetas en varias columnas y reparte el espacio de cada fila. En móvil y tablet, las tarjetas pasan a una columna, con la imagen y el nombre colocados en horizontal.

Los retratos incluyen texto alternativo y dimensiones explícitas. Las imágenes proceden de GitHub Avatars, como en el HTML original, y necesitan conexión a Internet.

📂 `index.html`  
📂 `styles/_components.scss`  
📂 `styles/_responsive.scss`

---

### 4️⃣ Estructura general y pie de página

El body utiliza **CSS Grid** con tres filas: cabecera, zona central y pie. La fila central crece para mantener el footer al final de la ventana cuando hay poco contenido.

En escritorio, la zona central utiliza otra rejilla para distribuir el menú lateral y el contenido. En móvil se organiza en vertical mediante **Flexbox**.

El footer muestra **Master Lemoncode** y permanece en el flujo del documento, después del contenido.

📂 `styles/_layout.scss`

---

### 5️⃣ Variables y estilos comunes

Los estilos se organizan en parciales de Sass cargados desde `main.scss` mediante **@use**. El archivo de variables centraliza los colores, el ancho de la barra lateral y los breakpoints de **768 px** y **360 px**.

Los componentes utilizan anidado de Sass. Se incluyen indicadores de foco y se desactivan las transiciones del menú cuando el usuario prefiere movimiento reducido.

📂 `styles/_variables.scss`  
📂 `styles/_base.scss`  
📂 `styles/main.scss`

---

## 🚀 Instalación y ejecución

Es necesario tener instalados **Node.js 22.12 o superior** y **npm**.

#### 1. Abre una terminal en la raíz del proyecto.

#### 2. Instala las dependencias:

```bash
npm install
```

#### 3. Levanta el entorno de desarrollo:

```bash
npm run dev
```

#### 4. Abre la URL que aparece en consola.

Normalmente será `http://localhost:5173`. Si el puerto está ocupado, Vite indicará otro.

El HTML fuente debe abrirse mediante Vite: abrirlo directamente con `file://` no compila Sass ni resuelve la ruta de estilos.

Para generar y revisar la versión de producción:

```bash
npm run build
npm run preview
```

La compilación genera los archivos en `dist/`.

---

## 🛠️ Tecnologías usadas

- HTML5
- CSS3
- SCSS (Sass)
- Vite
- CSS Grid
- Flexbox
- Media queries
- Position sticky
- Responsive Design
