---
description: Especifica como os rótulos da propriedade são exibidos.
ms.assetid: 9317aff9-abdd-46c2-aaff-62861925713b
title: labelInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d2d358270bfdf231f990feee54d90f6f39f16fa
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122475092"
---
# <a name="labelinfo"></a>labelInfo

Especifica como os rótulos da propriedade são exibidos. Deve haver apenas um elemento [labelInfo]() para cada elemento [propertyDescription](./propdesc-schema-propertydescription.md) .

Se houver vários elementos, o último será usado. Se nenhum elemento [labelInfo]() for fornecido, o rótulo da propriedade não será exibido; no entanto, isso normalmente seria um defeito.

## <a name="syntax"></a>Sintaxe


```
<!-- labelInfo -->
<xs:element name="labelInfo">
    <xs:complexType>
        <xs:attribute name="label" type="xs:string"/>
        <xs:attribute name="sortDescription">
            <xs:simpleType>
                <xs:restriction base="xs:string">
                    <xs:enumeration value="General"/>
                    <xs:enumeration value="AToZ"/>
                    <xs:enumeration value="LowestHighest"/>
                    <xs:enumeration value="OldestNewest"/>
                    <xs:enumeration value="SmallestLargest"/>
                </xs:restriction>
            </xs:simpleType>
        </xs:attribute>
        <xs:attribute name="invitationText" type="xs:string"/>
        <xs:attribute name="hideLabel" type="xs:boolean" default="false"/>
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
| label | Público. Opcional. O rótulo como é exibido na interface do usuário (por exemplo, o rótulo de coluna de detalhes ou o painel de visualização). A sintaxe permite uma cadeia de caracteres de exibição direta ou uma referência de cadeia de caracteres de exibição indireta. Use a cadeia de caracteres de exibição indireta porque ela pode ser localizada. <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-getdisplayname"><strong>IPropertyDescription:: GetDisplayName</strong></a> retorna o nome de exibição resolvido. | 
| sortDescription | Opcional. Especifica as cadeias de caracteres oferecidas como opções de classificação. <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-getsortdescription"><strong>IPropertyDescription:: GetSortDescription</strong></a> retorna essa descrição de classificação. Os valores a seguir fornecem as cadeias de caracteres da interface do usuário correspondentes.<ul><li>Geral: "classificar em andamento"/"classificar em andamento"</li><li>AToZ: "A na parte superior"/"Z no topo"</li><li>LowestHighest: "mais baixo no início"/"mais alto no início"</li><li>OldestNewest: "mais antigo no início"/"mais novo no início"</li><li>SmallestLargest: "menor no início"/"maior no início"</li></ul> | 
| invitationText | Opcional. O texto da cadeia de caracteres de ajuda que é exibido como uma instrução para o usuário para o controle ou dica de ferramenta (por exemplo, "inserir nome do autor".). A sintaxe permite uma cadeia de caracteres de exibição direta ou uma referência de cadeia de caracteres de exibição indireta. Use a cadeia de caracteres de exibição indireta porque ela pode ser localizada. <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-geteditinvitation"><strong>IPropertyDescription:: GetEditInvitation</strong></a> retorna o texto de convite resolvido. | 
| hideLabel | Opcional. O padrão é "falso". Indica se o rótulo está oculto. | 




 

 

 
