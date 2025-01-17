# Mejora de Accesibilidad en Elementos de Bootstrap con Atributos WAI-ARIA

## Elementos Mejorados

### 1. **Botón**
- **Descripción**: Para mejorar la accesibilidad del botón, añadí un atributo `aria-label` que describe su acción, lo que facilita a los usuarios de lectores de pantalla entender su propósito.
- **Mejoras Implementadas**:
  - Añadí el atributo `aria-label="Realizar acción"` para proporcionar una descripción más clara del propósito del botón para los usuarios que utilicen tecnologías de asistencia.

### 2. **Menú Desplegable**
- **Descripción**: El menú desplegable fue mejorado para ser más accesible mediante el uso de atributos WAI-ARIA que indican su estado y la relación entre los elementos.
- **Mejoras Implementadas**:
  - Añadí `role="navigation"` al contenedor del menú, para que sea más claro que este bloque es una sección de navegación.
  - Añadí `aria-expanded="false"` al botón que controla la apertura del menú, lo que indica si el menú está abierto o cerrado.
  - Asigné `role="menuitem"` a cada uno de los elementos dentro del menú, para indicar que son opciones dentro de un menú.

### 3. **Alerta**
- **Descripción**: Implementé mejoras en el componente de alerta para garantizar que los usuarios de lectores de pantalla reciban información sobre su contenido de forma inmediata.
- **Mejoras Implementadas**:
  - Añadí `aria-live="assertive"` para asegurar que la alerta sea anunciada inmediatamente por los lectores de pantalla.
  - Usé `aria-atomic="true"` para garantizar que el mensaje completo de la alerta se lea, incluso si solo cambia una parte del contenido.

### 4. **Navbar (Navegación)**
- **Descripción**: Mejoré la accesibilidad de las pestañas de navegación utilizando los atributos adecuados para describir la relación entre las pestañas y el contenido que controlan.
- **Mejoras Implementadas**:
  - Añadí `role="tablist"` al contenedor de las pestañas para indicar que es un grupo de pestañas navegables.
  - Cada pestaña tiene el atributo `role="tab"`, y además agregué `aria-controls`, `aria-selected` y `aria-labelledby` para asegurar que se identifiquen correctamente las pestañas y su contenido asociado.

### 5. **Paginación**
- **Descripción**: Mejoré la paginación para hacerla más accesible, permitiendo que los usuarios comprendan mejor su propósito y puedan navegar fácilmente entre las páginas.
- **Mejoras Implementadas**:
  - Cambié el atributo `role="listbox"` por `role="navigation"`, ya que `listbox` no es adecuado para la paginación y `navigation` describe mejor su propósito.
  - Añadí `aria-label` a los enlaces de paginación para describir claramente las acciones de cada enlace, como "Página anterior", "Ir a la página X", etc.
