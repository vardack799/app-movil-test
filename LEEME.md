# Análisis de movimiento · APK

App Android (Capacitor) que analiza tu técnica de movimiento con IA (MediaPipe BlazePose).
Funciona sin internet y el video nunca sale del teléfono.

## Opción A · Compilar en la nube (sin instalar nada)
1. Crea una cuenta en https://github.com y un repositorio nuevo (privado está bien).
2. Sube TODO el contenido de esta carpeta (incluida la carpeta oculta `.github`).
3. Ve a la pestaña **Actions** → **Compilar APK** → espera ~5–8 min a que termine.
4. Abre la ejecución terminada y descarga el artefacto **analisis-movimiento-apk** (zip con `app-debug.apk`).
5. Pasa el APK al celular, ábrelo y acepta **instalar apps de origen desconocido**.
6. Al elegir «Grabar o subir video», acepta el permiso de cámara.

## Opción B · Android Studio
1. Instala Node 18+ y Android Studio.
2. `npm install` y luego `npx cap sync android`.
3. `npx cap open android` → **Build > Build APK(s)**.

## Notas
- Es un APK de depuración (firmado con la clave debug): sirve para probar e instalar, no para Google Play.
- El botón «Interpretar con IA» solo existe en la versión web; en el APK se oculta porque requiere conexión a Claude.
- Para cambiar algo, edita `www/index.html` y repite `npx cap sync android`.
