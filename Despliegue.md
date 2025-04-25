# 🚀 ¡Despliega tu Pokedex en Azure con Estilo! 🌟

### Link de la web en la nube: [https://delightful-field-02ef8bb10.6.azurestaticapps.net/](https://delightful-field-02ef8bb10.6.azurestaticapps.net/)

✍️ **Autor:** Alberto José Hincapié Martínez   
📂 **Repositorio:** [https://github.com/Albertohincapie11/albertacho](https://github.com/Albertohincapie11/albertacho)   
📚 **Asignatura:** Sistemas Distribuidos   
🎓 **Semestre:** 9no semestre - Ingeniería de Sistemas   
📅 **Fecha:** 13/04/2025 

---

¡Prepárate para llevar tu Pokedex a la nube de una manera súper sencilla y visual! ☁️

## 1. 🍴 ¡A Bifurcar el Código! (Forking Time!) 🛠️

1.  Ve directo al corazón del código Pokedex: [https://github.com/rcuello/ac4dem1a/tree/master/sistemas-distribuidos/poke-dex-lab](https://github.com/rcuello/ac4dem1a/tree/master/sistemas-distribuidos/poke-dex-lab)
2.  En la esquina superior derecha, ¡busca el botón **Fork** y haz clic! 👆
3.  Ponle un nombre genial a tu copia, como **albertacho**, ¡y dale a **Create fork**! 🎉

---

## 2. 🗺️ ¡Navegando a la Ubicación Correcta! (App Location Adventure!) 🧭

1.  ¡Tu nuevo hogar para el código! 🏡 Visita: [https://github.com/albertacho/albertacho](https://github.com/albertacho/albertacho)
2.  Sumérgete en las carpetas: **albertacho/.github/workflows/** 📂
3.  Encuentra el archivo mágico **azure-static-web-apps-delightful-field-02ef8bb10.yml** (¡puede tener un nombre ligeramente diferente!).
4.  ¡Es hora de editar! ✏️ Haz clic en el icono del lápiz.
5.  Busca la línea **#31**:
    ```yaml
    app_location:
    ```
6.  ¡Reemplaza lo que esté entre las comillas por esta ruta secreta! 🤫
    ```yaml
    app_location: "./sistemas-distribuidos/poke-dex-lab/source/pokedex-angular"
    ```
7.  ¡Guarda los cambios con un clic en **Commit changes**! ✅

---

## 3. 🚦 ¡Luces, Cámara, Actions! (Checking the Magic!) ✨

1.  En la parte superior de tu repo, ¡haz clic en **Actions**! 🎬
2.  Verás un flujo de trabajo en acción (o ya terminado) de Azure Static Web Apps. ¡Espera a que diga "completado" para estar seguro! ⏳

---

## 4. 🚀 ¡Despegue a la Nube de Azure! (Azure Deployment!) ☁️

1.  ¡Dirígete a tu **App Services** en Azure! 🌠
2.  Haz clic en el nombre de tu Static Web App.
3.  ¡Busca el botón **Ir al recurso** y haz clic con emoción! 😄
4.  En la sección de **URL**, ¡encontrarás el enlace mágico a tu Pokedex en la web! 🌐 ¡Haz clic para verlo! 👀

---

## 5. 🛡️ ¡Añadiendo Escudos de Seguridad y Rutas Inteligentes! (Security & Navigation!) 🧭

1.  De vuelta a tu repositorio: [https://github.com/albertacho/albertacho](https://github.com/Albertohincapie11/albertacho)
2.  Navega a: **sistemas-distribuidos/poke-dex-lab/source/pokedex-angular/** 📂
3.  ¡Crea un nuevo archivo! ➕ Haz clic en **Add file** y luego en **Create new file**.
4.  ¡Nómbralo con estilo! 🏷️ **staticwebapp.config.json**
5.  ¡Pega este código secreto para la seguridad y navegación! 🔒
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
6.  ¡Guarda los cambios con **Commit changes**! ✅
7.  Ve a **Actions** de nuevo y espera a que la magia de Azure Static Web Apps se complete. ✨

---

## 6. 🖼️ ¡Dando Vida a los Pokémon con Imágenes! (Loading Pokemon Images!) 🎨

1.  Ve a esta ruta en tu repo: **albertacho/sistemas-distribuidos/poke-dex-lab/source/pokedex-angular/src/environments/** 📂
2.  ¡Edita el archivo **environment.prod.ts**! ✏️
3.  Busca la línea de la ruta de las imágenes:
    ```typescript
    imagesPath: 'pokedex-angular/assets/images',
    ```
4.  ¡Cámbiala a esta ruta mágica! ✨
    ```typescript
    imagesPath: '/assets/images',
    ```
5.  ¡Guarda los cambios con **Commit changes**! ✅
6.  ¡Una última visita a **Actions**! ⏳ Espera a que termine el proceso. ¡Y voilà! 🎉 Tus imágenes de Pokémon deberían aparecer.

¡Felicidades! 🎉 Has desplegado tu Pokedex en Azure Static Web Apps y has configurado todo para que luzca increíble. ¡Disfruta de tu Pokedex en la nube! 🚀

---

## 🌟 **Creador del Proyecto** 🙌

<div align="center" style="border: 3px solid #ffcb05; border-radius: 15px; padding: 20px; background: linear-gradient(135deg, #f5f7fa 0%, #e4f0fc 100%); margin: 20px 0;">

[![GitHub Follow](https://img.shields.io/github/followers/Albertohincapie11?style=social&label=Síguelo%20en%20GitHub!)](https://github.com/Albertohincapie11)

### 🧙‍♂️ **Alberto José Hincapié Martínez**  
#### *"Estudiante Apasionado de Ingeniería de Sistemas"*  

[![Portafolio Badge](https://img.shields.io/badge/🎮_Mi_Universo_Digital-GitHub-181717?style=for-the-badge&logo=github)](https://github.com/Albertohincapie11)

</div>

### 🏆 Habilidades Especiales:
- 🛠️ **Auxiliar Multifuncional**: Apoyo en Sistemas. IT y TIC.
- 💻 **Desarrollo de Software**: Full Stack Developer (front-end + back-end)
- 🔐 **Ciberseguridad**: Proteccón de datos y redes.
- 🖥️ **Mantenimiento de Computadores**: Diagnóstico y reparación de equipos.
- 🎨 **Herramientas Digitales**: 
  - Excel: Analisis de datos.
  - Photoshop: Diseño y edición gráfica.
- ⚕️ **SG-SST (50 Horas)**: Formación en seguridad laboral
- 📢 **Marketing Digital**: Estrategias en SEO y redes sociales.
