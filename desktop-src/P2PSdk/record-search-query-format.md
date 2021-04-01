---
description: Uma chamada para a função PeerGroupSearchRecords requer um parâmetro de cadeia de caracteres de consulta XML que é usado para determinar os critérios básicos de uma pesquisa.
ms.assetid: 2c5ab425-6959-418a-8d9a-c8155257fc7e
title: Gravar formato de consulta de pesquisa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02b475c8a449e3bcd360df5757fef508b1a744d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829333"
---
# <a name="record-search-query-format"></a>Gravar formato de consulta de pesquisa

Uma chamada para a função [**PeerGroupSearchRecords**](/windows/desktop/api/P2P/nf-p2p-peergroupsearchrecords) requer um parâmetro de cadeia de caracteres de consulta XML que é usado para determinar os critérios básicos de uma pesquisa. Use o esquema a seguir para formular uma cadeia de caracteres XML:

``` syntax
<?xml version="1.0" encoding="utf-8" ?>
<xs:schema xmlns:xs="https://www.w3.org/2001/XMLSchema">

  <xs:simpleType name="alphanumType">
     <xs:restriction base="xs:string">
        <xs:pattern value="\c+"/>
     </xs:restriction>
  </xs:simpleType>

  <xs:complexType name="operatorType">
      <xs:choice maxOccurs="unbounded">
         <xs:element ref="and" />
         <xs:element ref="or" />
         <xs:element ref="clause" />
      </xs:choice>
  </xs:complexType>

  <xs:element name="and" type="operatorType"/>

  <xs:element name="or" type="operatorType"/>

  <xs:element name="clause">
      <xs:complexType>
          <xs:simpleContent>
              <xs:extension base="xs:string">
        <xs:attribute name="attrib" type="alphanumType" />
        <xs:attribute name="type">
                  <xs:simpleType>
                    <xs:restriction base="xs:string">
                      <xs:enumeration value="string"/>
                      <xs:enumeration value="date"/>
                      <xs:enumeration value="int"/>
                    </xs:restriction>
                  </xs:simpleType>
                </xs:attribute>
        <xs:attribute name="compare" default="equal">
                  <xs:simpleType>
                    <xs:restriction base="xs:string">
                      <xs:enumeration value="equal"/>
                      <xs:enumeration value="greater"/>
                      <xs:enumeration value="less"/>
                      <xs:enumeration value="notequal"/>
                      <xs:enumeration value="greaterorequal"/>
                      <xs:enumeration value="lessorequal"/>
                    </xs:restriction>
                  </xs:simpleType>
                </xs:attribute>
              </xs:extension>
          </xs:simpleContent>
      </xs:complexType>
  </xs:element>

  <xs:element name="peersearch">
      <xs:complexType>
          <xs:choice>
              <xs:element ref="clause" />
              <xs:element ref="and" />
              <xs:element ref="or" />
          </xs:choice>
      </xs:complexType>
  </xs:element>
</xs:schema> 
```

### <a name="elements-to-use-for-a-record-search"></a>Elementos a serem usados para uma pesquisa de registro

O elemento principal em uma pesquisa de registro é **peersearch**, que contém a Uniform Resource Identifier (URI) do esquema associado no atributo **xmlns** . Quando **peersearch** é usado como um elemento filho, você pode usar **e**, **cláusula** e **ou** como elementos filho.

-   **e** -o elemento **and** executa uma operação and lógica em uma ou mais cláusulas contidas entre as marcas de abertura e de fechamento. Outras marcas **e** e **ou** podem ser filhas, e os resultados recursivos de suas cláusulas filho são incluídos na operação.

    Por exemplo, se você quiser obter um registro que contém um nome igual a James Peters e uma última atualização maior que 2/28/2003, ou uma data de criação menor que 1/31/2003, use a seguinte cadeia de caracteres de consulta XML:

    ``` syntax
    <?xml version="1.0" encoding="utf-8" ?> 
    <peersearch xmlns:xs="https://www.w3.org/2001/XMLSchema">
       <and>
          <clause attrib="peercreatorid" type="string" compare="equal">James Peters</clause>
          <or>
             <clause attrib="peerlastmodificationtime" type="date" compare="greater">2003-01-31</clause>
             <clause attrib="peercreationtime" type="date" compare="less">2003-02-328</clause>
          </or>
       </and>
    </peersearch>
    ```

