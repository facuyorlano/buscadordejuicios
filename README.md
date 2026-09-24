# Buscador de juicios — piloto La Plata

Objetivo: buscar un apellido en los organismos de La Plata disponibles en la MEV y reunir carátula, número, organismo y enlace.

## Resultado real del piloto — 24/09/2026

- Ingreso autenticado a la MEV: exitoso.
- Selección del Departamento Judicial La Plata: exitosa.
- Inventario de la sección general: **45 organismos** observados en el selector. Sus nombres e identificadores originales están en [data/la-plata-organismos.json](data/la-plata-organismos.json).
- Formulario observado: búsqueda por carátula, número de expediente o receptoría; selector de un único organismo; estado activos, archivados o ambos (ambos seleccionado).
- Primera prueba: búsqueda por carátula en Juzgado Civil y Comercial 1, incluyendo activos y archivados.
- Respuesta: **“Validando acceso ... El sistema está verificando si está siendo navegado por un ser humano. Si esto demora vuelva a cargar la página”**.
- Se recargó una sola vez siguiendo el aviso, con idéntico resultado. Se detuvo la prueba sin eludir la verificación.

**Balance: 1 consulta intentada y bloqueada; 0 consultas completadas; 44 organismos generales sin probar. No se obtuvieron resultados ni se verificó paginación. Familia, Penal y Justicia de Paz no fueron relevados. No hay un buscador funcional ni cobertura completa comprobada.**

## Alcance del inventario

El selector observado incluye cámaras, juzgados civiles y contenciosos, tribunales laborales, el Juzgado Notarial y la Secretaría de Apremios. Se preserva la lista real, incluidos saltos de numeración; no equivale a todos los organismos de la provincia ni a todos los fueros de La Plata.

## Próximas verificaciones necesarias

1. Resolver la verificación humana mediante el flujo admitido por el sitio antes de continuar las consultas.
2. Contrastar resultados y paginación de una consulta real con la MEV.
3. Recorrer secuencialmente los organismos, con pausas y cancelación, deteniéndose ante bloqueo, límite o sesión vencida.
4. Relevar por separado Familia, Penal y Justicia de Paz y sus restricciones de acceso.
5. Medir duración por organismo, páginas consultadas y cobertura efectiva; no estimar tiempos como si estuvieran medidos.

## Requisitos del futuro buscador

- Estados por organismo: pendiente, consultando, completo con coincidencias, completo sin coincidencias, acceso restringido, bloqueado o error.
- Un error o una consulta pendiente nunca se presenta como cero coincidencias.
- La búsqueda por carátula identifica coincidencias textuales, no identidad de personas ni todas las partes de un expediente.
- La cobertura se limita a lo publicado y accesible para el usuario. La página oficial informa que Familia y Penal requieren autorización, al igual que algunos expedientes de otros fueros.
- No guardar en Git contraseñas, cookies, sesiones ni resultados judiciales con datos personales.
- La integración definitiva depende de validar el flujo permitido. No se presupone API pública ni se eluden controles del sitio.

Fuente: interfaz autenticada de https://mev.scba.gov.ar/ observada durante el piloto. Este repositorio conserva el relevamiento y el estado de la prueba; todavía no contiene una aplicación operativa.
