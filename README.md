# Cruce de Figuritas

Aplicación web de una sola página para cruzar dos listas de figuritas de un álbum y encontrar las que **coinciden en ambas**. Pensada para detectar repetidas en común entre dos personas y facilitar intercambios.

No necesita instalación ni dependencias: es un único archivo `index.html` que se abre en cualquier navegador (escritorio o móvil).

## Cómo funciona

1. Pegás cada colección en su cuadro (**Lista A** y **Lista B**).
2. Cada línea empieza con un **código del álbum** seguido de los números de figurita, separados por comas o espacios:

   ```
   ARG 5, 12, 18, 20
   BRA 3 7 9
   MEX 44, 50
   ```

3. Pulsás **Buscar coincidencias**. La app muestra solo las figuritas que aparecen en ambas listas, agrupadas por código, con el total y un botón para copiar el resultado.

### Reglas de cruce

- El emparejamiento es por **código + número**: una figurita cuenta como coincidencia solo si el mismo código tiene el mismo número en ambas listas.
- El mismo número bajo un código distinto **no** es coincidencia.
- No distingue mayúsculas de minúsculas (`arg` = `ARG`).
- Tras el código se **omite cualquier emoji, letra o símbolo** hasta llegar a los números. Son válidas líneas como `ARG 🇦🇷 5, 12`, `BRA (Brasil) 3, 7` o incluso pegado `ARG🇦🇷5,12`.
- Los códigos no reconocidos se ignoran y se avisan debajo del resultado (útil para detectar errores de tipeo).

### Variables especiales

Tres códigos se muestran y se copian con su emoji, aunque el cruce se hace por el código base:

| Código | Se muestra como |
|--------|-----------------|
| FWC1   | FWC1 🏆         |
| FWC2   | FWC2 🌎         |
| FWC3   | FWC3 📜         |

## Códigos válidos (51)

```
FWC1, FWC2, FWC3, MEX, RSA, KOR, CZE, CAN, BIH, QAT, SUI, BRA, MAR, HAI,
SCO, USA, PAR, AUS, TUR, GER, CUW, CIV, ECU, NED, JPN, SWE, TUN, BEL, EGY,
IRN, NZL, ESP, CPV, KSA, URU, FRA, SEN, IRQ, NOR, ARG, ALG, AUT, JOR, POR,
COD, UZB, COL, ENG, CRO, GHA, PAN
```

## Publicar en GitHub Pages

1. Subí estos archivos a un repositorio de GitHub.
2. En el repo, andá a **Settings → Pages**.
3. En *Source*, elegí la rama `main` y la carpeta `/ (root)`.
4. Guardá. En unos minutos tu app quedará disponible en
   `https://TU-USUARIO.github.io/NOMBRE-DEL-REPO/`.

Como el archivo se llama `index.html`, GitHub Pages lo sirve automáticamente.

## Tecnología

HTML, CSS y JavaScript puro (sin frameworks ni dependencias). Las tipografías se cargan desde Google Fonts.

## Licencia

MIT — ver [LICENSE](LICENSE).
