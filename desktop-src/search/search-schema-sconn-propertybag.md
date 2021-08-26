---
description: O elemento &lt; propertyBag necessário especifica um conjunto de uma ou mais propriedades &gt; usadas por esse provedor de localização.
ms.assetid: 63f8f2e4-3b52-4d6e-8d3a-2e133aac0e86
title: Elemento propertyBag (esquema do conector de pesquisa)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7c186e9502c48a1fc052acf28bc8bd8063085b8
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122883324"
---
# <a name="propertybag-element-search-connector-schema"></a>Elemento propertyBag (esquema do conector de pesquisa)

O elemento &lt; propertyBag necessário especifica um conjunto de uma ou mais propriedades &gt; usadas por esse provedor de localização.

## <a name="syntax"></a>Syntax


```
<!-- propertyBag -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
        ...
            <xs:element name="locationProvider" minOccurs="0">
                <xs:complexType>
                    <xs:all>
                        <xs:element name="propertyBag" type="propertyStoreType" minOccurs="0">
                            <xs:element name="property" minOccurs="0" maxOccurrs="unbounded"/>
                        </xs:element>
                    </xs:all>
                <xs:attribute name="clsid" use="required"/>
                <xs:attribute name="codebase" type="xs:string"/>
            </xs:element>
        ...
        </xs:all>
        <xs:attribute name="publisher" type="xs:string"/>
        <xs:attribute name="product" type="xs:string"/>
    </xs:complexType>
```



## <a name="element-information"></a>Informações do elemento



| Elemento pai                                                                                 | Elementos filho                                                                                 |
|------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| [Elemento locationProvider (esquema do conector de pesquisa)](search-schema-sconn-locationprovider.md) | [Elemento property (Esquema do Conector de Pesquisa)](search-schema-sconn-locationproviderproperty.md) |



 

## <a name="example-of-a-propertybag-element-and-property-elements"></a>Exemplo de elementos PropertyBag e elementos de propriedade


```
<locationProvider clsid="{48E277F6-4E74-4cd6-BA6F-FA4F42898223}">
    <propertyBag>
        <property name="OpenSearchShortName">MSDN</property>
        <property name="OpenSearchQueryTemplate">https://social.msdn.microsoft.com/Search/Feed.aspx?locale=en-US&Query={searchTerms}&format=RSS&StartIndex={startIndex}</property>
        <property name="MaximumResultCount" type="uint32">100</property>
    </propertyBag>
</locationProvider>
```



 

 



