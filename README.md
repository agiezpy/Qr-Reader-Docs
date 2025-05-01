# Política de Privacidad para "Lector de Códigos QR Web"

**Fecha de Entrada en Vigor:** 28/04/2025

Bienvenido/a a **Lector de Códigos QR Web** (en adelante, *la extensión*). Esta política de privacidad explica cómo manejamos la información cuando utilizas nuestra extensión para Google Chrome. Tu privacidad es importante para nosotros.

---

## 1. Información que la Extensión Maneja

La extensión está diseñada para funcionar principalmente de forma local en tu navegador.

### Acceso al Contenido de la Página
Para encontrar códigos QR, la extensión necesita analizar la estructura (DOM) de las páginas web que visitas. Busca específicamente elementos de imagen (`<img>`) y canvas (`<canvas>`). Este análisis se realiza localmente en tu navegador.

### Procesamiento de Imágenes
- **Canvas:** Los datos de píxeles de los elementos `<canvas>` encontrados en la página se procesan localmente dentro del script de contenido para intentar decodificar un código QR.
- **Imágenes (`<img>`):** Para escanear imágenes de dominios distintos al de la página actual (evitando restricciones CORS), la URL de dichas imágenes se envía al *script de fondo* (Service Worker). Este descarga la imagen temporalmente para analizarla.  
  - **Importante:** Ni la URL ni el contenido de la imagen se almacenan permanentemente ni se envían a servidores externos.

### Almacenamiento Local (`chrome.storage.local`)
La extensión guarda localmente:
- Un historial de los códigos QR decodificados exitosamente (contenido del QR, identificador de fuente y fecha/hora).
- Tus preferencias de configuración (modo automático, modo clic-scan, etc.).

Toda esta información se almacena localmente en el navegador y no se transmite a ningún servidor externo. Puedes borrar el historial desde el popup de la extensión.

### Permisos

- **Portapapeles (`clipboardWrite`):** Solo se usa cuando haces clic en "Copiar" junto a un resultado QR. La extensión no accede a tu portapapeles en otros momentos.
- **Pestañas (`tabs`):** Se utiliza para permitir la comunicación entre el popup y el script de contenido de la pestaña activa (por ejemplo, para iniciar el escaneo).  
  No se utiliza para leer tu historial de navegación ni el contenido de otras pestañas.

---

## 2. Recopilación de Datos Personales

No recopilamos, almacenamos ni transmitimos ninguna información de identificación personal (PII) ni datos de navegación que no estén directamente relacionados con la funcionalidad descrita.

---

## 3. Uso de la Información

La información manejada por la extensión se utiliza exclusivamente para:

- Detectar y decodificar códigos QR en las páginas que visitas.
- Mostrarte el historial de QRs encontrados.
- Permitir que copies el contenido de los QRs.
- Guardar y aplicar tus preferencias.
- Facilitar la comunicación interna entre componentes de la extensión.

---

## 4. Intercambio de Información

No compartimos ninguna información manejada por la extensión con terceros. Todo el procesamiento ocurre localmente o dentro de los componentes propios de la extensión.

---

## 5. Seguridad

Utilizamos `chrome.storage.local` para almacenar los datos de forma segura en tu perfil de navegador.  
Sin embargo, como con cualquier software, no podemos garantizar una seguridad absoluta.

---

## 6. Cambios a esta Política de Privacidad

Podemos actualizar esta política ocasionalmente. Notificaremos cualquier cambio en la Chrome Web Store o por otros medios apropiados.  
Te recomendamos revisar esta política periódicamente.

---

## 7. Contacto

Si tienes alguna pregunta sobre esta Política de Privacidad, contáctanos en:  
📧 **anibalgiezpy@gmail.com**
