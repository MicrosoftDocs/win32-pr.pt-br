---
description: O <propertyStore> elemento opcional especifica o local de um IPropertyStore baseado em XML para armazenar metadados abertos para esse conector de pesquisa. Este elemento não tem atributos e apenas um elemento filho.
ms.assetid: 5720c69f-af87-432b-857c-dbd66ba74e80
title: Elemento propertyStore (esquema do conector de pesquisa)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11f8cda6457de764b00519a81a1134e7eecc8638
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646857"
---
# <a name="propertystore-element-search-connector-schema"></a>Elemento propertyStore (esquema do conector de pesquisa)

O <propertyStore> elemento opcional especifica o local de um IPropertyStore baseado em XML para armazenar metadados abertos para esse conector de pesquisa. Este elemento não tem atributos e apenas um elemento filho.

## <a name="syntax"></a>Syntax


```
<!-- propertyStore -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
        ...
        <xs:element name="propertyStore" type="propertyStoreType" minOccurs="0">
            <xs:element name="property" minOccurs="0" maxOccurrs="unbounded"/>
        </xs:element>
        ...
        </xs:all>
        <xs:attribute name="publisher" type="xs:string"/>
        <xs:attribute name="product" type="xs:string"/>
    </xs:complexType>
```



## <a name="element-information"></a>Informações do elemento



| Elemento pai                                                                                                   | Elementos filho                                                                                            |
|------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| [Elemento searchConnectorDescriptionType (esquema do conector de pesquisa)](search-schema-searchconnectordescription.md) | [Elemento Property de propertyStore (esquema do conector de pesquisa)](search-schema-sconn-propstore-property.md) |



 

## <a name="example"></a>Exemplo

O exemplo a seguir mostra um <propertyStore> elemento com dois <property> elementos.


```
<propertyStore>
    <property name="OpenSearchHTMLRolloverTemplate">https://www.adventureworks.com/Search/?Query={searchTerms}</property>
    <property name="isExternal" type="boolean">true</property>
</propertyStore>
```



 

 



