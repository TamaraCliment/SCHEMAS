En los DTD se diferencia entre los elementos terminales y los no terminales ¿en este caso también? Si, este lenguaje permite trabajar tanto con datos simples como con estructuras de datos complejos, es decir compuestos por el anidamiento de otros datos simples o compuestos.

**Tipos de datos simples:** Estos datos se suelen definir para hacer una restricción sobre un tipo de datos XDS ya definido y establece el rango de valores que puede tomar.

**_Ejercicio resuelto:_** Creación de un elemento simple de nombre edad que representa la edad de un alumno de la ESO, por tanto su rango está entre los 12 y los 18 años.

!!! example "Ejemplo de uso"
```xsd
<xs:simpleType name="edad">
    <xs:restriction base="xs:positiveInteger">
    <xs:maxExclusive value="10"/>
    </xs:restriction>
</xs:simpleType>
```

**_Ejercicio resuelto:_** Creación de una lista con los días de la semana en letras.

![](../img/EjemploLista.JPG)


!!! example "Ejemplo de uso"
```xsd
<?xml version="1.0" encoding="UTF-8"?>
<xs:schema xmlns:xs="http://www.w3.org/2001/XMLSchema" elementFormDefault="qualified">

<!--Elemento raíz "catalogo"-->
  <xs:element name="catalogo">
    <xs:complexType>
      <xs:sequence>
      <!--Elemento raíz "dias" que utiliza el tipo "DiasType"-->
        <xs:element name="dias" type="DiasType" />
      </xs:sequence>
    </xs:complexType>
  </xs:element>

  <!--Definición del tipo  "DiasType" como una lista de Strings-->
  <xs:simpleType name="DiasType">
    <xs:list itemType ="xs:string"/>
  </xs:simpleType>
</xs:schema>
```

- **Tipos de datos compuestos:** El elemento **xsd:complexType** permite definir estructuras complejas de datos. Su contenido son las declaraciones de elementos y atributos, o referencias a elementos y atributos declarados de forma global. Para determinar el orden en que estos elementos aparecen en el documento XML se utiliza el elemento .
  **_Ejercicio resuelto:_** Creación de un elemento compuesto de nombre alumno, formado por los elementos nombre, apellidos, web personal.

!!! example "Ejemplo de uso"
```xsd
<xs:complexType  name="alumno">
      <xs:sequence>
        <xs:element name="nombre" type="xs:string" minOccurs="1" maxOccurs="unbounded"/>
        <xs:element name="apellidos" type="xs:string" minOccurs="1" maxOccurs="unbounded"/>
        <xs:element name="web" type="xs:string" minOccurs="0" maxOccurs="unbounded"/>
            <xs:complexType>
                <xs:attribute name="href" type="xs:string"/>
            </xs:complexType>
      </xs:sequence>
    </xs:complexType>
```
