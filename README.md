# Mermaid Render

## Descripción General

**Mermaid Render** es una herramienta de software basada en tecnologías web (HTML5, CSS3 y JavaScript) diseñada para la creación, edición y visualización en tiempo real de diagramas mediante la sintaxis de **Mermaid.js**. Esta aplicación opera enteramente en el lado del cliente (client-side), eliminando la necesidad de servidores backend o instalaciones complejas, y proporciona un entorno persistente para la gestión de múltiples diagramas dentro de un mismo proyecto.

El sistema integra un editor de código con resaltado de sintaxis, un motor de renderizado dinámico y una interfaz gráfica que permite la manipulación visual (pan y zoom) de los gráficos generados.

## Características Principales

El análisis del código fuente revela las siguientes capacidades funcionales:

* **Renderizado en Tiempo Real:** Visualización inmediata de los cambios realizados en el código fuente del diagrama.
* **Gestión de Proyectos:** Capacidad para agrupar múltiples diagramas (requisitos) bajo un único proyecto.
* **Persistencia de Datos:** Funcionalidad para guardar y cargar proyectos completos mediante archivos en formato JSON.
* **Interfaz Ajustable:** Paneles de edición y visualización redimensionables.
* **Navegación Visual Avanzada:** Controles de *pan* (desplazamiento por arrastre) y *zoom* (mediante rueda del ratón) para inspeccionar diagramas extensos, incluyendo una función de restablecimiento de vista (*Reset View*).
* **Tematización:** Sistema de estilos integrado con seis temas predefinidos (Neutro, Azul, Verde, Ámbar, Púrpura y Oscuro) que inyectan directivas de inicialización de Mermaid automáticamente.
* **Modo de Bloqueo:** Funcionalidad para bloquear el editor en modo "solo lectura" para evitar modificaciones accidentales.
* **Editor de Código:** Implementación de CodeMirror para una experiencia de escritura fluida.

## Requisitos del Sistema

Dado que es una aplicación web estática, los requisitos se limitan a:

* Un navegador web moderno con soporte para JavaScript y ES6 (Chrome, Firefox, Edge, Safari).
* Conexión a internet para la carga de librerías CDN (Mermaid.js, Tailwind CSS, CodeMirror).

## Instalación y Ejecución

La herramienta no requiere un proceso de instalación convencional.

1. Descargue el archivo `index.html`.
2. Abra el archivo directamente con cualquier navegador web compatible.

## Manual de Uso

### 1. Inicio del Proyecto

Al ejecutar la aplicación, se presenta un modal inicial con dos opciones:

* **Cargar Proyecto Existente:** Permite importar un archivo `.json` generado previamente por esta herramienta.
* **Crear Nuevo Diagrama:** Inicia un lienzo en blanco con un diagrama de ejemplo y el tema por defecto.

### 2. Edición de Diagramas

El panel izquierdo contiene el editor de texto. Se utiliza la sintaxis estándar de Mermaid.

* **Creación:** Escriba el código en el editor; el panel derecho reflejará los cambios automáticamente tras una breve pausa (debounce).
* **Estilos:** Utilice el botón de "Palo de Pintura" en la barra superior para seleccionar un tema visual. Esto insertará o modificará la directiva `%%{init: ... }%%` en el código.

### 3. Gestión de Múltiples Diagramas

La barra superior permite administrar los diagramas dentro del proyecto actual:

* **Selector desplegable:** Permite cambiar entre los diferentes diagramas creados.
* **Botón Añadir (+):** Crea un nuevo diagrama vacío dentro del proyecto actual.
* **Renombrar/Eliminar:** Accesible desde el menú desplegable al pasar el cursor sobre un elemento de la lista.

### 4. Navegación en el Visor

El panel derecho permite interactuar con el gráfico generado:

* **Zoom:** Ruede la rueda del ratón para acercar o alejar.
* **Desplazamiento (Pan):** Haga clic izquierdo y arrastre para mover el lienzo.
* **Restablecer:** Pulse el icono de "encuadre" en la barra de herramientas para ajustar el diagrama al tamaño de la ventana.

### 5. Guardado y Exportación

* **Guardar:** El botón con el icono de "disco" descarga un archivo `.json` que contiene todos los diagramas del proyecto y sus metadatos.
* **Cargar:** El botón de "carpeta" permite importar archivos `.json` previamente guardados.

## Detalles Técnicos

La arquitectura de la aplicación se basa en las siguientes librerías de terceros, cargadas vía CDN:

* **Mermaid.js (v10):** Motor de generación de diagramas.
* **CodeMirror (v5.65.15):** Editor de texto embebido.
* **Tailwind CSS:** Framework de utilidades para el diseño de la interfaz.

## Descargo de Responsabilidad (Disclaimer)

Este software se proporciona "tal cual", sin garantía de ningún tipo, expresa o implícita, incluyendo, pero no limitado a, las garantías de comerciabilidad, idoneidad para un propósito particular y no infracción. En ningún caso los autores o titulares de los derechos de autor serán responsables de ninguna reclamación, daño u otra responsabilidad, ya sea en una acción de contrato, agravio o de otro tipo, que surja de, fuera de o en conexión con el software o el uso u otros tratos en el software.

El usuario asume toda la responsabilidad por el uso de esta herramienta y la integridad de los datos generados o cargados en ella.

## Licencia

**Licencia de Uso Libre con Atribución**

Se concede permiso, de forma gratuita, a cualquier persona para obtener una copia de este software y los archivos de documentación asociados, para tratar el Software sin restricciones, incluyendo, sin limitación, los derechos de uso, copia, modificación, fusión, publicación y distribución, sujeto a las siguientes condiciones:

1. **Atribución:** Las redistribuciones del código fuente o versiones modificadas del mismo deben conservar la nota de autoría original y este aviso de licencia.
2. **No Comercialización Directa:** Queda prohibida la venta del software como un producto independiente sin el consentimiento expreso del autor original.

Este aviso de permiso se incluirá en todas las copias o partes sustanciales del Software.
