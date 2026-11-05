# Dashboard TRM · Peso colombiano / Dólar

Dashboard de la **Tasa de Cambio Representativa del Mercado (TRM)** de Colombia. Consulta en vivo los datos abiertos de la Superintendencia Financiera publicados en datos.gov.co.

**Ver en línea:** https://asmecgreen.github.io/Prueba_TRM/

## Cómo usarlo

Es un solo archivo, `index.html`, con HTML, CSS y JavaScript sin dependencias externas ni proceso de compilación.

- **En línea:** abre el enlace de GitHub Pages.
- **En local:** descarga `index.html` y ábrelo con doble clic en el navegador.

Los datos se guardan en el navegador (`localStorage`), así que la página abre al instante. El botón **Actualizar** descarga solo los registros nuevos.

## Funciones

**Indicadores**
- TRM vigente hoy, con su rango de vigencia. Una misma TRM puede cubrir fines de semana y festivos.
- Variación frente a la TRM anterior, en COP y en %.
- Próxima TRM, si ya fue publicada.
- Rango de 52 semanas: mínimo y máximo, y en qué punto de ese rango está la TRM actual.
- Fecha y hora de la última actualización, en hora de Colombia.

**Histórico**
- Gráfico escalonado con rangos de 7D, 1M, 3M, 6M, año en curso, 1A, 5A y Todo.
- Medias móviles de 20 y 200 registros que se pueden activar o desactivar.
- Volatilidad móvil de 30 registros, anualizada.

**Herramientas**
- Consultar la TRM de cualquier fecha. Se busca con `vigenciadesde <= fecha <= vigenciahasta`.
- Conversor USD ↔ COP con la TRM de la fecha consultada.
- Tabla del rango seleccionado, con orden, paginación y exportación a CSV. El CSV usa `;` y coma decimal, compatible con Excel en español.

**Análisis**
- Comparar hasta 4 años sobre un eje de enero a diciembre, en valor COP o como índice (1 de enero = 100).
- Mapa de calor de la variación diaria por año.

## Fuente de los datos

- **Conjunto:** [Tasa de Cambio Representativa del Mercado - TRM](https://www.datos.gov.co/Econom-a-y-Finanzas/Tasa-de-Cambio-Representativa-del-Mercado-TRM/32sa-8pi3) (`32sa-8pi3`)
- **Publica:** Superintendencia Financiera de Colombia, vía datos.gov.co
- **API:** `https://www.datos.gov.co/resource/32sa-8pi3.json`
- **Licencia de los datos:** [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/deed.es)

## Licencia

El código se distribuye bajo la licencia MIT (ver [LICENSE](LICENSE)). Los datos conservan su propia licencia, CC BY-SA 4.0.
