Una vez que hemos visto como crear un esquema vamos a ver el modo de incorporar cierta documentación (quién es el autor, limitaciones de derechos de autor, utilidad del esquema, etc.) al mismo.

- Podemos pensar que un método para añadir esta información es utilizar comentarios. El problema es que los analizadores no garantizan que los comentarios no se modifiquen al procesar los documentos y por tanto, que los datos añadidos no se pierdan en algún proceso de transformación del documento.
- En lugar de usar los comentarios, XML Schema tiene definido un elemento xs:annotation que permite guardar información adicional. Este elemento a su vez puede contener una combinación de otros dos que son:
- xs:documentation, además de contener elementos de esquema puede contener elementos XML bien estructurados.
  También permite determinar el idioma del documento mediante el atributo xml:lang.
  - xs:appinfo, se diferencia muy poco del elemento anterior, aunque lo que se pretendió inicialmente era que xs:documentation fuese legible para los usuarios y que xs:appinfo guardase información para los programas
    de software.

También es usado para generar una ayuda contextual para cada elemento declarado en el esquema.

**_Ejercicio resuelto:_** Ejemplo de documentación de un esquema.

!!! example "Ejemplo de uso"
```xsd
<?xml version="1.0" encoding="UTF-8"?>
<xs:schema xmlns:xs="http://www.w3.org/2001/XMLSchema" >
  <xs:annotation>
    <xs:documentation xml:lang="es-es">
       Materiales para formación e-Learning
        <modulo>Lenguaje de marcas y ssitemas de gestión de información</modulo>
        <fecha_creacion>2011</fecha_creacion>
        <autos>Nuky La Bruji</autos>
    </xs:documentation>
</xs:annotation>
<xs:element name="lmsgi" type="xs:string">
  <xs:annotation>
    <xs:appinfo>
        <text_de_ayuda>Se debe de introducir el nombre completo del tema</text_de_ayuda>
    </xs:appinfo>
  </xs:annotation>
  </xs:element>
</xs:schema>
```