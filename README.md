# 🎓 Sistema de Formación Integral CUCBA

![Versión](https://img.shields.io/badge/version-1.0.0-gold)
![Licencia](https://img.shields.io/badge/licencia-MIT-black)
![Platform](https://img.shields.io/badge/platform-Web%20%7C%20PWA-blue)

## 📝 Descripción General

El **Sistema de Formación Integral CUCBA** es una plataforma integral diseñada para la administración, registro y validación de las actividades extracurriculares de los estudiantes del **Centro Universitario de Ciencias Biológicas y Agropecuarias (CUCBA)**. 

Este proyecto surge como una respuesta tecnológica para digitalizar procesos que tradicionalmente eran manuales, permitiendo un control preciso de la asistencia y la emisión automática de constancias de cumplimiento de créditos.

---

## 🚀 Características Principales

### 🔹 Gestión de Asistencia mediante QR
* **Generación Dinámica:** Creación de códigos QR únicos para cada evento.
* **Escaneo en Tiempo Real:** Validación inmediata de la asistencia de los alumnos mediante dispositivos móviles.
* **Prevención de Duplicados:** Lógica implementada para evitar registros múltiples de un mismo usuario en el mismo bloque horario.

### 🔹 Automatización de Documentos
* **Generación de PDFs:** Motor integrado para crear constancias oficiales de forma automática una vez que el alumno alcanza el umbral de horas o créditos requerido.
* **Firmas Digitales:** Espacio optimizado para la validación institucional en los documentos generados.

### 🔹 Experiencia de Usuario (UX/UI)
* **Diseño Responsivo:** Interfaz adaptable a computadoras de escritorio, tablets y smartphones.
* **Modo PWA (Progressive Web App):** Capacidad de instalación en la pantalla de inicio del celular, funcionamiento fluido y acceso rápido sin necesidad de tiendas de aplicaciones.

### 🔹 Panel Administrativo
* **Visualización de Datos:** Tablas organizadas para la revisión de listas de asistencia.
* **Filtros Avanzados:** Búsqueda por código de alumno, carrera o tipo de actividad.

---

## 🛠️ Stack Tecnológico

El proyecto está construido bajo una arquitectura moderna de desarrollo web *Vanilla*, priorizando la velocidad de carga y la compatibilidad:

* **Frontend:** HTML5 semántico y CSS3 avanzado (utilizando Flexbox y CSS Grid).
* **Lógica de Negocio:** JavaScript (ES6+) para la manipulación del DOM y lógica de validación.
* **Almacenamiento y Datos:** Implementación de persistencia de datos (Local Storage / Integración API según configuración).
* **PWA:** Service Workers para el almacenamiento en caché y manifiesto de aplicación para la instalación nativa.
* **Librerías Externas:** * *QRCode.js* (o similar) para la generación de códigos.
    * *jsPDF / pdfMake* para la creación de reportes en PDF.

---

## 📦 Estructura del Proyecto

```text
FormacionIntegralCucba/
├── assets/             # Imágenes, iconos y recursos estáticos
├── css/                # Hojas de estilo (layout, componentes, temas)
├── js/                 # Lógica principal, Service Worker y validaciones
├── docs/               # Documentación adicional o manuales de usuario
├── index.html          # Punto de entrada principal (Login/Dashboard)
├── manifest.json       # Configuración para PWA
└── sw.js               # Service Worker para funcionamiento Offline


## 🔒 Privacidad y Seguridad de los Datos

Este proyecto ha sido desarrollado bajo una filosofía de **cero recolección de datos sensibles** y procesamiento local siempre que sea posible. La transparencia es fundamental en las herramientas académicas:

### 🛡️ Compromiso de Privacidad
* **Procesamiento del Lado del Cliente (Client-Side):** La mayor parte de la lógica de generación de PDFs y escaneo de códigos QR ocurre directamente en el navegador del usuario. Esto significa que los datos no viajan a servidores externos innecesarios.
* **Sin Rastreo de Terceros:** El sistema no utiliza cookies de seguimiento, píxeles de publicidad ni herramientas de análisis (como Google Analytics) que puedan comprometer la identidad del estudiante.
* **Almacenamiento Local Seguro:** Se utiliza el almacenamiento del navegador (Local Storage / IndexedDB) únicamente para funciones operativas temporales y persistencia de la sesión del usuario, garantizando que la información permanezca bajo el control del dispositivo del alumno.
* **Cero Recopilación Externa:** No se venden, comparten ni distribuyen bases de datos a entidades externas. El sistema actúa estrictamente como un puente técnico entre el alumno y la administración de Formación Integral.

### 🛂 Control del Usuario
* **Permisos de Cámara:** El acceso a la cámara se solicita exclusivamente para el escaneo de códigos QR y solo se activa cuando el usuario inicia la función de "Pasar Lista". No se graban ni almacenan flujos de video.
* **Derechos ARCO:** Al ser una herramienta de apoyo, el sistema respeta las normativas de protección de datos personales de la Universidad de Guadalajara.

---
