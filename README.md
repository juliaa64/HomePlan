# 🛒 HomePlan App

Una aplicación web progresiva (**PWA**) rápida y colaborativa para la gestión de diferentes aspectos relacionados con la organización en el hogar, desarrollada con **Flutter Web** y respaldada por la infraestructura en la nube de **Supabase**.

[![Flutter](https://img.shields.io/badge/Flutter-3.x-02569B?style=for-the-badge&logo=flutter&logoColor=white)](https://flutter.dev)
[![Supabase](https://img.shields.io/badge/Supabase-Backend-3ECF8E?style=for-the-badge&logo=supabase&logoColor=white)](https://supabase.com)
[![GitHub Pages](https://img.shields.io/badge/Deployment-GitHub%20Pages-222222?style=for-the-badge&logo=github&logoColor=white)](https://pages.github.com)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg?style=for-the-badge)](LICENSE)

---

## 🌐 Demo en vivo

Puedes probar la aplicación directamente desde cualquier navegador o dispositivo móvil:

👉 **[Abrir Aplicación Web](https://juliaa64.github.io/homePlan/)**

---

## ✨ Características principales

- 🔒 **Autenticación completa:** Registro e inicio de sesión persistente gestionado mediante tokens de Supabase Auth.
- 🛡️ **Seguridad granular (RLS):** Implementación estricta de *Row Level Security* en PostgreSQL para aislar los datos privados de cada usuario.
- ⚡ **Sincronización en tiempo real:** Uso de *Supabase Realtime Streams* para reflejar cambios en las listas y productos sin necesidad de recargar.
- 📱 **Experiencia tipo app nativa (PWA):** Totalmente adaptada para instalarse en la pantalla de inicio de iOS (Safari) y Android sin pasar por las tiendas de aplicaciones.
- 🎨 **Diseño adaptativo con Material 3:** Interfaz intuitiva y optimizada tanto para escritorio como para pantallas táctiles.

---

## 🏗️ Arquitectura técnica

## 🏗️ Estructura del despliegue (Web Build)

El repositorio aloja exclusivamente los artefactos compilados para producción generados por Flutter Web, listos para ser servidos por GitHub Pages:

```text
├── assets/                  # Recursos estáticos, fuentes e imágenes
├── canvaskit/               # Motor de renderizado CanvasKit (WebAssembly)
├── icons/                   # Iconos adaptativos PWA para múltiples resoluciones
├── .last_build_id           # Identificador de la última compilación
├── favicon.jpg              # Icono para la pestaña del navegador
├── flutter.js               # Script de carga e inicialización del runtime de Flutter
├── flutter_bootstrap.js     # Script de arranque y configuración de la app
├── flutter_service_worker.js# Service Worker para caché offline y soporte PWA
├── index.html               # Punto de entrada HTML con ruta base y metadatos
├── main.dart.js             # Código fuente Dart compilado a JavaScript
├── manifest.json            # Manifiesto PWA para instalación en iOS / Android
└── version.json             # Información de versión y compilación