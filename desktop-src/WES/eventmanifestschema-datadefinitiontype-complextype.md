---
title: Tipo complexo datadefinitiontype
description: Define um item de dados que você deseja incluir com o evento. | Tipo complexo datadefinitiontype
ms.assetid: f4234e54-a5a8-48e4-941f-05107dcd3f88
keywords:
- Log de eventos de tipo complexo datadefinitiontype
topic_type:
- apiref
api_name:
- DataDefinitionType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 19584c28a7bdf7ae01b87d1f414b9464b7b4271d
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "105781482"
---
# <a name="datadefinitiontype-complex-type"></a>Tipo complexo datadefinitiontype

Define um item de dados que você deseja incluir com o evento.

``` syntax
<xs:complexType name="DataDefinitionType"
    mixed="true"
>
    <xs:simpleContent>
        <xs:extension
            base="string"
        >
            <xs:attribute name="name"
                type="string"
                use="required"
             />
            <xs:attribute name="inType"
                type="QName"
                use="required"
             />
            <xs:attribute name="outType"
                type="QName"
                use="optional"
             />
            <xs:attribute name="map"
                type="string"
                use="optional"
             />
            <xs:attribute name="length"
                type="LengthType"
                use="optional"
             />
            <xs:attribute name="count"
                type="CountType"
                use="optional"
             />
            <xs:anyAttribute
                processContents="lax"
                namespace="##other"
             />
        </xs:extension>
    </xs:simpleContent>
</xs:complexType>
```

