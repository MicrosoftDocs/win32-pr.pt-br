---
description: especifica como configurar o Windows mecanismo de pesquisa com relação a uma determinada definição de propriedade.
ms.assetid: 1cb0b630-323c-41cf-8aaf-db3028b2e369
title: searchInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bbcfc901dfb4610210c4990c962b5251710e5653
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122465623"
---
# <a name="searchinfo"></a>searchInfo

especifica como configurar o Windows mecanismo de pesquisa com relação a uma determinada definição de propriedade. se nenhum elemento [searchInfo]() for fornecido, a propriedade não será incluída no mecanismo de pesquisa Windows. este elemento foi alterado para Windows 7.

## <a name="syntax-for-windows-7"></a>sintaxe para Windows 7


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



## <a name="syntax-for-windows-vista"></a>sintaxe para Windows Vista


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




| Atributo | Descrição | 
|-----------|-------------|
| inInvertedIndex | Público. Opcional. Indica se o valor da propriedade deve ser armazenado no índice invertido. Isso permite que os usuários finais executem consultas de texto completo sobre os valores dessa propriedade. O padrão é "falso". | 
| IsColumn | Público. Opcional. indica se a propriedade também deve ser armazenada na Windows banco de dados de pesquisa como uma coluna, de modo que os ISVs (fornecedores independentes de software) possam criar consultas baseadas em predicado (por exemplo, "Select * onde" System. Title "= ' qqq '"). Se o criador do esquema quiser permitir que os usuários finais (ou desenvolvedores) criem consultas baseadas em predicado nas propriedades, isso precisará ser definido como "true". O padrão é "falso". | 
| isColumnSparse | Público. Opcional. O padrão é "true". Se a propriedade tiver valores múltiplos, esse atributo será sempre "true". | 
| columnIndexType | Público. Opcional. para otimizar a classificação e o agrupamento, o mecanismo de pesquisa Windows pode criar índices secundários para propriedades que tenham iscolumn = "true". esse atributo só é útil quando inInvertedIndex é "true" no Windows Vista ou quando iscolumn é "true" no Windows 7. Se a propriedade tende a ser classificada frequentemente pelos usuários, esse atributo deverá ser especificado. o valor padrão no Windows Vista é "não indexado". o valor padrão no Windows 7 é "ondemand". Os valores a seguir são válidos.<ul><li>Não <strong>indexado</strong>: nunca compile um índice de valor.</li><li>Em <strong>disco</strong>: Crie um índice de valor por padrão para essa propriedade.</li><li><strong>OnDiskAll</strong> (somente Windows 7 e posteriores): crie um índice de valor por padrão para essa propriedade e, se for uma propriedade de vetor, também um índice de valor para todos os valores de vetor concatenados.</li><li><strong>OnDiskVector</strong> (somente Windows 7 e posteriores): crie um índice de valor por padrão para os valores de vetor concatenados.</li><li><strong>ondemand</strong> (somente Windows 7 e posteriores): somente compilar índices de valor por demanda, ou seja, somente primeira vez que eles são usados para uma consulta.</li></ul> | 
| maxSize | Público. Opcional. o tamanho máximo, em bytes, permitido para uma determinada propriedade que é armazenada no banco de dados de pesquisa Windows. O padrão é:<ul><li><strong>Windows Vista</strong>: 128 bytes</li><li><strong>Windows 7 e posterior</strong>: 512 bytes</li></ul>Observe que esse tamanho máximo é medido em bytes, não em caracteres. O número máximo de caracteres depende de sua codificação.<br /> | 
| mnemônico | <strong>Windows 7 e posterior.</strong> Público. Opcional. Uma lista de valores mnemônicos que podem ser usados para fazer referência à propriedade em consultas de pesquisa. A lista é delimitada com o '|espaço. | 




 

 

 
