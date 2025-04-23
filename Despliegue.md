# 🚀 Despliegue de un sitio en Azure Static Web Apps mediante un Fork en GitHub (100% en la nube)

### Link de la web en la nube: [https://delightful-field-02ef8bb10.6.azurestaticapps.net/](https://delightful-field-02ef8bb10.6.azurestaticapps.net/)

✍️ **Autor:** Alberto José Hincapié Martínez   
📂 **Repositorio:** [https://github.com/Albertohincapie11/albertacho](https://github.com/Albertohincapie11/albertacho)   
📚 **Asignatura:** Sistemas Distribuidos   
🎓 **Semestre:** 9no semestre - Ingeniería de Sistemas   
📅 **Fecha:** 13/04/2025 

---
---

## 🧾 Requisitos Previos

- Cuenta de GitHub.
- Cuenta de Azure.

---

## 1. 🔱 Haz un Fork del Repositorio

1. Ve al repositorio original en GitHub.  
2. Haz clic en el botón **"Fork"** (arriba a la derecha).  
3. Selecciona tu cuenta como destino del fork.  
4. (Opcional) Cambia el nombre del repositorio fork si lo deseas.

---

## 2. ☁️ Crea una Static Web App en Azure

1. Accede al [Portal de Azure](https://portal.azure.com).
2. Busca **"Static Web Apps"** y haz clic en **Crear**.
3. Llena los campos requeridos:

   - **Subscription:** tu suscripción activa de Azure.
   - **Resource Group:** crea uno nuevo o selecciona uno existente.
   - **Name:** un nombre único para tu aplicación.
   - **Region:** selecciona la región más cercana a tus usuarios.
   - **Deployment source:** elige GitHub.

4. Autoriza a Azure a acceder a tu cuenta de GitHub si es la primera vez.
5. Selecciona el repositorio fork que creaste.
6. Selecciona la rama principal (main o master).
7. En la sección **Build Details**:

   - **Build Presets:** selecciona el tipo de aplicación (React, Angular, Vue, etc.) o "Custom".
   - **App location:** ruta raíz del código fuente (por ejemplo `/` si está en la raíz).
   - **Output location:** carpeta donde se genera el sitio compilado (por ejemplo `dist`, `build`, etc.).

8. Revisa y haz clic en **Crear**.

---

## 3. 🛡️ Configura seguridad con `staticwebapp.config.json`

Para agregar cabeceras de seguridad HTTP, crea un archivo en tu repositorio llamado:

```
staticwebapp.config.json
```

Coloca el siguiente contenido:

```json
{
  "globalHeaders": {
    "Content-Security-Policy": "default-src 'self'; img-src 'self' https://raw.githubusercontent.com https://pokeapi.co https://assets.pokemon.com; script-src 'self' 'unsafe-inline'; style-src 'self' 'unsafe-inline' https://fonts.googleapis.com; font-src 'self' https://fonts.gstatic.com; connect-src 'self' https://beta.pokeapi.co",
    "X-Frame-Options": "DENY",
    "Permissions-Policy": "geolocation=(), microphone=(), camera=()"
  },
  "navigationFallback": {
    "rewrite": "/index.html",
    "exclude": ["/images/", "/css/", "/js/*", "/favicon.ico"]
  }
}
```

📌 **Este archivo debe estar en la raíz del directorio de salida** (por ejemplo, dentro de la carpeta `dist/` si usas Angular, o `build/` si usas React).

---

## 4. 🤖 GitHub Actions se configura automáticamente

Azure agregará automáticamente un archivo de flujo de trabajo (`.github/workflows/azure-static-web-apps-<algo>.yml`) a tu repositorio fork.

Asegúrate de **verificar y ajustar la ruta** donde se encuentra tu aplicación en ese archivo. Este flujo define los pasos para construir y desplegar tu app cada vez que haces un cambio.

---

## 5. ✅ Primer despliegue automático

Una vez creada la Static Web App, Azure ejecutará el flujo de trabajo y desplegará tu aplicación automáticamente.

Puedes monitorear el proceso en:

- El **Portal de Azure** → tu recurso de Static Web App.
- En **GitHub** → pestaña **Actions** del repositorio fork.

---

## 6. 🌐 ¡Tu sitio ya está publicado!

Una vez completado el flujo de trabajo, tendrás una URL como esta:

👉 [https://white-field-0177d4a10.6.azurestaticapps.net/](https://white-field-0177d4a10.6.azurestaticapps.net/)

Puedes:

- Visitar la URL para ver tu sitio.
- Configurar un **dominio personalizado** desde el portal de Azure.

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
