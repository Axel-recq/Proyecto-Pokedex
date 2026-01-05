# ⚡ Pokédex SPA (React + Vite)

Aplicación de Página Única (SPA) de alto rendimiento para la consulta de datos Pokémon, desarrollada implementando una arquitectura modular basada en componentes y consumo de APIs RESTful.

![Status](https://img.shields.io/badge/Status-En_Desarrollo-yellow?style=flat-square)
![License](https://img.shields.io/badge/License-MIT-blue?style=flat-square)

## 🛠 Stack Tecnológico

El proyecto utiliza un stack moderno optimizado para velocidad de desarrollo (DX) y rendimiento en producción:

| Categoría | Tecnología | Propósito |
| :--- | :--- | :--- |
| **Core** | [React 18+](https://react.dev/) | Librería de UI basada en Virtual DOM. |
| **Build Tool** | [Vite 7+](https://vitejs.dev/) | Bundler de nueva generación (ESM nativo). |
| **Estilos** | [Sass (SCSS)](https://sass-lang.com/) | Preprocesador CSS con arquitectura de **CSS Modules**. |
| **HTTP Client** | [Axios](https://axios-http.com/) | Manejo de peticiones asíncronas a la PokeAPI. |
| **Iconografía** | [React Icons](https://react-icons.github.io/) | Inclusión optimizada de SVGs. |

## 🏗 Arquitectura del Proyecto

El proyecto sigue una **Arquitectura basada en Funcionalidades (Feature-based)** con **Colocación (Co-location)**. Cada componente vive en su propia carpeta junto con sus estilos y lógica específica, facilitando la escalabilidad y el mantenimiento.

```text
/src
├── /api           # Capa de servicios (Configuración de Axios y endpoints)
│   └── apiRest.js
├── /assets        # Recursos estáticos (imágenes, SVGs)
├── /pages         # Vistas principales de la aplicación (Módulos)
│   └── /home      # Módulo: Página de Inicio
│       ├── /card    # Componente: Tarjeta de Pokémon (Lógica + Estilos)
│       ├── /header  # Componente: Cabecera (Lógica + Estilos)
│       └── /layout  # Componente: Layout principal del Home
├── /styles        # Estilos globales y resets
│   └── index.scss
├── App.jsx        # Componente Raíz y enrutamiento base
└── main.jsx       # Punto de entrada (Montaje en el DOM)