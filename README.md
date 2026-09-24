# Buscador de juicios — piloto La Plata

Objetivo: buscar un apellido en los organismos del Departamento Judicial La Plata disponibles en la MEV y reunir coincidencias con carátula, número, organismo y enlace.

## Estado real

Relevamiento iniciado el 24/09/2026. Repositorio inicialmente vacío. Se comprobó que https://mev.scba.gov.ar/loguin.asp presenta ingreso con usuario, contraseña y departamento de creación. No hay todavía una sesión autenticada para el piloto. **No se ejecutaron búsquedas ni se verificó el listado de organismos. No hay un buscador funcional aún.**

## Prueba de integración pendiente de autenticación

1. Relevar el listado real de organismos de La Plata ofrecido por la MEV, conservando sus identificadores y nombres; no inferir cobertura a partir de numeraciones.
2. Verificar formulario y semántica de búsqueda por carátula/apellido en un organismo.
3. Ejecutar una consulta de control y comprobar paginación y resultados con el sitio.
4. Repetir secuencialmente en todos los organismos disponibles de La Plata, con pausas, cancelación y detención ante bloqueo o vencimiento de sesión.
5. Registrar por organismo: pendiente, consultando, completado con coincidencias, completado sin coincidencias, acceso restringido o error. Un error nunca cuenta como cero resultados.
6. Medir tiempo total, tiempo por organismo, páginas revisadas y cobertura efectiva.

La búsqueda por apellido identifica coincidencias en el campo consultado; no prueba identidad ni asegura localizar a todas las partes de un expediente. La cobertura se limita a lo publicado y accesible para el usuario. La página oficial informa que Familia y Penal requieren autorización, al igual que determinados expedientes de otros fueros.

## Seguridad y datos

No incorporar al repositorio contraseñas, cookies, sesiones, expedientes ni resultados con datos personales. La autenticación se realiza en la MEV. El mecanismo definitivo de integración se decidirá después de observar y validar el flujo autenticado; no se presupone una API pública ni autorización para eludir controles.

## Criterio para considerar exitoso el piloto

Inventario de organismos observado en una sesión real, recorrido documentado, resultados contrastados con la MEV y todos los errores/restricciones explícitos. Hasta completar esas comprobaciones no se promete cobertura total ni tiempos de búsqueda.
