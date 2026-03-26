# 👓 Meta AI HDR Fix (ColorOS/Oppo)

### 🇪🇸 Español - ¿Qué soluciona esto?
Este APK parcheado soluciona el problema de **importación de video corrupto** (tonalidades magenta y verdes) que sufren los usuarios de **Ray-Ban Meta V2 y Oakley Meta** con dispositivos **Oppo, OnePlus y Realme (ColorOS/OxygenOS)**. 

El fallo original ocurre porque el sistema operativo de estos móviles (Motor Atlas) intercepta la decodificación HDR de las gafas Meta e intenta aplicar una conversión de color redundante, estropeando el resultado final al guardarlo en la galería.

#### Parches aplicados:
*   **Identidad Forzada**: La App se identifica como un **Google Pixel** para saltar las restricciones de Oppo.
*   **Anulación de Shader**: Se ha simplificado el código de color (`hlg_fs.glsl`) de Meta para evitar la doble conversión.
*   **Paso de Datos Puro**: Desactivación del post-procesado de hardware en `assets/video_config_android.json`.

---

### 🇬🇧 English - What does this solve?
This patched APK fixes the **corrupted video import** issue (magenta and green tints) experienced by **Ray-Ban Meta V2 and Oakley Meta** users on **Oppo, OnePlus, and Realme (ColorOS/OxygenOS)** devices.

The original bug occurs because the device's OS (Atlas Engine) intercepts the Meta glasses' HDR decoding and attempts a redundant color conversion, breaking the final file saved to the gallery.

#### Applied Patches:
*   **Forced Identity**: The App identifies as a **Google Pixel** to bypass Oppo-specific 19:50 26/03/2026hardware paths.
*   **Shader Bypass**: Simplified Meta's color code (`hlg_fs.glsl`) to prevent double-tone-mapping.
*   **Pure Data Flow**: Disabled hardware post-processing in `assets/video_config_android.json`.

---

⚠️ **IMPORTANTE / IMPORTANT (LIMITACIONES/LIMITATIONS)**:

**ES**: Al ser un APK con una firma externa personalizada (re-firmado para poder aplicar los parches), **se pierden las funciones de sincronización con WhatsApp, Instagram y Messenger**. Esto es una medida de seguridad de Meta que bloquea la comunicación entre apps si la firma no es la oficial. **Usa este parche solo si tu prioridad es que los videos se vean perfectos.**

**EN**: Since this is a custom-signed APK (re-signed to apply patches), **WhatsApp, Instagram, and Messenger synchronization features will not work**. This is a security measure by Meta that blocks inter-app communication if the signature is not official. **Use this patch only if your priority is perfect video quality.**
