# Estudiantes migrantes en la matrícula de Medellín

Informe público de la **Secretaría de Educación de la Alcaldía de Medellín** sobre la población extranjera matriculada en el Distrito, vigencia 2026.

Presenta dónde está la población estudiantil extranjera por comuna y corregimiento, cuánta atiende en promedio cada institución educativa, cuáles son las instituciones con más estudiantes extranjeros y cómo se compone esa población por nacionalidad y modelo educativo.

---

## Contenido del repositorio

```
index.html                      Informe completo
assets/
  css/sistema-diseno.css        Tokens y componentes del sistema de diseño Educación Medellín
  fonts/                        Tipografía Metropolis
  img/                          Logos institucionales
  datos/datos-informe.js        Cifras agregadas que alimentan el informe
.nojekyll                       Publica los archivos tal cual en GitHub Pages
```

No requiere compilación, servidor ni dependencias externas. El informe funciona abriendo `index.html` directamente en el navegador.

## Publicación en GitHub Pages

1. Suba el contenido de esta carpeta a la rama `main` del repositorio.
2. En el repositorio, entre a **Settings → Pages**.
3. En **Build and deployment**, elija **Deploy from a branch**, rama `main` y carpeta `/ (root)`.
4. Guarde. El informe queda disponible en `https://<usuario>.github.io/<repositorio>/`.

## Actualización con un corte nuevo

Todas las cifras, los textos de lectura y las fechas del informe se generan desde `assets/datos/datos-informe.js`; `index.html` no contiene cifras escritas a mano y no se modifica.

El archivo lo genera el proceso interno del Observatorio (`exportar_informe_github.py`), que aplica el universo y el filtro de publicación —solo las cifras que el informe muestra y ninguna con menos de cinco estudiantes extranjeros— y se detiene si alguna cifra no cumple. No publique a mano el `datos.js` del proceso interno en lugar de este: es un archivo más amplio.

## Alcance de los datos

- **Universo.** Matrícula en establecimientos oficiales, grados 0 a 11 y 99. Ningún registro fuera de ese universo entra en las cifras.
- **Solo cifras agregadas.** La fuente es el Sistema Integrado de Matrícula (SIMAT) cruzado con el Directorio Único de Establecimientos. Los datos personales de origen no se reproducen.
- **Solo lo que el informe muestra.** El archivo de datos contiene únicamente las cifras visibles: las 21 divisiones territoriales, las 12 instituciones con más estudiantes extranjeros, las nacionalidades y los modelos educativos representados.
- **Sin grupos pequeños.** No se publica ninguna institución, sede, nacionalidad ni modelo con menos de cinco estudiantes extranjeros. Las sedes por debajo de ese umbral no se dibujan en el mapa.
- **Definiciones.** Se considera estudiante extranjero a quien registra un país de origen distinto de Colombia sobre matrícula activa. El promedio por I. E. en la comuna es el número de estudiantes extranjeros de una comuna o corregimiento dividido entre sus instituciones educativas; el promedio por I. E. en la ciudad divide el total de la ciudad entre todas las instituciones.

Los datos personales se tratan conforme a la Ley 1581 de 2012.

## Marca y tipografía

- Logos e identidad visual de la Alcaldía de Medellín conforme al *Manual de Identidad Visual, versión 20*. Su uso está sujeto a la validación y aprobación de la Secretaría de Comunicaciones.
- Geometría de comunas y corregimientos: Área Metropolitana del Valle de Aburrá, capa Límite_Comuna_Sector, EPSG:4326.
- Tipografía Metropolis, de Chris Simpson, distribuida bajo SIL Open Font License 1.1.
