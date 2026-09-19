# Hecho

Registro diario de actividades por categoría, con estadísticas de horas
dedicadas a cada una. Construido con React, Vite y Radix.

Publicado en https://hecho.aebn.cl

## Requisitos

- Node.js 20 o superior
- npm

## Desarrollo

```bash
npm install
npm run dev
```

El servidor de desarrollo queda en http://localhost:5173

## Comandos

| Comando | Descripción |
| --- | --- |
| `npm run dev` | Servidor de desarrollo con recarga en caliente |
| `npm run build` | Compila la versión de producción en `dist/` |
| `npm run preview` | Sirve localmente lo compilado en `dist/` |
| `npm run lint` | Analiza el código con oxlint |

## Despliegue

El despliegue es automático: `.github/workflows/deploy.yml` compila y publica
`dist/` en GitHub Pages en cada push a `main`, usando el origen "GitHub
Actions" de Pages (Settings → Pages → Build and deployment → Source). El
archivo `public/CNAME` fija el dominio `hecho.aebn.cl`, por lo que el
subdominio debe apuntar por CNAME a `tecnocoopcl.github.io`.

`.github/workflows/ci.yml` corre lint y build en cada Pull Request.

## Sistema de diseño

Los componentes compartidos (Button, Input, CategorySelect) viven en
`src/ui`, construidos sobre [Radix](https://www.radix-ui.com/) y copiados
desde `por-hacer` hasta que se publiquen como `@newale/ui`. Ver
[hecho.md](hecho.md) para lo pendiente.

Los gráficos de la vista de estadísticas usan
[recharts](https://recharts.org/), independiente del sistema de diseño.
