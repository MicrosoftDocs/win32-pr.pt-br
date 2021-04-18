---
description: Contêiner para um ou vários elementos propertyDescription individuais.
ms.assetid: b54aaa85-6928-470e-9630-44b094205106
title: propertyDescriptionList
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2cd0beaf4dbbd8b71c7f4b3335c169754c704d9c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105751531"
---
# <a name="propertydescriptionlist"></a>propertyDescriptionList

Contêiner para um ou vários elementos [propertyDescription](./propdesc-schema-propertydescription.md) individuais. Um arquivo de esquema de descrição da propriedade. propDesc deve conter pelo menos um elemento [propertyDescriptionList]() .

## <a name="syntax"></a>Syntax


```
<!-- propertyDescriptionList -->
<xs:element name="propertyDescriptionList">
    <xs:complexType>
        <xs:sequence>
            <xs:element ref="s:propertyDescription" minOccurs="1" maxOccurs="unbounded"/>
        </xs:sequence>
        <xs:attribute name="publisher" type="xs:string" use="required"/>
        <xs:attribute name="product"   type="xs:string" use="required"/>
    </xs:complexType>

    <xs:unique name="No_two_propertyDescriptions_can_have_the_same_formatid_and_propid">
        <xs:selector xpath="s:propertyDescription"/>
        <xs:field    xpath="@formatID"/>
        <xs:field    xpath="@propID"/>
    </xs:unique>

    <xs:unique name="No_two_propertyDescriptions_can_have_the_same_canonical_name">
        <xs:selector xpath="s:propertyDescription"/>
        <xs:field    xpath="@name"/>
    </xs:unique>
</xs:element>
```



## <a name="element-information"></a>Informações do elemento



| Elemento pai                        | Elementos filho                                                   |
|---------------------------------------|------------------------------------------------------------------|
| [schema](./propdesc-schema-entry.md) | [propertyDescription](./propdesc-schema-propertydescription.md) |



 

## <a name="attributes"></a>Atributos



| Atributo | Descrição                                                               |
|-----------|---------------------------------------------------------------------------|
| editor | Público. Obrigatórios. O nome de exibição do Publicador que fornece o esquema. |
| product   | Público. Obrigatórios. O nome de exibição do produto que fornece o esquema.   |



 

## <a name="remarks"></a>Comentários

O [propertyDescriptionList]() não deve ser confundido com "listas de propriedades" e [**IPropertyDescriptionList**](/windows/win32/api/propsys/nn-propsys-ipropertydescriptionlist), que são completamente separadas.

 

 
