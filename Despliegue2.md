# Despliegue de Pokedex en Azure Static Web Apps

Este documento describe los pasos para crear una copia (Fork) del repositorio de Pokedex, configurar la ubicación de la aplicación y desplegarla utilizando Azure Static Web Apps. También se incluye la configuración para cargar las imágenes de los Pokémon.

## Paso 1: Crear un Fork del Repositorio

1.  Dirígete al repositorio fuente en GitHub: [https://github.com/rcuello/ac4dem1a/tree/master/sistemas-distribuidos/poke-dex-lab](https://github.com/rcuello/ac4dem1a/tree/master/sistemas-distribuidos/poke-dex-lab)
2.  En la parte superior derecha de la página, haz clic en el botón **Fork**.
3.  Se te pedirá que elijas un nombre para tu nuevo repositorio. En este caso, escribe **albertacho** y haz clic en **Create fork**.

## Paso 2: Configurar la Ubicación de la Aplicación

1.  Navega a tu repositorio recién creado: [https://github.com/albertacho/albertacho](https://github.com/albertacho/albertacho)
2.  Dirígete a la siguiente ruta: **albertacho/.github/workflows/**
3.  Haz clic en el archivo llamado **azure-static-web-apps-delightful-field-02ef8bb10.yml** (el nombre puede variar ligeramente).
4.  Haz clic en el icono de **Editar** (lápiz) para modificar el archivo.
5.  Busca la línea **#31** que dice:
    ```yaml
    app_location:
    ```
6.  Reemplaza el valor dentro de las comillas dobles (`""`) por la siguiente ruta:
    ```yaml
    app_location: "./sistemas-distribuidos/poke-dex-lab/source/pokedex-angular"
    ```
7.  Haz clic en el botón **Commit changes** en la parte inferior de la página para guardar los cambios.

## Paso 3: Verificar la Aplicación de los Cambios en Actions

1.  En la parte superior de tu repositorio, haz clic en la pestaña **Actions**.
2.  Deberías ver un flujo de trabajo en ejecución (o que se ha completado) relacionado con Azure Static Web Apps. Espera a que este flujo de trabajo termine para asegurarte de que los cambios de configuración se hayan aplicado.

## Paso 4: Acceder a la Aplicación Desplegada en Azure

1.  Dirígete al servicio de **App Services** que creaste en Azure.
2.  Haz clic en el nombre de tu Static Web App.
3.  En la página de información general de tu Static Web App, busca el botón o enlace que diga **Ir al recurso**. Haz clic en él.
4.  Dentro de los detalles del recurso, busca la sección de **URL**. La URL proporcionada es el enlace a tu proyecto Pokedex desplegado en la nube. Haz clic en este enlace para visualizar tu aplicación.

## Paso 5: Configurar las Cabeceras de Seguridad y la Redirección de Navegación

1.  Vuelve a tu repositorio en GitHub: [https://github.com/albertacho/albertacho](https://github.com/albertacho/albertacho)
2.  Navega a la siguiente ruta: **sistemas-distribuidos/poke-dex-lab/source/pokedex-angular/**
3.  Haz clic en el botón **Add file** y selecciona **Create new file**.
4.  Nombra el nuevo archivo **staticwebapp.config.json**.
5.  En el editor del archivo, pega el siguiente código:
    ```json
    {
      "globalHeaders": {
        "Content-Security-Policy": "default-src 'self'; img-src 'self' [https://raw.githubusercontent.com](https://raw.githubusercontent.com) [https://pokeapi.co](https://pokeapi.co) [https://assets.pokemon.com](https://assets.pokemon.com); script-src 'self' 'unsafe-inline'; style-src 'self' 'unsafe-inline' [https://fonts.googleapis.com](https://fonts.googleapis.com); font-src 'self' [https://fonts.gstatic.com](https://fonts.gstatic.com); connect-src 'self' [https://beta.pokeapi.co](https://beta.pokeapi.co)",
        "X-Frame-Options": "DENY",
        "Permissions-Policy": "geolocation=(), microphone=(), camera=()"
      },
      "navigationFallback": {
        "rewrite": "/index.html",
        "exclude": ["/images/", "/css/", "/js/*", "/favicon.ico"]
      }
    }
    ```
6.  Haz clic en el botón **Commit changes** para guardar el archivo.
7.  Ve a la pestaña **Actions** en tu repositorio y espera a que el flujo de trabajo de Azure Static Web Apps se complete para aplicar esta nueva configuración.

## Paso 6: Configurar la Carga de Imágenes de los Pokémon

1.  Dirígete a la siguiente ruta en tu repositorio: **albertacho/sistemas-distribuidos/poke-dex-lab/source/pokedex-angular/src/environments/**
2.  Haz clic en el archivo **environment.prod.ts** para editarlo.
3.  Busca la línea que define la variable `imagesPath`:
    ```typescript
    imagesPath: 'pokedex-angular/assets/images',
    ```
4.  Reemplaza el valor de `imagesPath` con la siguiente ruta:
    ```typescript
    imagesPath: '/assets/images',
    ```
5.  Haz clic en el botón **Commit changes** para guardar los cambios.
6.  Una vez más, ve a la pestaña **Actions** y espera a que el flujo de trabajo de Azure Static Web Apps se complete. Después de esto, las imágenes de los Pokémon deberían aparecer correctamente en tu proyecto desplegado.

¡Listo! Siguiendo estos pasos, deberías tener tu Pokedex desplegada en Azure Static Web Apps con las imágenes de los Pokémon cargando correctamente.