## <a name="attributes"></a>Atributos



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Nome</th>
<th>Tipo</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>count</td>
<td><a href="eventmanifestschema-counttype-simpletype.md"><strong>Número de contagem</strong></a></td>
<td>O número de elementos na matriz se o item de dados for uma matriz. Você pode especificar a contagem real ou o nome de outro item de dados que contém a contagem. <br/></td>
</tr>
<tr class="even">
<td>intipo</td>
<td><strong>QName</strong></td>
<td>O tipo de dados para este item de dados. Para obter uma lista de tipos de dados de entrada predefinidos, consulte o tipo complexo <a href="eventmanifestschema-inputtype-complextype.md"><strong>InputType</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td>comprimento</td>
<td><a href="eventmanifestschema-lengthtype-simpletype.md"><strong>Comprimentotype</strong></a></td>
<td>O comprimento de um item de dados de comprimento variável, como um blob binário. Para dados binários, especifique o comprimento em bytes e para dados de cadeia de caracteres, especifique o comprimento em caracteres. Você pode especificar o comprimento real ou o nome de outro item de dados que contém o comprimento.<br/> Se você usar o atributo Length para especificar uma cadeia de caracteres de comprimento fixo, será necessário preencher a cadeia de caracteres para seu comprimento fixo, permitindo o caractere de terminador nulo no final (por exemplo, se o comprimento for 5, a cadeia de caracteres &quot; ABC &quot; deverá ser preenchida como &quot; ABC &quot; . O comprimento da cadeia de caracteres deve incluir o caractere de terminador nulo.<br/></td>
</tr>
<tr class="even">
<td>mapa</td>
<td>string</td>
<td>O nome do mapa de nome/valor a ser usado para mapear valores inteiros para cadeias de caracteres. O tipo de dados do item de dados deve ser de um dos seguintes tipos:<br/>
<ul>
<li>win:UInt8</li>
<li>win:UInt16</li>
<li>win:UInt32</li>
</ul></td>
</tr>
<tr class="odd">
<td>name</td>
<td>string</td>
<td>O nome do item de dados. Você pode usar o nome para fazer referência a este item de dados no fragmento XML se especificar uma seção <a href="eventmanifestschema-userdata-templateitemtype-element.md"><strong>UserData</strong></a> em seu modelo. Você também pode referenciar esse nome em um atributo Length ou Count de outro item de dados se esse item de dados contiver seu comprimento ou valor de contagem.<br/> <strong>Windows Vista:</strong> Esse atributo é opcional.<br/></td>
</tr>
<tr class="even">
<td>outtipo</td>
<td><strong>QName</strong></td>
<td>O tipo de dados a ser usado ao renderizar este item de dados. Para obter uma lista de tipos de dados de saída predefinidos, consulte o tipo de <a href="eventmanifestschema-outputtype-complextype.md"><strong>saída</strong></a> complexo.<br/> <strong>Windows Vista:</strong> O tipo de saída é ignorado e o serviço determina o tipo com base no tipo de entrada.<br/></td>
</tr>
</tbody>
</table>



## <a name="remarks"></a>Comentários

Para tipos de entrada de comprimento variável, como blobs binários, você deve usar o atributo Length para especificar explicitamente o tamanho dos dados. Para cadeias de caracteres, especifique o atributo Length somente se as cadeias de caracteres tiverem um comprimento fixo.

## <a name="examples"></a>Exemplos

Veja a seguir alguns exemplos das definições de item de dados.


```XML
<!-- The data item is an 8-bit integer -->
<data name="binaryChar" inType="win:UInt8">
 
<!-- The data item is a single ANSI character -->
<data name="ansiChar" inType="win:UInt8" outtype="xs:string">
 
<!-- The data item is a single Unicode character -->
<data name="unicodeChar" inType="win:UInt16" outtype="xs:string">
 
<!-- The data item is an IP address that is rendered as a dot separated list of interger values -->
<data name="ipAddress" inType="win:UInt32" outtype="win:IPv4">
 
<!-- The data item is a Boolean value -->
<data name="success" inType="win:boolean">
 
<!-- The data item is a null-terminated ANSI string -->
<data name="string" inType="win:AnsiString"> 

<!-- The data item is a fixed length ANSI string -->
<data name="string" inType="win:AnsiString" length="42"> 
 
<!-- The data item is a fixed length array of null-terminated ANSI strings -->
<data name="strings" inType="win:AnsiString" count="20">
 
<!-- The data item is a fixed length array of fixed length ANSI strings -->
<data name="strings" inType="win:AnsiString" length="42" count="20">
 
<!-- The data item is a variable length array of same sized ANSI strings -->
<data name="stringLength" inType="win:UInt16">
<data name="arrayCount" inType="win:Uint16">
<data name="strings" inType="win:AnsiString" length="stringLength" count="arrayCount"> 
 
<!-- For binary data, you must specify the size.
<!-- The data item is a fixed length array of fixed length binary blobs -->
<data name="blobs" inType="win:Binary" length="42" count="20">

<!-- The data item is a fixed length binary blob -->
<data name="blob" inType="win:Binary" length="42">

<!-- The following are illegal binary data definitions -->
<!-- This definition is illegal because no length is specified -->
<data name="blob" inType="win:Binary"> 
 
<!-- This definition is illegal because you cannot determine the length of each binary blob -->
<data name="blob" inType="win:Binary" count="20"> 
 
<!-- The data item is a variable length array of structures. Each structure -->
<!-- contains an array of same sized ANSI strings --> 
<data name="arrayStructCount" inType="win:UInt16">
<struct name="countedStrings" count="arrayStructCount">
      <data name="stringLength" inType="win:UInt16">
      <data name="string" inType="win:AnsiString" length="stringLength">
</struct>
 
<!-- The data item is a time stamp that is rendered in 100ns units -->
<data name="timestamp" inType="win:UInt32" outType="win:ETWTIME">

<!-- The data item is a fixed length array of integers --> 
<data name="integers" inType="win:UInt32" count="20">

<!-- The data item is a variable length array of integers -->
<data name="arrayCount" inType="win:UInt16"> 
<data name="integers" inType="win:UInt32" count="arrayCount"> 

<!-- The following is illegal because you cannot assign a length value to a data type of a known size -->
<data name="integer" inType="win:UInt32" length="42">
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/> |



 

 





