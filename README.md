# Catalogo-Pagina-Pasteleria\

# Checklist — Clonar el catálogo para un cliente nuevo

Este template está armado para reusarse. Casi todo se edita desde el bloque `CONFIG` al principio del `<script>` del HTML. Seguí este orden para no olvidarte nada.

## 1. Repo y proyecto

- [ ] Crear un repo nuevo en GitHub (no reusar el de otro cliente).
- [ ] Copiar el HTML base a ese repo.
- [ ] Crear un proyecto nuevo en Vercel conectado a ese repo.

## 2. Google Sheet del cliente

- [ ] Duplicar la Sheet de referencia (`MIGA_catalogo_productos`) — Archivo → Hacer una copia.
- [ ] Cargar los productos reales del cliente (o dejar unas filas de ejemplo si todavía no los tiene).
- [ ] Confirmar columnas: `categoria | nombre | descripcion | precio | precio_descuento | stock | destacado | imagen`.
- [ ] Publicar: Archivo → Compartir → Publicar en la Web → hoja correspondiente → formato **CSV** → Publicar.
- [ ] Tildar "Republicar automáticamente cuando se realicen cambios".
- [ ] Revisar permisos de Compartir: que **nadie externo pueda editar**, solo ver (la publicación ya es de solo lectura, pero el acceso de edición es otro permiso aparte).
- [ ] Copiar el link CSV publicado.

## 3. Editar el bloque `CONFIG` en el código

- [ ] `brand.name` — nombre del negocio.
- [ ] `brand.heroTitle` / `brand.heroSubtitle` — frase principal y bajada.
- [ ] `brand.footerText` — usuario de Instagram / ciudad.
- [ ] `brand.ogDescription` / `brand.ogImage` — texto e imagen que se ven al compartir el link.
- [ ] `whatsapp` — número del cliente, formato `549` + código de área sin el 0 + número sin el 15.
- [ ] `sheetCsvUrl` — pegar el link CSV publicado en el paso 2.
- [ ] `colors` — paleta del cliente (`paper`, `paperSoft`, `ink`, `wine`, `rose`, `red`, `grey`). El borde (`line`) se calcula solo, no hace falta tocarlo salvo que se quiera algo distinto.
- [ ] `categories` — nombres y descripciones de las categorías del rubro del cliente. El `id` de cada una tiene que coincidir en minúscula con lo que se escriba en la columna `categoria` de la Sheet.

## 4. Logo / favicon (esto no está en CONFIG, se edita a mano)

- [ ] Reemplazar el SVG del favicon (`<link id="favicon">` en el `<head>`).
- [ ] Reemplazar el mismo SVG en el ícono del `nav` y en el de la sección `hero` (son 3 lugares distintos, todos con el mismo dibujo).
- [ ] Si no hay tiempo de armar un ícono a medida, dejar el mismo genérico y avisar que se puede personalizar después.

## 5. Probar antes de mostrarlo

- [ ] Crear una rama nueva en GitHub (nunca commitear directo a `main`).
- [ ] Subir los cambios ahí.
- [ ] Abrir el link de Preview que genera Vercel y revisar: colores, categorías, WhatsApp, carrito, que cargue bien desde la Sheet.
- [ ] Recién ahí, mergear a `main`.

## 6. Extras opcionales

- [ ] Activar Vercel Analytics para este proyecto si el cliente quiere ver tráfico.
- [ ] Conectar dominio propio si el cliente ya tiene uno.
- [ ] Pasar el archivo de instrucciones de la Sheet (pestaña "Instrucciones") explicándole al dueño cómo cargar productos, marcar stock y ofertas.

