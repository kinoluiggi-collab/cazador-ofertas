# 🎬 Cazador — Blu-ray & Vinilos MX

Cazador de ofertas de Blu-ray y vinilos en Mercado Libre MX y Amazon MX. Búsqueda en tiempo real con filtros por formato y ordenamiento por precio. Sin backend, sin claves API — funciona 100% desde el browser.

## Demo

> Despliega en GitHub Pages y agrega la URL aquí.

## Características

- Búsqueda simultánea en **Mercado Libre MX** (API oficial) y **Amazon MX** (vía proxy CORS)
- Filtros por formato: Blu-ray · Vinilo/LP · 4K UHD · DVD · CD
- Ordenamiento por precio (↑↓) y título
- Toggle para activar/desactivar cada fuente
- Sin registro, sin backend, sin claves

## Cómo usar localmente

Abre `index.html` directamente en el navegador. No requiere servidor.

## Cómo desplegar en GitHub Pages

1. Sube `index.html` al repositorio
2. Ve a **Settings → Pages**
3. Source: `Deploy from a branch` → `main` → `/ (root)`
4. En ~1 minuto estará disponible en `https://tuusuario.github.io/nombre-repo`

## Notas técnicas

- **Mercado Libre**: usa la [API pública](https://developers.mercadolibre.com.mx/es_ar/items-y-busquedas) sin autenticación (límite ~50 req/día por IP en modo público).
- **Amazon MX**: usa [corsproxy.io](https://corsproxy.io) para hacer fetch de las páginas de búsqueda y parsear el DOM. Es la parte más frágil — puede fallar si Amazon cambia su HTML o el proxy tiene rate limit. Para uso más robusto considera [Rainforest API](https://rainforestapi.com).
- La detección de formato es por keywords en el título del producto.

## Posibles mejoras

- [ ] Filtro de precio máximo
- [ ] Paginación / "cargar más"
- [ ] Historial de búsquedas recientes
- [ ] Integración con Rainforest API para Amazon más confiable
- [ ] PWA / modo offline

## Licencia

MIT
