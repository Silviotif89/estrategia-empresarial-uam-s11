# Estrategia Empresarial UAM · Sesión 11

Presentación académica de 44 diapositivas y laboratorio de decisiones de Café Horizonte, en una sola experiencia para proyector y teléfonos.

## Archivos

- `index.html`: presentación, navegación, temporizadores y acceso a la actividad.
- `activity.html` y `activity-app.js`: registro de equipos, cinco rondas, panel docente, QR, notificaciones y ruleta.
- `firestore.rules`: reglas para separar los datos de cada equipo y proteger las herramientas del docente.
- `firebase.json`: ruta de las reglas para Firebase CLI.

## Actividad local

Abrí `index.html` desde un servidor web local. La demostración local conserva los datos en ese navegador y avisa que no sincroniza entre dispositivos. El QR real requiere GitHub Pages y autenticación/reglas Firebase activadas.

## Firebase

El proyecto `estrategia-empresarial-uam-s11` ya está creado bajo la cuenta del docente, con una aplicación web y Cloud Firestore en `northamerica-south1` (México), dentro del plan Spark. La configuración pública de Firebase ya está prellenada en el panel docente; no incluye contraseñas ni claves administrativas.

1. En Authentication activa los proveedores **Anónimo** para equipos y **Correo/contraseña** para docente. Crea el usuario docente en la consola; no habilites registro público.
2. Publica `firestore.rules` en Cloud Firestore → Reglas (o usa Firebase CLI):

   ```sh
   firebase login
   firebase use --add
   firebase deploy --only firestore:rules
   ```

3. En el panel docente, abre **Firebase**, escribe el correo y contraseña del usuario docente y pulsa **Conectar y crear sesión**. La contraseña se usa solo para autenticación; no se guarda ni se incluye en el QR.
4. La sesión genera un QR con la URL publicada, su identificador y la configuración web pública. Los estudiantes usan autenticación anónima y solo escriben en su documento; el docente propietario puede consultar el grupo.

No pegues contraseñas administrativas ni claves de servicio en el sitio. El API key de Firebase para web es un identificador público; el acceso a Firestore depende de sus reglas de seguridad.

## Publicación

La URL de GitHub Pages para este repositorio será:

`https://silviotif89.github.io/estrategia-empresarial-uam-s11/`

La publicación se habilitará cuando se activen los proveedores de Authentication, se publiquen las reglas y se verifique el recorrido real entre estudiante y docente.