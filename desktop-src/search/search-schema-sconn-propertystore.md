---
description: O &lt; elemento de propertyStore opcional &gt; especifica o local de um IPropertyStore baseado em XML para armazenar metadados abertos para esse conector de pesquisa. Este elemento não tem atributos e apenas um elemento filho.
ms.assetid: 5720c69f-af87-432b-857c-dbd66ba74e80
title: Elemento propertyStore (esquema do conector de pesquisa)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73c617f560e0471062064bcec8020dd5e6efa026
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122886800"
---
# <a name="propertystore-element-search-connector-schema"></a>Elemento propertyStore (esquema do conector de pesquisa)

O &lt; elemento de propertyStore opcional &gt; especifica o local de um IPropertyStore baseado em XML para armazenar metadados abertos para esse conector de pesquisa. Este elemento não tem atributos e apenas um elemento filho.

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

O exemplo a seguir mostra &lt; um &gt; elemento propertyStore com &lt; dois &gt; elementos Property.


```
<propertyStore>
    <property name="OpenSearchHTMLRolloverTemplate">https://www.adventureworks.com/Search/?Query={searchTerms}</property>
    <property name="isExternal" type="boolean">true</property>
</propertyStore>
```



 

 



