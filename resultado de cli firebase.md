¡Entendido! Como tu desarrollador guía, he preparado este manual técnico estructurado para preparar tu entorno de trabajo. Configurar correctamente el **CLI de Firebase** y **Node.js** es el "cimiento" de tu proyecto `xflutterjaziel1194`.

---

## 🟢 1. Software Base: Node.js y NPM en Windows

Para usar Firebase CLI, necesitamos el motor de **Node.js**, que incluye **NPM** (Node Package Manager).

### Cómo verificar si ya lo tienes:
Abre tu terminal (PowerShell o CMD) y escribe:
```bash
node -v
npm -v
```
* **Si aparece una versión (ej. v20.x.x):** ¡Estás listo!
* **Si dice "no se reconoce como un comando":** Sigue los pasos de instalación.

### Instalación paso a paso de Node.js:
1.  **Descarga:** Ve a [nodejs.org](https://nodejs.org/) y elige la versión **LTS** (Long Term Support), es la más estable.
2.  **Ejecución:** Abre el instalador `.msi`.
3.  **Configuración Global:** Durante la instalación, asegúrate de que la opción **"Add to PATH"** esté seleccionada (esto es lo que permite usarlo de manera "global").
4.  **Finalización:** Haz clic en "Next" hasta terminar y **reinicia tu terminal** para que reconozca los cambios.

---

## 🔥 2. Instalación de Firebase CLI

Una vez instalado Node.js, instalaremos las herramientas de Firebase de forma global.

### Instalación Global de `firebase-tools`:
En tu terminal, ejecuta el siguiente comando:
```bash
npm install -g firebase-tools
```
> **¿Qué significa `-g`?** Indica que la instalación es **global**, permitiéndote usar el comando `firebase` en cualquier carpeta de tu computadora, incluyendo tu proyecto `crud_libreria`.

---

## 🛠️ 3. Comandos Esenciales de Firebase

### Cómo acceder a Firebase con tu Cuenta de Google
Para que tu computadora tenga permiso de modificar tus proyectos de consola, debes loguearte:

1.  **Comando de inicio:**
    ```bash
    firebase login
    ```
2.  **Proceso:** Se abrirá automáticamente una pestaña en tu navegador.
3.  **Selección:** Elige la cuenta de Google donde creaste el proyecto de Firebase.
4.  **Autorización:** Haz clic en "Permitir". Al regresar a la terminal, verás un mensaje de éxito: `Success! Logged in as usuario@gmail.com`.

### Cómo usar `firebase-tools` en Flutter
Para vincular tu aplicación Flutter específicamente, se utiliza el comando de configuración que automatiza todo:

1.  **Instalar FlutterFire CLI (Recomendado):**
    ```bash
    dart pub global activate flutterfire_cli
    ```
2.  **Configurar el proyecto:**
    Dentro de tu carpeta `crud_libreria`, ejecuta:
    ```bash
    flutterfire configure
    ```
    *Este comando te permitirá seleccionar tu proyecto de la consola y creará automáticamente el archivo `firebase_options.dart` con todas las credenciales.*

---

## 📁 4. Flujo de Trabajo: Agentes y Skills (Metodología)

Para tu práctica de **Antigravity**, aquí tienes cómo se divide el flujo de trabajo para el **CRUD de Empleados**:



| Componente | Rol / Responsabilidad | Acción en el Proyecto |
| :--- | :--- | :--- |
| **Agente (Controller)** | Orquestador | Recibe los datos del formulario de la UI y decide qué "Skill" llamar. |
| **Rol (Model)** | Contrato de Datos | Define que un "Empleado" tiene: `Nombre` (String), `Edad` (int) y `Puesto` (String). |
| **Skill (Service)** | Ejecutor Técnico | Contiene la lógica pura de Firebase: `add()`, `update()`, `delete()`. |
| **Workflow** | Flujo de Trabajo | El usuario pulsa "Guardar" ➔ Agente valida ➔ Skill envía a Firestore. |

### Resumen de comandos útiles:
* `firebase projects:list` : Lista todos tus proyectos activos en la nube.
* `firebase logout` : Cierra la sesión actual.
* `npm update -g firebase-tools` : Mantiene tus herramientas actualizadas.

**¿Deseas que procedamos ahora con el código detallado para el Agente y el Skill de este flujo de trabajo?**
