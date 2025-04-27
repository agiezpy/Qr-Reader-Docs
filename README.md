## Política de Privacidad para "Lector de Códigos QR Web"

Fecha de Entrada en Vigor: 28/04/2025

Bienvenido/a a Lector de Códigos QR Web (en adelante, "la Extensión"). Esta política de privacidad explica cómo manejamos la información cuando utilizas nuestra extensión para Google Chrome. Tu privacidad es importante para nosotros.

1. Información que la Extensión Maneja:

La Extensión está diseñada para funcionar principalmente de forma local en tu navegador.

Acceso al Contenido de la Página: Para encontrar códigos QR, la Extensión necesita analizar la estructura (DOM) de las páginas web que visitas. Busca específicamente elementos de imagen (<img>) y canvas (<canvas>). Este análisis se realiza localmente en tu navegador.
Procesamiento de Imágenes:
Canvas: Los datos de píxeles de los elementos <canvas> encontrados en la página se procesan localmente dentro del script de contenido para intentar decodificar un código QR.
Imágenes (<img>): Para poder escanear imágenes que provienen de dominios diferentes a la página actual (evitando restricciones de seguridad del navegador - CORS), la URL (dirección web) de dichas imágenes se envía al script de fondo (Service Worker) de la extensión. El script de fondo descarga la imagen temporalmente para analizarla en busca de códigos QR. Ni la URL ni el contenido de la imagen se almacenan permanentemente ni se envían a servidores externos.
Almacenamiento Local (chrome.storage.local):
La Extensión guarda un historial de los códigos QR que ha decodificado exitosamente (incluyendo el contenido del QR, un identificador de la fuente y la fecha/hora).
También guarda tus preferencias de configuración (si el escaneo automático está activado/desactivado, si el modo Clic-Scan está activado/desactivado).
Toda esta información se guarda localmente en el almacenamiento de tu navegador asociado a la Extensión y no se transmite a ningún servidor externo. Puedes borrar el historial en cualquier momento desde el popup de la Extensión.
Permiso del Portapapeles (clipboardWrite): Este permiso se utiliza únicamente cuando tú haces clic explícitamente en el botón "Copiar" junto a un resultado de QR en el popup, para copiar ese texto específico a tu portapapeles. La extensión no lee ni escribe en tu portapapeles en ningún otro momento.
Permiso de Pestañas (tabs): Este permiso se utiliza para permitir la comunicación entre el popup de la extensión y el script de contenido que se ejecuta en la pestaña activa (por ejemplo, para activar los modos de escaneo o para solicitar un re-escaneo con el botón "Escanear Página"). No se utiliza para leer tu historial de navegación ni el contenido de pestañas inactivas.
2. Recopilación de Datos Personales:

No recopilamos, almacenamos ni transmitimos ninguna Información de Identificación Personal (PII) tuya ni datos de navegación que no estén directamente relacionados con la funcionalidad descrita anteriormente. La extensión funciona localmente en tu navegador.

3. Uso de la Información:

La información manejada por la Extensión se utiliza exclusivamente para:

Encontrar y decodificar códigos QR en las páginas web que visitas.
Mostrarte el historial de QRs encontrados en el popup.
Permitirte copiar el contenido de los QRs.
Guardar y aplicar tus preferencias de configuración.
Facilitar la comunicación interna entre las partes de la extensión.
4. Intercambio de Información:

No compartimos ninguna información manejada por la extensión con terceros. Todo el procesamiento relevante ocurre localmente o dentro de los componentes de la propia extensión en tu navegador.

5. Seguridad:

Utilizamos las APIs de almacenamiento local de Chrome (chrome.storage.local), que almacenan los datos de forma segura dentro de tu perfil de navegador. Sin embargo, como con cualquier software, no podemos garantizar una seguridad absoluta.

6. Cambios a esta Política de Privacidad:

Podemos actualizar esta Política de Privacidad ocasionalmente. Te notificaremos sobre cualquier cambio publicando la nueva Política de Privacidad en la ficha de la Chrome Web Store o a través de otros medios apropiados. Te recomendamos revisar esta Política periódicamente.   

7. Contacto:

Si tienes alguna pregunta sobre esta Política de Privacidad, por favor, contáctanos en: anibalgiezpy@gmail.com
