# Sistema PSCJ — proyecto para generar el APK

La página está en www/index.html (con las fuentes incluidas, funciona sin internet).

## Opción A: con Android Studio
Requisitos: Node.js 18+ y Android Studio (incluye el JDK).

    npm install
    npx cap add android
    npx cap sync android
    npx cap open android

En Android Studio: Build > Build Bundle(s) / APK(s) > Build APK(s).
El archivo queda en android/app/build/outputs/apk/debug/app-debug.apk

## Opción B: sin instalar nada (GitHub)
1. Cree un repositorio en github.com y suba el contenido de esta carpeta.
2. Pestaña Actions > "Construir APK" > Run workflow.
3. Cuando termine (5-10 min), descargue "sistema-pscj-apk" desde Artifacts y descomprima el .apk.

## Actualizar la página
Reemplace www/index.html y repita "npx cap sync android" y el Build (o vuelva a ejecutar el workflow).

## Instalar en el teléfono
Pase el .apk al teléfono y ábralo; debe permitir "instalar apps de orígenes desconocidos".
