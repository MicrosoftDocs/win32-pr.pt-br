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
# <a name="propertystore-element-search-connector-schema"></a><span data-ttu-id="c2d99-104">Elemento propertyStore (esquema do conector de pesquisa)</span><span class="sxs-lookup"><span data-stu-id="c2d99-104">propertyStore Element (Search Connector Schema)</span></span>

<span data-ttu-id="c2d99-105">O <propertyStore> elemento opcional especifica o local de um IPropertyStore baseado em XML para armazenar metadados abertos para esse conector de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="c2d99-105">The optional <propertyStore> element specifies the location of an XML-based IPropertyStore to store open metadata for this search connector.</span></span> <span data-ttu-id="c2d99-106">Este elemento não tem atributos e apenas um elemento filho.</span><span class="sxs-lookup"><span data-stu-id="c2d99-106">This element has no attributes and only one child element.</span></span>

## <a name="syntax"></a><span data-ttu-id="c2d99-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="c2d99-107">Syntax</span></span>


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



## <a name="element-information"></a><span data-ttu-id="c2d99-108">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="c2d99-108">Element Information</span></span>



| <span data-ttu-id="c2d99-109">Elemento pai</span><span class="sxs-lookup"><span data-stu-id="c2d99-109">Parent Element</span></span>                                                                                                   | <span data-ttu-id="c2d99-110">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="c2d99-110">Child Elements</span></span>                                                                                            |
|------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c2d99-111">Elemento searchConnectorDescriptionType (esquema do conector de pesquisa)</span><span class="sxs-lookup"><span data-stu-id="c2d99-111">searchConnectorDescriptionType Element (Search Connector Schema)</span></span>](search-schema-searchconnectordescription.md) | [<span data-ttu-id="c2d99-112">Elemento Property de propertyStore (esquema do conector de pesquisa)</span><span class="sxs-lookup"><span data-stu-id="c2d99-112">property Element of propertyStore (Search Connector Schema)</span></span>](search-schema-sconn-propstore-property.md) |



 

## <a name="example"></a><span data-ttu-id="c2d99-113">Exemplo</span><span class="sxs-lookup"><span data-stu-id="c2d99-113">Example</span></span>

<span data-ttu-id="c2d99-114">O exemplo a seguir mostra um <propertyStore> elemento com dois <property> elementos.</span><span class="sxs-lookup"><span data-stu-id="c2d99-114">The following example shows a <propertyStore> element with two <property> elements.</span></span>


```
<propertyStore>
    <property name="OpenSearchHTMLRolloverTemplate">https://www.adventureworks.com/Search/?Query={searchTerms}</property>
    <property name="isExternal" type="boolean">true</property>
</propertyStore>
```



 

 



