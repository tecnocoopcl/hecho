# Por hacer

## Sistema de diseño

- [ ] Publicar `@newale/ui` y consumirlo desde ahí en vez de mantener una
      copia de `src/ui` duplicada en `por-hacer` y en `hecho`.

## Despliegue

- [ ] Verificar en GitHub que Pages esté activado (Settings → Pages, fuente
      "GitHub Actions").
- [ ] Agregar el registro DNS `CNAME` de `hecho.aebn.cl` apuntando a
      `tecnocoopcl.github.io`, sin proxy de Cloudflare (DNS only).
- [ ] Hacer push de la rama `feat/vite-migration` a `main`.

## Posibles mejoras

- [ ] `recharts` pesa buena parte del bundle (~130 kB gzip de los ~200 kB
      totales). Si el gráfico de estadísticas se usa poco, evaluar cargarlo
      con `import()` dinámico para no pagar ese peso en la carga inicial.
