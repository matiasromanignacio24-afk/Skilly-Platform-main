# React + Vite

This template provides a minimal setup to get React working in Vite with HMR and some ESLint rules.

Currently, two official plugins are available:

- [@vitejs/plugin-react](https://github.com/vitejs/vite-plugin-react/blob/main/packages/plugin-react) uses [Oxc](https://oxc.rs)
- [@vitejs/plugin-react-swc](https://github.com/vitejs/vite-plugin-react/blob/main/packages/plugin-react-swc) uses [SWC](https://swc.rs/)

## React Compiler

The React Compiler is not enabled on this template because of its impact on dev & build performances. To add it, see [this documentation](https://react.dev/learn/react-compiler/installation).

## Expanding the ESLint configuration

If you are developing a production application, we recommend using TypeScript with type-aware lint rules enabled. Check out the [TS template](https://github.com/vitejs/vite/tree/main/packages/create-vite/template-react-ts) for information on how to integrate TypeScript and [`typescript-eslint`](https://typescript-eslint.io) in your project.

## Configuracion local de la API

La API lee DJANGO_SECRET_KEY, DB_NAME, DB_USER, DB_PASSWORD, DB_HOST y DB_PORT desde variables de entorno. No subas una contrasena ni una clave real al repositorio.

En PowerShell define las variables solo en la terminal que usaras para iniciar Django. Ejemplo:

    $env:DJANGO_SECRET_KEY = "genera-una-clave-local"
    $env:DB_NAME = "Skilly2"
    $env:DB_USER = "postgres"
    $env:DB_PASSWORD = "tu-clave-local"
    $env:DB_HOST = "localhost"
    $env:DB_PORT = "5432"
    python backend/manage.py runserver

Cambia tu-clave-local por la contrasena configurada en PostgreSQL. DEBUG permanece habilitado para desarrollo local. Antes de desplegar, configura una clave propia y DEBUG=False.
