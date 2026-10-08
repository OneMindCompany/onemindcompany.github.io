# onemindcompany.github.io

Sitio **raíz** de GitHub Pages de la organización OneMindCompany: sirve
`https://onemindcompany.github.io/`. Hoy su único contenido es el archivo `app-ads.txt` que pide
AdMob para verificar que las apps de One Mind Company son de la cuenta de editor
`pub-4728591837862628`.

## Por qué existe

AdMob busca `app-ads.txt` **solo en la raíz del dominio** del sitio web del desarrollador que declara
la ficha de cada tienda. La ficha de Suscripciones declara
`https://onemindcompany.github.io/suscripcion-politicas/`, así que AdMob lo busca en
`https://onemindcompany.github.io/app-ads.txt`. Los sitios de proyecto (como
`suscripcion-politicas`) se sirven en una subcarpeta y no pueden poner archivos en la raíz; la raíz
solo la sirve un repositorio con este nombre exacto.

Las páginas de proyecto (`/suscripcion-politicas/`, …) siguen funcionando igual: este repo no las
toca.

## Excepciones al estándar de repositorios

| Regla | Excepción | Motivo |
|---|---|---|
| Nombre `{sol}-{pieza}` | `onemindcompany.github.io` | GitHub exige ese nombre para el sitio raíz de la organización |
| Repo privado | Público | GitHub Pages en el plan de la organización solo publica repos públicos (como `suscripcion-politicas`) |

El resto del estándar se cumple: ramas `main`, `qa` y `develop` protegidas, y todo cambio por PR.
GitHub Pages publica desde `main`, raíz.

## Ramas

| Rama | Rol | Protegida |
|------|-----|-----------|
| `main` | Producción: lo que sirve GitHub Pages | ✅ |
| `qa` | Validación | ✅ |
| `develop` | Integración del trabajo en curso | ✅ |
| `feature/*` | Trabajo puntual, se integra a `develop` vía PR | ❌ |
