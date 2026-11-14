<!-- perforlegacy:readme:start (generado por Perforlegacy; se sobrescribe al guardar el proyecto) -->
# test

![Perforlegacy](https://img.shields.io/static/v1?label=Perforlegacy&message=proyecto&color=C01674) ![Windows](https://img.shields.io/static/v1?label=Windows&message=10%2B&color=3A4F8C)

## De qué se trata

Este repositorio es un proyecto de Perforlegacy. Automatiza una aplicación de escritorio en Windows mirando la pantalla: no lee el código ni el DOM. Cada test es un flujo grabado de clics, teclado y esperas. Los pasos reconocen botones y textos por imágenes, visión y OCR, y los vuelven a encontrar si la ventana se movió.

- Grabás el flujo con la aplicación abierta.
- Cada paso guarda la imagen de lo que hay que encontrar.
- Las imágenes compartidas viven en `assets/` y se reutilizan entre tests.
- Una suite corre varios tests en un entorno (DEV, QA, PREPROD o PROD). Los secretos no se guardan en el repositorio.

## Estructura del proyecto

- `tests/` — flujos grabados. Cada carpeta tiene `test.json` y las imágenes de sus pasos.
- `flows/` — trozos de flujo reutilizables desde varios tests.
- `suites/` — grupos de tests para correrlos juntos.
- `assets/` — librería de imágenes compartida.
- `environments.json` — entornos. No incluye secretos.
- `.perforlegacy/project.json` — nombre, descripción y aplicación bajo prueba.

> [!WARNING]
> Se guardan en el disco del proyecto. `.gitignore` solo evita subirlos al repositorio: son resultados de esta máquina, no la definición de los tests.
> 
> - `runs/` — historial de cada ejecución: resultado, línea de tiempo, logs y capturas.
> - `reports/` — el HTML o PDF que se escribe al exportar el reporte de una suite.
> - `recordings/` — carpeta local que la app crea y deja vacía. Lo grabado se guarda en `tests/`.

## Cómo ejecutar

> [!TIP]
> 1. Instalá Perforlegacy (Windows 10 o posterior).
> 2. Abrí esta carpeta como proyecto, o cloná el repositorio.
> 3. Elegí el entorno y ejecutá un test o una suite.
<!-- perforlegacy:readme:end -->
