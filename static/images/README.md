# Imágenes requeridas para CIUMMP 2026

## Estructura de carpetas

```
static/
├── images/
│   ├── logo.webp                      # Logo principal del evento
│   ├── logo_ciummp.webp               # Logo específico CIUMMP (fallback al logo general)
│   ├── logo_blue.webp                 # Logo alternativo (usado en navbar y footer)
│   ├── cartel.png                     # Cartel/poster del evento
│   ├── cartel_ciummp_2026.png         # Cartel específico (fallback al cartel general)
│   ├── fondo*.webp/png/jpg            # Imágenes de fondo aleatorias
│   ├── credential_bg.webp/png         # Fondo para credenciales PDF
│   ├── ciummp_programa_d1.png         # Programa descargable día 1
│   ├── ciummp_programa_d2.png         # Programa descargable día 2
│   └── carrusel/                      # Imágenes para el carrusel
│       ├── *.jpg
│       ├── *.png
│       └── *.webp
└── qrcodes/                           # Códigos QR generados automáticamente
```

## Lista de imágenes necesarias

### Obligatorias

1. **logo.webp** - Logo principal del CIUMMP 2026
   - Formato: WebP recomendado
   - Tamaño sugerido: 400x200px

2. **logo_ciummp.webp** (o usar logo.webp como fallback)
   - Logo específico del evento
   - Se muestra en la página principal

3. **cartel_ciummp_2026.png** o **cartel.png**
   - Cartel del evento para el modal inicial
   - Formato: PNG con transparencia o JPG
   - Tamaño sugerido: 800x1200px (vertical)

4. **fondo*.webp** (múltiples archivos)
   - Imágenes de fondo aleatorias
   - Nombres sugeridos: fondo1.webp, fondo2.webp, etc.
   - Resolución: mínimo 1920x1080px

5. **credential_bg.webp** o **credential_bg.png**
   - Fondo para las credenciales/certificados PDF
   - Tamaño: 600x900 puntos (aprox)

### Opcionales pero recomendadas

6. **ciummp_programa_d1.png**
   - Imagen descargable del programa día 1
   - Tamaño: A4 o similar

7. **ciummp_programa_d2.png**
   - Imagen descargable del programa día 2
   - Tamaño: A4 o similar

8. **carrusel/*.jpg/png/webp**
   - Múltiples imágenes para el carrusel de la página principal
   - Se cargan dinámicamente desde la carpeta carrusel/

## Colores del evento

Para diseñar las imágenes, usar la paleta de colores:

- **Azul marino:** #1e3a5f (color principal)
- **Azul hospitalario:** #2c5282 (color secundario)
- **Turquesa:** #319795 (acento)
- **Arena:** #d4c4a8 (detalles)
- **Blanco:** #ffffff (fondos)

## Notas

- Las imágenes se cargan con fallback: si no existe la específica, usa la general
- El logo en la navbar usa `logo.webp` con texto "CIUMMP 2026"
- El carrusel carga automáticamente todas las imágenes de la carpeta carrusel/
- Los QR se generan automáticamente en static/qrcodes/

## TODO

- [ ] Crear diseño del logo CIUMMP 2026
- [ ] Diseñar cartel del evento (23-24 Oct 2026, Hospital Marina Mazatlán)
- [ ] Crear imágenes de fondo con paleta de colores CIUMMP
- [ ] Diseñar fondo para credenciales PDF
- [ ] Crear imágenes descargables del programa (día 1 y día 2)
- [ ] Preparar imágenes para el carrusel (fotos de instalaciones, eventos anteriores, etc.)
