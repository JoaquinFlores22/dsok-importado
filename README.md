# DSOK.IMPORTADO — Rediseño (Tailwind CSS)

## Archivos
- `index.html` — la página, usa clases de Tailwind directamente
- `output.css` — el CSS ya compilado (esto es lo que carga index.html, no lo edites a mano)
- `input.css` — el "código fuente" del estilo: acá está tu paleta, tipografías y componentes (.tag, .chip, .cta-btn, etc)
- `package.json` — dependencias del proyecto

## Cómo volver a compilar si editás algo
Si cambiás clases en index.html o algo en input.css, tenés que recompilar:

1. Instalar dependencias (una sola vez): `npm install`
2. Compilar: `npx @tailwindcss/cli -i input.css -o output.css --minify`

Eso regenera output.css con los cambios. Sin este paso, los cambios en las clases de Tailwind no se ven.

## Nota
Este es solo el frontend (diseño visual). El catálogo de productos, carrito y checkout
siguen funcionando con Jotform como ya lo tenían — falta integrar/embeber ese motor acá.

## Sobre el catálogo de productos
El catálogo se conecta directo a la misma Google Sheet que ya usa DSOK (fetch de solo lectura).
El botón "PEDIR" está en modo DEMO a propósito — muestra un aviso en vez de mandar el pedido
al Google Apps Script real de ellos, para no ensuciarles su hoja de pedidos con datos de prueba
mientras esto es solo una propuesta. Para producción, hay que reconectar ese botón al mismo
flujo de carrito + WhatsApp que ya tienen funcionando (código de referencia disponible).
