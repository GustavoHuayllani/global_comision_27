# 🚀 Guía de Referencia Rápida: Comandos Básicos de Git

> **Objetivo:** Material de consulta rápida para inicializar proyectos locales, registrar versiones y sincronizar cambios con repositorios en **GitHub**.

---

## ⚙️ 0. Configuración Inicial (Solo la primera vez)

Antes del primer guardado, Git requiere asociar tu identidad a cada cambio realizado.

| Comando | Función |
| :--- | :--- |
| `git config --global user.name "Tu Nombre"` | Registra tu nombre en la configuración global de Git. |
| `git config --global user.email "tu_email@ejemplo.com"` | Registra tu correo electrónico asociado a GitHub. |

<pre><code># Ejemplo práctico en terminal:
git config --global user.name "Gustavo"
git config --global user.email "gustavo@ejemplo.com"</code></pre>

---

## 📁 1. Inicialización y Conexión Remota

| Comando | Descripción | Ejemplo de Uso |
| :--- | :--- | :--- |
| `git init` | Inicializa un repositorio Git vacío en la carpeta actual del proyecto. | `git init` |
| `git remote add origin <URL>` | Conecta el proyecto local con el repositorio creado en GitHub. | `git remote add origin https://github.com/usuario/mi-repositorio.git` |
| `git remote -v` | Muestra las URLs remotas vinculadas (`fetch` y `push`) para verificar la conexión. | `git remote -v` |

---

## 📝 2. Preparación y Registro de Cambios

| Comando | Descripción | Ejemplo de Uso |
| :--- | :--- | :--- |
| `git status` | Informa el estado de los archivos (modificados, en preparación o sin seguimiento). | `git status` |
| `git add <archivo>` | Agrega un archivo específico al área de preparación (*staging area*). | `git add index.html` |
| `git add .` | Agrega **todas** las modificaciones del proyecto de una sola vez. | `git add .` |
| `git commit -m "<mensaje>"` | Confirma y guarda permanentemente los cambios con un mensaje descriptivo. | `git commit -m "Estructura inicial del proyecto"` |

---

## 📜 3. Historial y Deshacer Modificaciones

| Comando | Descripción | Ejemplo de Uso |
| :--- | :--- | :--- |
| `git log` | Muestra el registro histórico de confirmaciones (autor, fecha, código hash y mensaje). | `git log` |
| `git reset --hard` | **Cuidado:** Descarta todos los cambios locales no confirmados y regresa al último commit. | `git reset --hard` |

---

## ☁️ 4. Sincronización con GitHub

| Comando | Descripción | Ejemplo de Uso |
| :--- | :--- | :--- |
| `git push -u origin main` | Sube los cambios a la rama principal en GitHub vinculándola por primera vez. | `git push -u origin main` |
| `git push` | Sube los nuevos commits locales a GitHub en las operaciones siguientes. | `git push` |
| `git pull` | Descarga y combina los cambios existentes en GitHub hacia tu máquina local. | `git pull` |

---

## 🔄 Resumen del Flujo de Trabajo Diario

Una vez configurado y vinculado el proyecto, el ciclo habitual de trabajo se ejecuta con estos 4 comandos:

<pre><code># 1. Verificar qué archivos se modificaron
git status

# 2. Preparar todos los cambios
git add .

# 3. Guardar la versión con un mensaje descriptivo
git commit -m "Implementación de nueva funcionalidad"

# 4. Enviar los cambios a GitHub
git push</code></pre>