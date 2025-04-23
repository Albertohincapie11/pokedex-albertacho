# 🧪 Despliegue del Proyecto Pokedex en Azure Static Web Apps

## 1️⃣ Fork del Repositorio

1. Ingresamos al siguiente repositorio en GitHub:  
   [https://github.com/rcuello/ac4dem1a](https://github.com/rcuello/ac4dem1a/tree/master/sistemas-distribuidos/poke-dex-lab)

2. Damos click en el botón **Fork** en la parte superior derecha.

3. Nombramos nuestro nuevo repositorio, por ejemplo: `albertacho`.

---

## 2️⃣ Configurar Ruta de Aplicación en el Workflow de Azure

1. Entramos al nuevo repositorio creado (en este caso, `albertacho`).

2. Navegamos hasta:  
   `.github/workflows/azure-static-web-apps-delightful-field-02ef8bb10.yml`

3. Damos click en **Edit**.

4. Buscamos la línea **#31** donde está la propiedad `app_location:` y modificamos su valor por:
   ```yaml
   app_location: "./sistemas-distribuidos/poke-dex-lab/source/pokedex-angular"
