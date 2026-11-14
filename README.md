# geoseda-web

Página pública de GeoSEDA en <https://geoseda.com>: un HTML estático publicado con GitHub Pages.

Este repositorio es público. No van aquí datos de clientes, geodatabases ni nada confidencial.

## Archivos

| Archivo | Qué es |
|---|---|
| `index.html` | La landing completa: estilos y animaciones (curvas de nivel en canvas) dentro del mismo archivo. |
| `favicon.svg`, `favicon-32.png`, `apple-touch-icon.png` | Íconos de la pestaña y del iPhone. |
| `og.jpg` | Imagen de 1200×630 que se ve al compartir el enlace (WhatsApp, LinkedIn). |
| `404.html` | Lo que muestra GitHub Pages en una ruta que no existe (también `/login` y `/register` mientras la plataforma no está en producción). |
| `CNAME` | Dominio propio para GitHub Pages (`geoseda.com`). |

## DNS (GoDaddy)

| Tipo | Nombre | Valor |
|---|---|---|
| A | @ | 185.199.108.153 |
| A | @ | 185.199.109.153 |
| A | @ | 185.199.110.153 |
| A | @ | 185.199.111.153 |
| CNAME | www | dacolora.github.io |

Todo GeoSEDA vive en `geoseda.com`, sin subdominios. La plataforma (validación y creación de GDB, en el repo
privado `seda-gdb`, carpeta `plataforma/`) ya trae esta misma landing como su página de inicio (`frontend/src/inicio/`):
cuando salga a producción, `geoseda.com` apuntará a su servidor y este repositorio y GitHub Pages dejan de servirla.
Mientras tanto los botones «Entrar» y «Crear cuenta» llevan a `/login` y `/register`, que aquí no existen: GitHub
Pages muestra `404.html`, que avisa que la plataforma abre muy pronto. Un cambio a la landing se hace en los dos
lugares hasta entonces.

## Probar en local

```bash
python3 -m http.server 4610
```
