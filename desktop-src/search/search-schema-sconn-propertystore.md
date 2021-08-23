---
description: O <propertyStore> elemento opcional especifica o local de um IPropertyStore baseado em XML para armazenar metadados abertos para esse conector de pesquisa. Este elemento não tem atributos e apenas um elemento filho.
ms.assetid: 5720c69f-af87-432b-857c-dbd66ba74e80
title: Elemento propertyStore (esquema do conector de pesquisa)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0de5a9e801163bd85635b82c1915394f24c39d3dfdafcb64c81fcff0bf84a219
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119351846"
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



 

 



