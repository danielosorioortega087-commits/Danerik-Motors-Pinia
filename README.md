# Danerik Motors — Nuxt 4 + Pinia

Tienda reconstruida siguiendo la estructura y el patrón Options Store del proyecto `ejemplopinia` y su video.

## Patrón aplicado
- `app/stores/tienda.ts`: `defineStore('tienda', { state, getters, actions })`.
- Los componentes obtienen la misma instancia con `useTiendaStore()`.
- `storeToRefs(tienda)` se utiliza para extraer estado y getters sin perder reactividad.
- Los componentes son independientes: no se pasan datos por props ni se notifican acciones por emits.
- `finalizarCompra()` es una action asíncrona con `async/await`.
- Pinia mantiene el estado compartido durante la navegación dentro de la aplicación.

## Ejecutar
```bash
npm install
npm run dev
```

## Estructura
```text
app/
  app.vue
  assets/main.css
  components/
    AppHeader.vue
    ListaProductos.vue
    CarritoCompra.vue
    FacturaCompra.vue
    AppFooter.vue
  pages/index.vue
  stores/tienda.ts
public/
  logo-danerik.jpeg
  img/
nuxt.config.ts
package.json
```
