# 🚀 Guía de Referencia Rápida: Comandos Básicos de Git

> **Objetivo:** Material de consulta rápida para inicializar proyectos locales, registrar versiones y sincronizar cambios con repositorios en **GitHub**.

---

## ⚙️ 0. Configuración Inicial (Solo la primera vez)

Antes del primer guardado, Git requiere asociar tu identidad a cada cambio realizado.

| Comando | Función |
| :--- | :--- |
| `git config --global user.name "Tu Nombre"` | Registra tu nombre en la configuración global de Git. |
| `git config --global user.email "tu_email@ejemplo.com"` | Registra tu correo electrónico asociado a GitHub. |

```bash
# Ejemplo práctico:
git config --global user.name "Gustavo"
git config --global user.email "gustavo@ejemplo.com"

Comando,Descripción,Ejemplo de Uso
git init,Inicializa un repositorio Git vacío en la carpeta actual del proyecto.,git init
git remote add origin <URL>,Conecta el proyecto local con el repositorio creado en GitHub.,git remote add origin https://github.com/usuario/mi-repositorio.git
git remote -v,Muestra las URLs remotas vinculadas (fetch y push) para verificar la conexión.,git remote -v