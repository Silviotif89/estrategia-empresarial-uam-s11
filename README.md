# Estrategia Empresarial UAM · Sesión 11

Presentación académica de 44 diapositivas y laboratorio de decisiones de Café Horizonte, en una sola experiencia para proyector y teléfonos.

## Archivos

- `index.html`: presentación, navegación, temporizadores y acceso a la actividad.
- `activity.html` y `activity-app.js`: registro de equipos, cinco rondas, panel docente, QR, notificaciones y ruleta.
- `firestore.rules`: reglas que separan los datos de cada equipo y limitan el control a la persona propietaria de la sesión.
- `firebase.json`: ruta de las reglas para Firebase CLI.

## Firebase

El proyecto `estrategia-empresarial-uam-s11` ya está creado bajo la cuenta del docente, con una app web, Authentication (Anónimo y Correo/contraseña) y Cloud Firestore en `northamerica-south1` (México), plan Spark. Las reglas de seguridad ya están publicadas. La configuración web pública ya está precargada en el panel; no incluye contraseñas ni claves administrativas.

Falta crear en Authentication → Usuarios la cuenta docente con el correo de acceso elegido. No habilites registro público. La contraseña se introduce solo al iniciar sesión desde el panel y no se guarda ni se envía en el QR.

## Publicación

La URL de GitHub Pages es:

`https://silviotif89.github.io/estrategia-empresarial-uam-s11/`

El flujo de GitHub Actions publicará la página al habilitarse. Para que la autenticación funcione desde esa dirección, agrega `silviotif89.github.io` a los dominios autorizados en Firebase Authentication. Después crea una sesión desde el panel y escanea el QR para probar el recorrido real.

El API key de Firebase para web es un identificador público; el acceso a Firestore depende de sus reglas. Nunca incluyas una contraseña o clave de servicio en la página.