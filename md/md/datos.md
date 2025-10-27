- Son los distintos valores que puede tomar el atributo type cuando se declara un elemento o un atributo y
  representan el tipo de dato que tendrá el elemento o atributo asociado a ese type en el documento XML.

Algunos de estos valores predefinidos son:

- **string**, se corresponde con una cadena de caracteres UNICODE.
- **boolean**, representa valores lógicos, es decir que solo pueden tomar dos valores, true o false.
- **integer**, número entero positivo o negativo.
- **positiveInteger**, número entero positivo.
- **negativeInteger**, número entero negativo.
- **decimal**, número decimal, por ejemplo, 8,97.
- **dateTime**, representa una fecha y hora absolutas.
- **duration**, representa una duración de tiempo expresado en años, meses, días, horas, minutos segundos. El formato utilizado es: PnYnMnDTnHnMnS. Por ejemplo para representar una duración de 2 años, 4 meses, 3 días, 5 horas, 6 minutos y 10 segundos habría que poner: P2Y4M3DT5H6M7S. Se pueden omitir los valores nulos, luego una duración de 2 años será P2Y. Para indicar una duración negativa se pone un signo – precediendo a la P.
- **time**, hora en el formato hh:mm:ss.
- **date**, fecha en formato CCYY–MM–DD.
- **gYearMonth**, representa un mes de un año determinado mediante el formato CCYY–MM.
- **gYear**, indica un año gregoriano, el formato usado es CCYY.
- **gMothDay**, representa un día de un mes mediante el formato –MM–DD.
- **gDay**, indica el ordinal del día del mes mediante el formato –DD, es decir el 4º día del mes será –04.
- **gMonth**, representa el mes mediante el formato –MM. Por ejemplo, febrero es –02.
- **anyURI**, representa una URI.
- **language**, representa los identificadores de lenguaje, sus valores están definidos en RFC 1766.
- **ID, IDREF, ENTITY, NOTATION, MTOKEN**.Representan lo mismo que en los DTD's
  En este enlace encontrarás los tipos de datos admitidos por el estándar. XML Schema Tipos de datos https://www.w3.org/TR/xmlschema-2/
