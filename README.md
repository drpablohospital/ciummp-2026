# CIUMMP 2026 - Adaptación completada

## Resumen de cambios realizados

### Archivos modificados/creados:

1. **config.py**
   - Cambiado nombre de base de datos de `clinical_care.db` a `ciummp_2026.db`

2. **models.py**
   - Agregado campo `talleres` (String 200) en el modelo Registration para almacenar IDs de talleres seleccionados

3. **app.py**
   - Cambiado email de contacto de `medicinacriticasjdr@gmail.com` a `investigacionhmm@gmail.com`
   - Actualizados precios: $1,200 general + $250 por taller
   - Modificada función `purchase()` para usar el nuevo sistema de boletos (general + talleres opcionales)
   - Modificada función `generate_certificate()` con fechas actualizadas (23 y 24 de octubre 2026, Hospital Marina Mazatlán)
   - Actualizado producto de Stripe a "CIUMMP 2026"
   - Modificada función `verify()` para incluir campo talleres
   - Actualizado email de destino en contact() a investigacionhmm@gmail.com

4. **templates/base.html** (completamente reescrito)
   - Meta tags actualizados a CIUMMP 2026
   - Nueva paleta de colores: azul marino (#1e3a5f), azul hospitalario (#2c5282), turquesa (#319795), arena (#d4c4a8)
   - Navbar actualizado con "CIUMMP 2026"
   - Footer actualizado con Hospital Marina Mazatlán y contactos nuevos

5. **templates/index.html** (completamente reescrito)
   - Título: CIUMMP 2026
   - Subtítulo: Congreso Integral de Urgencias Médicas y Medicina Prehospitalaria
   - Fechas: 23 y 24 de octubre de 2026
   - Sede: Hospital Marina Mazatlán
   - Modal con cartel del evento

6. **templates/info.html** (completamente reescrito)
   - Información del CIUMMP 2026
   - Modalidad presencial con cupo limitado
   - Costos: $1,200 general, $250 taller
   - Contacto: investigacionhmm@gmail.com, +52 669 278 2010, +52 720 294 5855

7. **templates/program.html** (completamente reescrito)
   - Programa CIUMMP 2026 con pestañas Día 1 y Día 2
   - Día 1 (Viernes 23 Oct): Talleres ultrasonido/accesos + Conferencias (protección pulmonar, oxigenoterapia, evento vascular cerebral, fluidoterapia, paciente crítico aéreo, SDRA, cáncer de mama)
   - Día 2 (Sábado 24 Oct): Talleres intubación/RCP + Conferencias (código sepsis, preeclampsia, fracturas expuestas, TCE, politraumatizado, sedación, nutrición)

8. **templates/purchase.html** (completamente reescrito)
   - Formulario simplificado: boleto general ($1,200) + selección de talleres ($250 c/u)
   - Talleres: Ultrasonido en paciente crítico, Accesos ecoguiados, Intubación orotraqueal, RCP
   - Sin modalidad virtual
   - Sin curso de fisioterapia

9. **templates/success.html** (actualizado)
   - Textos actualizados a CIUMMP 2026

10. **templates/cancel.html** (actualizado)
    - Textos actualizados a CIUMMP 2026

11. **templates/verify.html** (completamente reescrito)
    - Diseño actualizado con colores CIUMMP
    - Muestra información de talleres si existen

12. **static/images/README.md** (creado)
    - Documentación de imágenes necesarias
    - Lista de TODOs para diseño

## TODOs pendientes (imágenes)

- [ ] Crear diseño del logo CIUMMP 2026
- [ ] Diseñar cartel del evento (23-24 Oct 2026, Hospital Marina Mazatlán)
- [ ] Crear imágenes de fondo con paleta de colores CIUMMP
- [ ] Diseñar fondo para credenciales PDF
- [ ] Crear imágenes descargables del programa (día 1 y día 2)
- [ ] Preparar imágenes para el carrusel

## Comando para ejecutar

```bash
cd "/home/xiu/Escritorio/Arcaive/Tablero/Prog/Main Proyects/Web-Master/ciummp_2026"
python3 app.py
```

O para producción con gunicorn:

```bash
cd "/home/xiu/Escritorio/Arcaive/Tablero/Prog/Main Proyects/Web-Master/ciummp_2026"
gunicorn -w 4 -b 0.0.0.0:5000 app:app
```

## Notas importantes

1. Se requieren variables de entorno:
   - `SECRET_KEY` (opcional, usa 'dev-secret-key' por defecto)
   - `STRIPE_PUBLIC_KEY`
   - `STRIPE_SECRET_KEY`
   - `STRIPE_WEBHOOK_SECRET`
   - `MAIL_PASSWORD`
   - `BASE_URL` (opcional, para códigos QR)

2. La base de datos SQLite se creará automáticamente al iniciar la app

3. Las imágenes del proyecto original se copiaron como fallback, pero deben reemplazarse por diseños específicos del CIUMMP 2026
