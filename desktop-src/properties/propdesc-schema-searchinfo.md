---
description: Especifica como configurar o mecanismo de pesquisa do Windows com relação a uma determinada definição de propriedade.
ms.assetid: 1cb0b630-323c-41cf-8aaf-db3028b2e369
title: searchInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eee94585aaa66a761e527ac6ada1c33b0d23966d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105783320"
---
# <a name="searchinfo"></a>searchInfo

Especifica como configurar o mecanismo de pesquisa do Windows com relação a uma determinada definição de propriedade. Se nenhum elemento [searchInfo]() for fornecido, a propriedade não será incluída no mecanismo de pesquisa do Windows. Esse elemento foi alterado para o Windows 7.

## <a name="syntax-for-windows-7"></a>Sintaxe do Windows 7


```
<!-- searchInfo for Windows 7-->
<xs:element name="searchInfo">
    <xs:complexType>
        <xs:attribute name="inInvertedIndex"    type="xs:boolean" default="false"/>
        <xs:attribute name="isColumn"           type="xs:boolean" default="false"/>
        <xs:attribute name="isColumnSparse"     type="xs:boolean" default="true">
            <xs:annotation>
                <xs:documentation>
                    isColumnSparse: Default is true. If the property is multi-valued, this is always true.
                </xs:documentation>
            </xs:annotation>
        </xs:attribute>
        
        <xs:attribute name="columnIndexType" default="OnDemand">
            <xs:simpleType>
                <xs:restriction base="xs:string">
                    <xs:enumeration value="NotIndexed"/>
                    <xs:enumeration value="OnDisk"/>
                    <xs:enumeration value="OnDiskAll"/>
                    <xs:enumeration value="OnDiskVector"/>
                    <xs:enumeration value="OnDemand"/>
                </xs:restriction>
            </xs:simpleType>
        </xs:attribute>
        <xs:attribute name="maxSize" type="xs:nonNegativeInteger" default="512"/>
        <xs:attribute name="mnemonics" type="xs:string"/>                            
    </xs:complexType>
</xs:element>
```



## <a name="syntax-for-windows-vista"></a>Sintaxe do Windows Vista


```
<!-- searchInfo for Windows Vista-->
<xs:element name="searchInfo">
    <xs:complexType>
        <xs:attribute name="inInvertedIndex"    type="xs:boolean" default="false"/>
        <xs:attribute name="isColumn"           type="xs:boolean" default="false"/>
        <xs:attribute name="isColumnSparse"     type="xs:boolean" default="true">
            <xs:annotation>
                <xs:documentation>
                    isColumnSparse: Default is true. If the property is multi-valued, this is always true.
                </xs:documentation>
            </xs:annotation>
        </xs:attribute>
        
        <xs:attribute name="columnIndexType" default="OnDemand">
            <xs:simpleType>
                <xs:restriction base="xs:string">
                    <xs:enumeration value="NotIndexed"/>
                    <xs:enumeration value="OnDisk"/>
                </xs:restriction>
            </xs:simpleType>
        </xs:attribute>
        <xs:attribute name="maxSize" type="xs:nonNegativeInteger" default="128"/>
    </xs:complexType>
</xs:element>
```



## <a name="element-information"></a>Informações do elemento



| Elemento pai                                                   | Elementos filho |
|------------------------------------------------------------------|----------------|
| [propertyDescription](./propdesc-schema-propertydescription.md) | Nenhum           |



 

## <a name="attributes"></a>Atributos



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Atributo</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>inInvertedIndex</td>
<td>Público. Opcional. Indica se o valor da propriedade deve ser armazenado no índice invertido. Isso permite que os usuários finais executem consultas de texto completo sobre os valores dessa propriedade. O padrão é &quot;false&quot;.</td>
</tr>
<tr class="even">
<td>IsColumn</td>
<td>Público. Opcional. Indica se a propriedade também deve ser armazenada no banco de dados do Windows Search como uma coluna, de modo que os ISVs (fornecedores independentes de software) possam criar consultas baseadas em predicado (por exemplo, &quot; Selecione *, em que &quot; System. title &quot; = ' qqq ' &quot; ). Se o criador do esquema quiser permitir que os usuários finais (ou desenvolvedores) criem consultas baseadas em predicado nas propriedades, isso precisará ser definido como &quot; true &quot; . O padrão é &quot;false&quot;.</td>
</tr>
<tr class="odd">
<td>isColumnSparse</td>
<td>Público. Opcional. O padrão é &quot;true&quot;. Se a propriedade tiver valores múltiplos, esse atributo será sempre &quot; verdadeiro &quot; .</td>
</tr>
<tr class="even">
<td>columnIndexType</td>
<td>Público. Opcional. Para otimizar a classificação e o agrupamento, o mecanismo de pesquisa do Windows pode criar índices secundários para propriedades que têm IsColumn = &quot; true &quot; . Esse atributo só é útil quando inInvertedIndex é &quot; verdadeiro &quot; no Windows Vista ou quando IsColumn é &quot; true &quot; no Windows 7. Se a propriedade tende a ser classificada frequentemente pelos usuários, esse atributo deverá ser especificado. O valor padrão no Windows Vista é não &quot; indexado &quot; . O valor padrão no Windows 7 é &quot; OnDemand &quot; . Os valores a seguir são válidos.
<ul>
<li>Não <strong>indexado</strong>: nunca compile um índice de valor.</li>
<li>Em <strong>disco</strong>: Crie um índice de valor por padrão para essa propriedade.</li>
<li><strong>OnDiskAll</strong> (somente Windows 7 e posterior): Crie um índice de valor por padrão para essa propriedade e, se for uma propriedade de vetor, também um índice de valor para todos os valores de vetor concatenados.</li>
<li><strong>OnDiskVector</strong> (somente Windows 7 e posterior): Crie um índice de valor por padrão para os valores de vetor concatenados.</li>
<li><strong>OnDemand</strong> (somente Windows 7 e posterior): somente compilar índices de valor por demanda, ou seja, somente primeira vez que eles são usados para uma consulta.</li>
</ul></td>
</tr>
<tr class="odd">
<td>maxSize</td>
<td>Público. Opcional. O tamanho máximo, em bytes, permitido para uma determinada propriedade que é armazenada no banco de dados do Windows Search. O padrão é:
<ul>
<li><strong>Windows Vista</strong>: 128 bytes</li>
<li><strong>Windows 7 e posterior</strong>: 512 bytes</li>
</ul>
Observe que esse tamanho máximo é medido em bytes, não em caracteres. O número máximo de caracteres depende de sua codificação.<br/></td>
</tr>
<tr class="even">
<td>mnemônico</td>
<td><strong>Windows 7 e posterior.</strong> Público. Opcional. Uma lista de valores mnemônicos que podem ser usados para fazer referência à propriedade em consultas de pesquisa. A lista é delimitada com o caractere ' | '.</td>
</tr>
</tbody>
</table>



 

 

 
