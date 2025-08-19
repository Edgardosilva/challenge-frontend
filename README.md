# 🎯 SWAG Frontend Challenge

**Tiempo utilizado para la prueba:** 90 minutos exactos


---

## ✅ Bugs Corregidos

- **Búsqueda (Search)**  
  Ahora es **case-insensitive** y maneja correctamente tildes/acentos en español.

- **Ordenamiento por precio**  
  Implementado ordenamiento ascendente (`price-asc`) y descendente (`price-desc`).  
  Se actualizaron las opciones del `<select>` en la UI.

- **Estado de productos (`pending`)**  
  Los productos con estado `pending` ahora se muestran como **Pendiente**, con su propio badge.

- **Stock (validación de cantidad)**  
  Se corrigió el input de cantidad en:
  - **Detalle de producto**: no permite valores menores a 1 ni mayores al stock disponible.  
  - **Calculadora de precios**: mismo comportamiento, usando `clamp` y `maxStock`.  
  Además, los botones `+`/`-` respetan los límites.

- **Formato de precios**  
  Todos los precios se muestran con formato chileno (**CLP**), usando `Intl.NumberFormat('es-CL', { style: 'currency', currency: 'CLP', currencyDisplay: 'code' })`.

- **Cálculo de precios con descuentos por volumen**  
  La calculadora ahora encuentra el **mejor break** aplicable (menor precio unitario efectivo), sin depender del orden del array y soportando tanto `price` como `discount`.

- **Bug de Datos (productos faltantes)**  
  Verificado: el catálogo ya incluye los **20 productos solicitados** en `products.ts`, y se renderizan correctamente en pantalla.  