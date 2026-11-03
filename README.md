# MiPlata

App personal de finanzas para llevar en un solo lugar mis ingresos, gastos, préstamos, el dinero que guardo de otras personas y la tarjeta de crédito. Funciona en el navegador (computador y celular) y se publica con GitHub Pages.

## Qué hace

- **Mi dinero vs. dinero en custodia.** Separa la plata que es mía de la que otras personas me dan a guardar (por ejemplo, la de mi mamá o la de un grupo). Un gasto puede pagarse con dinero propio o con el de alguien más, y se descuenta de quien corresponde.
- **Ingresos por fuente:** trabajo, Airbnb y otros.
- **Gastos por categoría**, con búsqueda en todos los movimientos y filtros por tipo.
- **Tarjeta de crédito.**
  - Cada compra se registra como un gasto con su categoría real y su número de cuotas.
  - El pago mensual se registra aparte: baja el dinero disponible y la deuda, pero no se cuenta como gasto (las compras ya se contaron).
  - La app muestra la deuda total, que debe coincidir con el "saldo utilizado" del banco.
- **Préstamos** (presté / me prestaron) con abonos parciales editables. Un préstamo puede marcarse como pagado con la tarjeta.
- **Dividir un gasto:** al registrar un gasto se puede indicar que alguien debe una parte; se crea el gasto propio y el préstamo automáticamente.
- **Cuadre de cuentas:** se escriben los saldos reales de cada cuenta y la deuda real de la tarjeta, y la app muestra la diferencia y permite crear un ajuste visible para dejarla igual a la realidad.
- **Tendencias** mes a mes (ingresos, gastos y balance), tema claro/oscuro y diseño adaptado a celular.

## Dónde quedan los datos

**Este repositorio no contiene datos financieros.** Solo tiene el código de la app.

- Los datos se guardan en el navegador de cada dispositivo (`localStorage`).
- Opcionalmente se sincronizan entre dispositivos con Firebase Firestore. La configuración de Firebase y el código de sincronización se pegan desde *Ajustes → Sincronización en la nube* en cada dispositivo, y no se suben al repositorio.
- Desde *Ajustes → Respaldo manual* se puede exportar todo a un archivo `.json` o importarlo. Importar **reemplaza** los datos actuales.

> No subas al repositorio archivos de respaldo (`miplata-*.json`) ni la configuración de Firebase: el repositorio es público.

## Uso

- **Computador:** abrir la URL de GitHub Pages.
- **Android (Chrome):** abrir la URL → menú ⋮ → *Agregar a la pantalla principal* / *Instalar app*. Queda con su ícono, como una app.
- Cada cambio se guarda solo. Al abrir la app en otro dispositivo con la sincronización activa, carga lo último de la nube.

## Archivos

| Archivo | Para qué sirve |
|---|---|
| `index.html` | La app completa (React precompilado, estilos y lógica en un solo archivo) |
| `manifest.webmanifest` | Permite instalarla en el celular con nombre e ícono |
| `icon-192.png`, `icon-512.png` | Íconos de la app |

## Publicar cambios

Reemplazar `index.html` (y los demás archivos si cambian) en la rama `main`. GitHub Pages publica en uno o dos minutos. En el celular, cerrar la app y volver a abrirla para cargar la versión nueva **antes de registrar movimientos**.
