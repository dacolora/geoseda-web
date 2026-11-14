# geoseda-web

Página pública de GeoSEDA en <https://geoseda.com>: un HTML estático publicado con GitHub Pages.

Este repositorio es público. No van aquí datos de clientes, geodatabases ni nada confidencial.

## Archivos

| Archivo | Qué es |
|---|---|
| `index.html` | La landing completa: estilos y animaciones (curvas de nivel en canvas) dentro del mismo archivo. |
| `favicon.svg`, `favicon-32.png`, `apple-touch-icon.png` | Íconos de la pestaña y del iPhone. |
| `og.jpg` | Imagen de 1200×630 que se ve al compartir el enlace (WhatsApp, LinkedIn). |
| `CNAME` | Dominio propio para GitHub Pages (`geoseda.com`). |

## DNS (GoDaddy)

| Tipo | Nombre | Valor |
|---|---|---|
| A | @ | 185.199.108.153 |
| A | @ | 185.199.109.153 |
| A | @ | 185.199.110.153 |
| A | @ | 185.199.111.153 |
| CNAME | www | dacolora.github.io |

La plataforma (validación y creación de GDB) se publica aparte en `app.geoseda.com`. Los botones «Entrar» y «Crear
cuenta» de la landing llevan a `https://app.geoseda.com/login` y `/register`; no abren hasta que la plataforma
salga a producción y exista el registro DNS de `app`.

## Probar en local

```bash
python3 -m http.server 4610
```
