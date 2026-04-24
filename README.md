# 🚀 Landing Page Template - Plantilla Reutilizable para Negocios

Una plantilla de landing page moderna, responsive y lista para producción, diseñada para ser fácilmente personalizable para cualquier tipo de negocio (kioscos, heladerías, barberías, restaurantes, etc.).

## ✨ Características Principales

- 🎨 **Diseño Moderno**: Interfaz limpia y profesional con animaciones suaves
- 📱 **Mobile-First**: Optimizado para dispositivos móviles y tablets
- ⚡ **Alto Rendimiento**: Lazy loading, código optimizado y sin dependencias externas
- 🔧 **Fácil Configuración**: Todo el contenido se edita desde un archivo `data.json`
- 💬 **WhatsApp Integrado**: Botón flotante y en hero con contacto directo
- 🖼️ **Galería Dinámica**: Carrusel de imágenes con navegación táctil
- 🗺️ **Mapa Integrado**: Google Maps embebido configurable
- 🎯 **SEO Optimizado**: Meta tags dinámicos y estructura semántica
- ♿ **Accesible**: Navegación por teclado y buenas prácticas WCAG

## 📁 Estructura del Proyecto

```
landing-page-template/
├── index.html          # Página principal
├── styles.css          # Estilos CSS completos
├── script.js           # Funcionalidad JavaScript
├── data.json           # Configuración del negocio
├── assets/             # Directorio de assets opcionales
│   └── README.md       # Instrucciones para assets
└── README.md           # Este archivo
```

## 🚀 Instalación y Uso Rápido

### 1. Clonar o Descargar el Proyecto

```bash
# Si usas Git
git clone <URL-del-repositorio>
cd landing-page-template

# O descarga y descomprime el ZIP
```

### 2. Personalizar la Información

Edita el archivo `data.json` con la información de tu negocio:

```json
{
  "businessName": "Nombre de tu Negocio",
  "description": "Descripción corta y atractiva",
  "whatsapp": "5491123456789",
  "heroImage": "https://URL-de-tu-imagen.jpg",
  "gallery": [
    "https://URL-imagen-1.jpg",
    "https://URL-imagen-2.jpg"
  ],
  "address": "Dirección completa",
  "hours": "Lunes a Viernes: 9:00 - 18:00",
  "mapEmbed": "<iframe>...</iframe>"
}
```

### 3. Subir a GitHub Pages

1. **Crea un repositorio en GitHub**
2. **Sube los archivos**:
   ```bash
   git init
   git add .
   git commit -m "Initial commit"
   git branch -M main
   git remote add origin https://github.com/tu-usuario/nombre-repo.git
   git push -u origin main
   ```
3. **Activa GitHub Pages**:
   - Ve a Settings → Pages
   - Selecciona "Deploy from a branch"
   - Elige `main` y `/ (root)`
   - Guarda y espera unos minutos

¡Tu sitio estará disponible en `https://tu-usuario.github.io/nombre-repo`!

## 📝 Guía de Personalización Detallada

### 🏢 Configuración del Negocio (`data.json`)

#### Información Básica
- `businessName`: Nombre del negocio (aparece en título, hero y footer)
- `description`: Descripción corta para SEO y hero section
- `whatsapp`: Número de WhatsApp (formato: código país + número sin espacios)

#### Imágenes
- `heroImage`: URL de imagen de fondo del hero (recomendado: 1920x1080px)
- `gallery`: Array de URLs para el carrusel (recomendado: 800x600px)

**Tip**: Puedes usar imágenes locales:
```json
"heroImage": "assets/mi-imagen.jpg"
```

#### Ubicación y Contacto
- `address`: Dirección completa del negocio
- `hours`: Horarios de atención (usa `\n` para saltos de línea)
- `mapEmbed`: Iframe de Google Maps

