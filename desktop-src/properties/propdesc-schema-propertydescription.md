---
description: Descreve uma única propriedade canônica exclusiva.
ms.assetid: 1a36ec83-5d8a-4fc5-be3d-a8c2f0983057
title: propertyDescription
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 233f6d9b1242a9f02b2edbb2bb29cefaef625c7e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921338"
---
# <a name="propertydescription"></a>propertyDescription

Descreve uma única propriedade canônica exclusiva. Cada propriedade desse tipo deveria estar disponível no sistema deve ter um elemento [propertyDescription]() correspondente.

## <a name="syntax-for-windows-7"></a>Sintaxe do Windows 7


```
<!-- propertyDescription for Windows 7-->
<xs:element name="propertyDescription">
    <xs:complexType>
        <xs:all>
            <xs:element ref="searchInfo"          minOccurs="0" maxOccurs="1"/>
            <xs:element ref="labelInfo"           minOccurs="0" maxOccurs="1"/>
            <xs:element ref="typeInfo"            minOccurs="0" maxOccurs="1"/>
            <xs:element ref="aliasInfo"           minOccurs="0" maxOccurs="1"/>
            <xs:element ref="displayInfo"         minOccurs="0" maxOccurs="1"/>
            <xs:element ref="relatedPropertyInfo" minOccurs="0" maxOccurs="1"/>
        </xs:all>

        <xs:attribute name="formatID"  type="uuid" use="required"/>
        <xs:attribute name="propID"    type="propid" use="required"/>
        <xs:attribute name="name"      type="canonical-name"        use="required"/>
    </xs:complexType>
</xs:element>
```



## <a name="syntax-for-vista"></a>Sintaxe do vista


```
<!-- propertyDescription for Windows Vista-->
<xs:element name="propertyDescription">
    <xs:complexType>
        <xs:all>
            <xs:element ref="searchInfo"          minOccurs="0" maxOccurs="1"/>
            <xs:element ref="labelInfo"           minOccurs="0" maxOccurs="1"/>
            <xs:element ref="typeInfo"            minOccurs="0" maxOccurs="1"/>
            <xs:element ref="aliasInfo"           minOccurs="0" maxOccurs="1"/>
            <xs:element ref="displayInfo"         minOccurs="0" maxOccurs="1"/>
        </xs:all>

        <xs:attribute name="formatID"  type="uuid" use="required"/>
        <xs:attribute name="propID"    type="xs:nonNegativeInteger" use="required"/>
        <xs:attribute name="name"      type="canonical-name"        use="required"/>
    </xs:complexType>
</xs:element>
```



## <a name="element-information"></a>Informações do elemento



| Elemento pai                                                           | Elementos filho                                                   |
|--------------------------------------------------------------------------|------------------------------------------------------------------|
| [propertyDescriptionList](./propdesc-schema-propertydescriptionlist.md) | [searchInfo](./propdesc-schema-searchinfo.md)                   |
|                                                                          | [labelInfo](./propdesc-schema-labelinfo.md)                     |
|                                                                          | [typeInfo](./propdesc-schema-typeinfo.md)                       |
|                                                                          | [aliasInfo](./propdesc-schema-aliasinfo.md)                     |
|                                                                          | [displayInfo](./propdesc-schema-displayinfo.md)                 |
|                                                                          | [relatedPropertyInfo](./propdesc-schema-relatedpropertyinfo.md) |



 

## <a name="attributes"></a>Atributos



| Atributo | Descrição                                                                                                                                                                                                                                                                                                                                                                         |
|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| name      | Obrigatórios. O nome da propriedade canônica, exclusivo para o sistema; por exemplo, `System.Rating` . Essa cadeia de caracteres é do tipo canônico e é limitada a 64 caracteres. O nome diferencia maiúsculas de minúsculas e deve usar a seguinte sintaxe: Publisher. Application. PropertyName. [**IPropertyDescription:: Getcanônicaname**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-getcanonicalname) retorna esse valor. |
| FormatID  | Obrigatórios. O identificador de formato da propriedade (FMTID). O valor deve incluir chaves de circunscrição; por exemplo, `{64440492-4C8B-11D1-8B70-080036B11A03}` . [**IPropertyDescription:: GetPropertyKey**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-getpropertykey) retorna esse valor.                                                                                                                       |
| propID    | Obrigatórios. O identificador de propriedade (PID); por exemplo, `9` . [**IPropertyDescription:: GetPropertyKey**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-getpropertykey) retorna esse valor. Esse valor deve ser maior ou igual a 2. Os valores 0 e 1 são reservados pelo sistema.                                                                                                                  |



 

 

 
