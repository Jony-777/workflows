# Workflows - Git Flow & GitHub Actions

## Descripción
Proyecto de demostración para implementar el flujo de trabajo **Git Flow** con **GitHub Actions**.

## Estructura de ramas
- **main**: Rama principal protegida. Solo se actualiza mediante Pull Requests.
- **dev**: Rama de desarrollo donde se integran los cambios antes de ir a producción.
- **build**: Rama generada automáticamente por GitHub Actions con los archivos compilados.

## Flujo de trabajo
1. Se desarrolla en la rama `dev`
2. Se crea un Pull Request de `dev` → `main`
3. Al hacer merge, GitHub Actions ejecuta el workflow `deploy.yml`
4. El workflow compila el proyecto y pushea los archivos a la rama `build`

## Tecnologías
- Vite (Vanilla JS)
- GitHub Actions
- Git Flow

## Comandos útiles
```bash
# Instalar dependencias
npm install

# Servidor de desarrollo
npm run dev

# Compilar para producción
npm run build
```
