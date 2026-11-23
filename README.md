# Radio Encoder (Android)

Transmite a un servidor Icecast o SHOUTcast v1 en AAC-LC mono 44.1 kHz.

## Fuentes de audio
- **Micrófono**.
- **Automático**: reproduce las canciones de la carpeta que tengas asignada a cada hora
  (hora del teléfono), en orden aleatorio sin repetir, e inserta un ID de la radio
  cada N canciones. Si una hora no tiene carpeta, usa la carpeta por defecto.
  El cambio de carpeta ocurre al terminar la canción en curso.
  Configúralo en "Programación por hora e IDs". Formatos: mp3, aac, m4a, ogg, opus, wav, flac.
- El título de la canción se actualiza en el servidor (en un ID se muestra el nombre de la emisora).

## Cómo compilar

### Opción A: Android Studio (en tu computadora)
1. **Descomprime** el zip (clic derecho > Extraer todo). No funciona desde dentro del zip.
2. Instala Android Studio (developer.android.com/studio).
3. File > Open y elige la carpeta RadioEncoder. Espera a que termine "Gradle sync"
   (la primera vez descarga cosas; acepta instalar el SDK si lo pide).
4. Para el APK: Build > Build Bundle(s) / APK(s) > Build APK(s). Al terminar pulsa "locate":
   el archivo está en app/build/outputs/apk/debug/app-debug.apk.
5. Pásalo al teléfono y ábrelo (permite "instalar apps desconocidas"). O conecta el teléfono
   por USB con la depuración USB activada y pulsa el botón Run.

### Opción B: sin instalar nada (GitHub)
1. Crea una cuenta gratis en github.com y un repositorio nuevo.
2. Sube el CONTENIDO de la carpeta RadioEncoder (arrastra todo, incluida la carpeta .github)
   con "Add file > Upload files".
3. Entra en la pestaña "Actions": se ejecuta solo "Compilar APK" (tarda unos minutos).
4. Abre la ejecución terminada y descarga "RadioEncoder-apk" (viene en un zip con app-debug.apk).

## Pendiente
- Audio interno del teléfono, MP3 (LAME), SHOUTcast v2.
