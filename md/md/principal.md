# Lenguaje de Marcas (LMSGI): Schemas

- Los DTD permiten diseñar un vocabulario para ficheros XML, pero, ¿qué sucede cuando los valores de los elementos y atributos de esos ficheros han de corresponder a datos de un tipo determinado, o cumplir determinadas restricciones que no pueden reflejarse en los DTD? Para ello se definen XML Schemas.
- ¿También se definen en ficheros planos? Si, ya que son documentos XML, pero en este caso la extensión de los archivos es xsd, motivo por el cual también se les denomina documentos XSD.
- Los elementos XML que se utilizan para generar un esquema han de pertenecer al espacio de nombre XML Schema, que es: http://www.w3.org/2001/XMLSchema.
- El ejemplar de estos ficheros es xs:schema, contiene declaraciones para todos los elementos y atributos que puedan aparecer en un documento XML asociado válido. Los elementos hijos inmediatos de este ejemplar son xs:element que nos permiten crear globalmente un elemento. Esto significa que el elemento creado puede ser el ejemplar del documento XML asociado.