<!-- -->

-   **cláusula** -o elemento **Clause** especifica uma regra comparativa básica que compara o valor de um atributo de registro específico com o valor contido entre as marcas de abertura e de fechamento. Os atributos **Type** e **Compare** devem ser fornecidos **Compare** indica a operação de comparação a ser executada. Por exemplo, uma pesquisa simples que indica que todos os registros correspondentes deve ter um valor de **peercreatorid** igual a James Peters aparece na cadeia de caracteres de consulta XML como a seguir:

    ``` syntax
    <?xml version="1.0" encoding="utf-8" ?> 
    <peersearch xmlns:xs="https://www.w3.org/2001/XMLSchema">
       <clause attrib="peercreatorid" type="string" compare="equal">James Peters</clause>
    </peersearch>
    ```

    Os atributos de **tipo** comum incluem **int**, **String** e **Date**. O atributo **Date** pode ser um dos formatos de data padrão descritos em [https://www.w3.org/TR/NOTE-datetime](https://www.w3.org/TR/NOTE-datetime) .

    Os valores para o atributo de **comparação** são **igual**, não **igual**, **menor**, **maior**, **lessorequal** e **greaterorequal**.

<!-- -->

-   **or** -o elemento **or** executa uma operação OR lógica em uma ou mais cláusulas contidas entre as marcas de abertura e de fechamento. Outros elementos **ou** e **e** podem ser filhos, e os resultados recursivos das cláusulas filho são incluídos na operação. Por exemplo, se você quiser obter um registro que contenha um nome igual a James Peters ou uma última atualização que esteja entre 1/31/2003 e 2/28/2003, use a seguinte cadeia de caracteres de consulta XML:

``` syntax
<?xml version="1.0" encoding="utf-8" ?> 
<peersearch xmlns:xs="https://www.w3.org/2001/XMLSchema">
   <or>
      <clause attrib="peercreatorid" type="string" compare="equal">James Peters</clause>
      <and>
         <clause attrib="peerlastmodificationtime" type="date" compare="greater">2003-01-31</clause>
         <clause attrib="peerlastmodificationtime" type="date" compare="less">2003-02-28</clause>
      </and>
   </or>
</peersearch>
```

## <a name="more-information-about-a-record-search"></a>Mais informações sobre uma pesquisa de registro

O primeiro nível de nós após **peersearch** pode ter apenas um elemento. No entanto, os filhos subsequentes desse elemento podem ter muitos elementos no mesmo nível.

A seguinte consulta de pesquisa está incorreta:

``` syntax
<?xml version="1.0" encoding="utf-8" ?> 
<peersearch xmlns:xs="https://www.w3.org/2001/XMLSchema">
   <clause attrib="peercreatorid" type="string" compare="equal">James Peters</clause>
   <and>
      <clause attrib="peerlastmodificationtime" type="date" compare="greater">2003-01-31</clause>
      <clause attrib="peerlastmodificationtime" type="date" compare="less">2003-02-28</clause>
   </and>
</peersearch>
```

A consulta falha porque dois valores são retornados para a correspondência sem serem resolvidos em um valor verdadeiro/falso, o que significa que uma cláusula é uma consulta para o nome de um registro que é igual a James Peters, e a operação AND corresponde às duas cláusulas de componente. O resultado são dois valores lógicos true/false que são contraditórias.

Para obter todos os registros que contêm um nome igual a James Peters e uma última atualização entre 1/31/2003 e 2/28/2003, coloque a **cláusula** **e as marcas que** estão no mesmo nível entre abertura e fechamento **e** marcas. O exemplo a seguir mostra a consulta bem-sucedida:

``` syntax
<?xml version="1.0" encoding="utf-8" ?> 
<peersearch xmlns:xs="https://www.w3.org/2001/XMLSchema">
    <and>
      <clause attrib="peercreatorid" type="string" compare="equal">James Peters</clause>
      <and>
         <clause attrib="peerlastmodificationtime" type="date" compare="greater">2003-01-31</clause>
         <clause attrib="peerlastmodificationtime" type="date" compare="less">2003-02-28</clause>
      </and>
   </and>
</peersearch>
```

A lista a seguir identifica outras informações específicas que você deve saber para escrever uma consulta bem-sucedida:

-   As marcas **e** e **ou** não podem ser localizadas entre marcas de **cláusula** de abertura e fechamento porque, nessa configuração, elas são interpretadas como parte do valor para correspondência, o que resulta em um erro ou uma correspondência com falha.
-   Cada **par de marcas e/** **ou** abertura e fechamento deve incluir pelo menos um ou mais nós filho.
-   Um conjunto zero de elementos não é permitido neste esquema.

## <a name="record-attributes"></a>Atributos de registro

Usando o [esquema de atributo de registro](record-attribute-schema.md), um usuário pode criar atributos de registro que o atributo XML **attrib** em um elemento de cláusula especifica. Os atributos para um novo registro são adicionados definindo o membro **pszAttributes** do [**\_ registro de pares**](/windows/desktop/api/P2P/ns-p2p-peer_record) para uma cadeia de caracteres XML usando o formato especificado no esquema.

A infraestrutura de pares reserva os seguintes nomes de atributo:

-   **peerlastmodifiedby**
-   **peercreatorid**
-   **peerlastmodificationtime**
-   **peerrecordid**
-   **peerrecordtype**
-   **peercreationtime**
-   **peerlastmodificationtime**

## <a name="special-characters"></a>Caracteres Especiais

Determinados caracteres podem ser usados para expressar padrões de correspondência ou para escapar outros caracteres especiais. Esses caracteres são descritos na tabela a seguir. 

| Padrão de caractere | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                             |
|-------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \*                | O caractere curinga. Quando esse caractere é encontrado em um valor de cláusula, ele corresponde a 0-n caracteres de qualquer valor, incluindo caracteres de espaço em branco e não alfanuméricos. Por exemplo:<br/> "<clause attrib="peercreatorid" type="string" compare="equal">James P \* </clause>"<br/> Essa cláusula corresponde a todos os valores de **peercreatorid** com um nome "James" e um sobrenome começando com "P".<br/> |
| \\\*              | Um asterisco com escape. Essa sequência corresponde a um caractere de asterisco.                                                                                                                                                                                                                                                                                                                                                                       |
| ?                 | O caractere curinga de caractere único. Quando esse caractere é encontrado em um valor de cláusula, ele corresponde a qualquer caractere único, incluindo caracteres de espaço em branco e não alfanuméricos. Por exemplo:<br/> "<clause attrib="filename" type="string" compare="equal">data-0?. XML</clause>"<br/> Essa cláusula corresponde aos valores de **nome de arquivo** como "data-01.xml" e "data-0B.xml".<br/>                              |
| \\?               | Um ponto de interrogação de escape. Essa sequência corresponde a um caractere de ponto de interrogação.                                                                                                                                                                                                                                                                                                                                                              |
| \\\\              | Uma barra invertida de escape. Essa sequência corresponde a um caractere de barra invertida simples.                                                                                                                                                                                                                                                                                                                                                               |



 

Se a sequência de caracteres não for válida, a função [**PeerGroupSearchRecords**](/windows/desktop/api/P2P/nf-p2p-peergroupsearchrecords) retornará o erro **E \_ INVALIDARG**. Uma sequência inválida é qualquer sequência que contenha um \\ caractere "" (barra invertida) não seguido imediatamente por um \* caractere "" (asterisco), um "?" (ponto de interrogação) ou outro \\ caractere "" (barra invertida).

 

 




