
[![GitHub stars](https://img.shields.io/github/stars/Representaciones-Pedraja/gh-actions)](https://github.com/Representaciones-Pedraja/gh-actions/stargazers) 
[![GitHub forks](https://img.shields.io/github/forks/Representaciones-Pedraja/gh-actions)](https://github.com/Representaciones-Pedraja/gh-actions/network) 
[![GitHub release](https://img.shields.io/github/v/release/Representaciones-Pedraja/gh-actions)](https://github.com/Representaciones-Pedraja/gh-actions/releases/)
[![Github All Releases](https://img.shields.io/github/downloads/Representaciones-Pedraja/gh-actions/total.svg)](https://github.com/Representaciones-Pedraja/gh-actions/releases/)
[![Github issues](https://img.shields.io/github/issue/Representaciones-Pedraja/gh-actions)](https://github.com/Representaciones-Pedraja/gh-actions/issues)

# GitHub Actions para Representaciones Pedraja

Este repositorio contiene flujos de trabajo de GitHub Actions específicos para automatizar diversas tareas en los proyectos de Representaciones Pedraja.

## Flujos de trabajo disponibles

### 1. **CI/CD Pipeline**
   - **Descripción:** Automatiza la integración continua y el despliegue de código en varios entornos.
   - **Archivos involucrados:** `.github/workflows/ci_cd.yml`
   - **Acciones principales:**
     - Validación de código
     - Generación de artefactos
     - Despliegue en producción (si procede)

### 2. **Backup Automático**
   - **Descripción:** Ejecuta copias de seguridad periódicas de archivos y bases de datos.
   - **Archivos involucrados:** `.github/workflows/backup.yml`
   - **Acciones principales:**
     - Copias de seguridad de bases de datos
     - Compresión y almacenamiento seguro

### 3. **Actualización de Dependencias**
   - **Descripción:** Verifica y actualiza las dependencias de los proyectos automáticamente.
   - **Archivos involucrados:** `.github/workflows/dependency_update.yml`
   - **Acciones principales:**
     - Revisión de versiones
     - Actualización y pruebas automáticas

## Cómo usar

1. **Configura las variables de entorno:** Accede a la configuración del repositorio y define las variables necesarias para cada flujo.
2. **Revisa y personaliza:** Asegúrate de que los parámetros en cada archivo YAML se ajusten a las necesidades de tu proyecto.
3. **Ejecuta el flujo:** Los flujos se ejecutarán automáticamente según los eventos definidos (push, pull request, cron, etc.).

## Requisitos

- **GitHub Secrets:** Asegúrate de definir los secretos necesarios en la configuración del repositorio (p.ej., `DATABASE_URL`, `DEPLOY_KEY`, etc.).
- **Permisos:** Verifica que los permisos de GitHub Actions estén habilitados para este repositorio.

## Estructura del repositorio

```plaintext
.github/
└── workflows/
    ├── ci_cd.yml              # Flujo de CI/CD
    ├── backup.yml             # Flujo de respaldo automático
    └── dependency_update.yml  # Flujo de actualización de dependencias