**Cómo obtener el iframe de Google Maps**:
1. Ve a [Google Maps](https://maps.google.com)
2. Busca tu dirección
3. Haz clic en "Compartir" → "Insertar un mapa"
4. Copia el código `<iframe>` completo

### 🎨 Personalización Visual (`styles.css`)

#### Colores Principales
Modifica las variables CSS al inicio del archivo:

```css
:root {
    --primary-color: #2563eb;      /* Color principal */
    --secondary-color: #10b981;    /* Color de botones */
    --text-dark: #1f2937;          /* Texto oscuro */
    /* ... otras variables */
}
```

#### Tipografías
Cambia la fuente base modificando:
```css
:root {
    --font-family: 'Tu-Fuente', sans-serif;
}
```

#### Espaciado y Tamaños
Ajusta las variables de espaciado según tus preferencias:
```css
:root {
    --spacing-sm: 1rem;    /* Espaciado pequeño */
    --spacing-md: 2rem;    /* Espaciado medio */
    /* ... */
}
```

### 📱 Optimización para Móviles

El diseño es mobile-first por defecto. Para ajustes específicos:

```css
/* Tablets */
@media (max-width: 768px) {
    /* Tus ajustes aquí */
}

/* Móviles */
@media (max-width: 480px) {
    /* Tus ajustes aquí */
}
```

## 🔄 Duplicar para Nuevos Clientes

### Método 1: Usando Git (Recomendado)

```bash
# 1. Clona el template original
git clone <URL-template> nuevo-cliente
cd nuevo-cliente

# 2. Cambia el remote al nuevo repositorio
git remote remove origin
git remote add origin https://github.com/tu-usuario/nuevo-cliente.git

# 3. Edita data.json con la información del nuevo cliente
# 4. Sube al nuevo repositorio
git add .
git commit -m "Configurado para [Nombre Cliente]"
git push -u origin main
```

### Método 2: Manual

1. **Copia la carpeta completa** del template
2. **Renombra la carpeta** con el nombre del cliente
3. **Edita `data.json`** con la información del cliente
4. **Crea un nuevo repositorio** en GitHub
5. **Sube los archivos** al nuevo repositorio

## 🌐 Imágenes y Assets

### Imágenes Externas (Dropbox, Google Drive, etc.)

Para usar URLs externas:
1. Sube las imágenes a Dropbox/Google Drive
2. Obtén el enlace público
3. Asegúrate de que termine en formato de imagen directa

**Ejemplo Dropbox**:
```
❌ https://www.dropbox.com/s/abc123/imagen.jpg?dl=0
✅ https://dl.dropboxusercontent.com/s/abc123/imagen.jpg
```

### Imágenes Locales

1. Coloca las imágenes en la carpeta `assets/`
2. Referencia con ruta relativa en `data.json`:
```json
"gallery": [
    "assets/foto1.jpg",
    "assets/foto2.jpg"
]
```

## 🛠️ Funcionalidades Avanzadas

### Carrusel de Imágenes
- **Navegación**: Botones laterales, indicadores y teclas de flecha
- **Autoplay**: Cambia cada 5 segundos (se pausa al hover)
- **Responsive**: Se adapta al tamaño de pantalla
- **Lazy Loading**: Las imágenes cargan según se necesitan

### Animaciones al Scroll
Las secciones aparecen con efecto fade-in al hacer scroll. Para desactivar:
```css
.fade-in-section {
    opacity: 1 !important;
    transform: none !important;
}
```

### WhatsApp Integration
El botón flotante crea un mensaje predeterminado:
```
"Hola! Estoy interesado/a en tus servicios. Vi tu página web y me gustaría obtener más información."
```

## 🐛 Solución de Problemas

### Imágenes No Cargan
1. **Verifica URLs**: Asegúrate de que sean enlaces directos a imágenes
2. **CORS**: Las imágenes deben permitir acceso desde tu dominio
3. **Formatos**: Usa formatos web (JPEG, PNG, WebP)

### Mapa No Aparece
1. **Verifica el iframe**: Copia el código completo de Google Maps
2. **Privacidad**: Algunas ubicaciones requieren configuración especial

### WhatsApp No Funciona
1. **Formato del número**: Usa formato internacional sin espacios
2. **Código país**: Incluye el código (ej: 54 para Argentina)

## 📈 Performance y SEO

### Optimización Automática
- ✅ Lazy loading de imágenes
- ✅ CSS y JavaScript minificados (opcional)
- ✅ Meta tags dinámicos
- ✅ Estructura semántica HTML5

### Mejoras Manuales
```bash
# Minificar CSS (opcional)
npx clean-css-cli -o styles.min.css styles.css

# Minificar JavaScript (opcional)
npx terser script.js -o script.min.js
```

## 🔧 Mantenimiento

### Actualizar Contenido
Simplemente edita `data.json` y los cambios se reflejarán inmediatamente.

### Agregar Nuevas Funcionalidades
El código está modularizado y comentado para facilitar extensiones:
- Nuevas secciones en `index.html`
- Estilos adicionales en `styles.css`
- Funcionalidades en `script.js`

## 📄 Licencia

Este template es libre para uso comercial y personal. Puedes:
- ✅ Usarlo para clientes
- ✅ Modificarlo según necesites
- ✅ Incluirlo en tus servicios

## 🤝 Soporte

Si encuentras algún problema o necesitas ayuda:
1. Revisa la sección de solución de problemas
2. Verifica la consola del navegador para errores
3. Asegúrate de que `data.json` tenga formato JSON válido

---

**¡Listo para empezar a crear sitios web profesionales para tus clientes!** 🎉
