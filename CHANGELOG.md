# Changelog

Formato basado en [Keep a Changelog](https://keepachangelog.com/es-ES/1.1.0/).

## [Unreleased]

### Added

- Configurado GitHub Actions: `deploy.yml` compila y publica `dist/` en
  GitHub Pages en cada push a `main` (origen "GitHub Actions" de Pages, sin
  rama `gh-pages`); `ci.yml` corre lint y build en cada Pull Request.

### Changed

- Migrado el proyecto de Create React App a Vite, directo a Radix sin pasar
  por baseui: `hecho` solo usaba `Button`, `Input` y el `CategorySelect`
  creatable, ya resueltos en `por-hacer`. Ver el
  [CHANGELOG de por-hacer](https://github.com/tecnocoopcl/por-hacer/blob/main/CHANGELOG.md)
  para el detalle de esa migración y las dos trampas de Radix que costaron
  tiempo ahí (combobox y foco del diálogo).
- `src/ui` reúne `Button`, `Input`, `CategorySelect` y `colorForCategoria`,
  copiados de `por-hacer` hasta que `@newale/ui` se publique.

### Removed

- Eliminados `react-scripts`, `baseui`, `styletron` y el paquete vendorizado
  `@newale/ui`.

## [0.1.0] — Configuración inicial de despliegue

### Added

- Configurado el despliegue en GitHub Pages: `public/CNAME` con
  `hecho.aebn.cl`.
- Commit inicial del proyecto, descomprimido desde el SIP original.
