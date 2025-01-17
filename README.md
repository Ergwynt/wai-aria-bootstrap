## Elementos Mejorados

### 1. **Botón**
- **Descripción**: El botón original de Bootstrap se mantuvo, pero se le agregó el atributo `aria-label` para describir mejor la acción que realiza el botón.
- **Mejora Implementada**:
  - Se eliminó el atributo `role="button"`, ya que el propio elemento `<button>` de HTML ya tiene el rol `button` por defecto.
  - Se mantuvo el atributo `aria-label="Realizar acción"` para proporcionar una descripción más clara y accesible para los usuarios de lectores de pantalla.

### 2. **Menú Desplegable**
- **Descripción**: El menú desplegable de Bootstrap fue modificado para incluir los atributos WAI-ARIA que mejoran la accesibilidad para usuarios de tecnologías de asistencia.
- **Mejora Implementada**:
  - Se agregó `role="navigation"` al contenedor del menú desplegable, lo que indica que el bloque es una sección de navegación.
  - Se añadió `aria-expanded="false"` al botón que controla la expansión del menú. Este atributo indica si el menú está abierto o cerrado, pero debería ser gestionado dinámicamente con JavaScript para cambiar según el estado real del menú.
  - Se agregó `role="menuitem"` a cada uno de los elementos del menú para indicar que son opciones dentro de un menú.

### 3. **Alerta**
- **Descripción**: Se mantuvo el diseño de la alerta de Bootstrap, pero se mejoró la accesibilidad con los atributos `aria-live` y `aria-atomic`.
- **Mejora Implementada**:
  - Se agregó `aria-live="assertive"` para asegurar que los lectores de pantalla anuncien inmediatamente el contenido de la alerta cuando se presenta.
  - Se añadió `aria-atomic="true"` para garantizar que el mensaje completo de la alerta sea leído por el lector de pantalla, incluso si solo cambia una parte del contenido.

### 4. **Navbar (Navegación)**
- **Descripción**: La barra de navegación de Bootstrap fue modificada para mejorar la accesibilidad de las pestañas de navegación.
- **Mejora Implementada**:
  - Se añadió `role="tablist"` al contenedor de las pestañas, lo que indica que es una lista de pestañas navegables.
  - Cada pestaña individual tiene el atributo `role="tab"`, y se añadió `aria-controls`, `aria-selected` y `aria-labelledby` para mejorar la relación entre las pestañas y el contenido que controlan.
  
### 5. **Paginación**
- **Descripción**: El componente de paginación de Bootstrap fue mejorado con atributos WAI-ARIA para garantizar que los usuarios de tecnologías de asistencia puedan navegar correctamente a través de las páginas.
- **Mejora Implementada**:
  - Se cambió el atributo `role="listbox"` a `role="navigation"`, ya que `listbox` no es apropiado para paginación, y `navigation` describe mejor el propósito de este elemento.
  - Se añadió `aria-label` a los enlaces de paginación para describir su función, como "Página anterior", "Ir a la página X", etc.
