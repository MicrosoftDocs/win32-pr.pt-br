---
description: Descreve uma única propriedade canônica exclusiva.
ms.assetid: 1a36ec83-5d8a-4fc5-be3d-a8c2f0983057
title: Propertydescription
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1797880fbc9ce5bf56999c6fbd869b259f893f1391fbde6fca580da29dac3a61
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120011466"
---
# <a name="propertydescription"></a>Propertydescription

Descreve uma única propriedade canônica exclusiva. Cada propriedade que se destina a estar disponível no sistema deve ter um [elemento propertyDescription]() correspondente.

## <a name="syntax-for-windows-7"></a>Sintaxe para Windows 7


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



## <a name="syntax-for-vista"></a>Sintaxe para Vista


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
|                                                                          | [Typeinfo](./propdesc-schema-typeinfo.md)                       |
|                                                                          | [Aliasinfo](./propdesc-schema-aliasinfo.md)                     |
|                                                                          | [displayInfo](./propdesc-schema-displayinfo.md)                 |
|                                                                          | [relatedPropertyInfo](./propdesc-schema-relatedpropertyinfo.md) |



 

## <a name="attributes"></a>Atributos



| Atributo | Descrição                                                                                                                                                                                                                                                                                                                                                                         |
|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| name      | Obrigatórios. O nome da propriedade canônica, exclusivo para o sistema; por exemplo, `System.Rating` . Essa cadeia de caracteres é do tipo canônica e é limitada a 64 caracteres. O nome faz a resiência de minúsculas e deve usar a seguinte sintaxe: Publisher. Application.PropertyName. [**IPropertyDescription::GetCanonicalName**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-getcanonicalname) retorna esse valor. |
| formatID  | Obrigatórios. O FMTID (identificador de formato) da propriedade. O valor deve incluir chaves delimitadores; por exemplo, `{64440492-4C8B-11D1-8B70-080036B11A03}` . [**IPropertyDescription::GetPropertyKey**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-getpropertykey) retorna esse valor.                                                                                                                       |
| Propid    | Obrigatórios. O PID (identificador de propriedade); por exemplo, `9` . [**IPropertyDescription::GetPropertyKey**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-getpropertykey) retorna esse valor. Esse valor deve ser maior ou igual a 2. Os valores 0 e 1 são reservados pelo sistema.                                                                                                                  |



 

 

 
