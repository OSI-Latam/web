# Jekyll Setup en VS Code

## ¿Qué es Jekyll?
Jekyll convierte archivos Markdown en un sitio web estático. Lo usamos para hacer la web más fácil de editar.

## Setup Rápido

### 1. Clonar proyecto
```powershell
git clone https://github.com/TU-USUARIO/web.git
code web
```

### 2. Instalar extensiones (VS Code te las sugerirá automáticamente)
- ✅ **Ruby** - Soporte para Ruby
- ✅ **Jekyll Snippets** - Snippets para Jekyll  
- ✅ **Liquid** - Syntax highlighting
- ✅ **Markdown All in One** - Mejor Markdown

### 3. Ejecutar Jekyll
```powershell
# En terminal de VS Code (Ctrl+`)
bundle install
bundle exec jekyll serve

# Abre: http://localhost:4000
```

## Comandos Útiles

```powershell
# Servidor con auto-reload (recomendado para desarrollo)
bundle exec jekyll serve --livereload

# Puerto personalizado si 4000 está ocupado
bundle exec jekyll serve --port 4001

# Construir sitio final
bundle exec jekyll build
```

## Estructura del Proyecto

```
web/
├── _config.yml      # ⚙️ Configuración principal
├── _pages/          # 📄 Páginas del sitio  
├── _includes/       # 🧩 Componentes reutilizables
├── _layouts/        # 🎨 Plantillas
├── _sass/           # 🎯 Estilos CSS
├── assets/          # 📁 Imágenes, JS, CSS compilado
└── _site/           # 🚫 Sitio generado (no editar)
```

## Editar Contenido

### Editar páginas existentes
Las páginas están en `_pages/`. Ejemplo:
- `_pages/about.md` - Página "Acerca de"
- `_pages/projects.md` - Página de proyectos

### Crear nueva página
1. **Ctrl+N** → Nuevo archivo
2. Guardar en `_pages/mi-pagina.md`

```markdown
---
layout: page
title: "Mi Nueva Página"
permalink: /mi-pagina/
---

# Mi contenido aquí

Texto en **Markdown**.
```

### Ver cambios en tiempo real
- Ejecuta `bundle exec jekyll serve --livereload`
- Abre http://localhost:4000
- Edita archivos → Se actualiza automáticamente en navegador

## Problemas Comunes

### Error: "Could not find gem"
```powershell
bundle clean --force
bundle install
```

### Puerto 4000 ocupado
```powershell
# Usar otro puerto
bundle exec jekyll serve --port 4001
```

### Cambios no se ven
- Verifica que Jekyll esté corriendo
- Actualiza navegador con **Ctrl+R**
- Revisa errores en terminal

### Ruby/Jekyll no instalado
1. Instala **Ruby** desde [rubyinstaller.org](https://rubyinstaller.org/) (Windows)
2. Reinicia VS Code
3. Ejecuta `bundle install`

---
