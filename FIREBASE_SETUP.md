# Firebase para ENCAPS: preparación (NO activado todavía)

El sitio sigue servido por **GitHub Pages**. Firebase se utilizará solo para inicio de sesión y sincronización del progreso, **sin reemplazar el almacenamiento local ni borrar historial**.

## Pasos en Firebase Console
1. Entrar a https://console.firebase.google.com/ e iniciar sesión.
2. Crear un proyecto específico (por ejemplo, **encaps-estudio**) o elegir uno existente.
3. En Authentication > Sign-in method, habilitar **Correo/contraseña** (o Google, según preferencia).
4. En Firestore Database, crear base de datos y colocar las reglas del archivo `firestore.rules`. **No dejar reglas de prueba abiertas**.
5. En Project settings > Your apps, registrar una aplicación **Web** y copiar el objeto de configuración pública de Firebase (`apiKey`, `authDomain`, `projectId`, `appId`, etc.). No compartir contraseñas, claves de cuentas de servicio ni tokens privados.
6. En Authentication > Settings > Authorized domains, autorizar `juanmavar2828-pixel.github.io` si no aparece.

## Integración pendiente en la web
- Añadir Firebase Web SDK (Auth y Firestore) a la app.
- Crear pantalla de acceso y selector de cuenta.
- Guardar por UID: sesión/simulacro, respuestas, errores, favoritos, progreso de tarjetas FSRS y ajustes.
- Mantener la escritura local como respaldo; sincronizar al iniciar sesión y en cada cambio relevante.
- Resolver conflictos entre PC y celular (por registro y fecha, preservando el progreso más completo). Nunca sobreescribir el progreso local automáticamente con una nube vacía.
- Probar inicio de sesión, desconexión temporal, reingreso y sincronización PC ↔ Android.
- Ofrecer exportación y respaldo antes de la primera migración. Confirmar el éxito antes de limpiar cualquier dato local.

**Estado:** solo infraestructura/documentación preparada. Ninguna sincronización funcionará hasta configurar un proyecto Firebase e integrar el SDK en la aplicación real.
