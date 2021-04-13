---
description: O elemento booliano <isSearchOnlyItem> especifica se o provedor de pesquisa dá suporte ao modo de procura, além do modo de pesquisa. Esse elemento é opcional e não tem nenhum elemento filho e nenhum atributo.
ms.assetid: eec1b735-ae78-48ef-8ebf-05b9fd038963
title: Elemento isSearchOnlyItem (esquema do conector de pesquisa)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ded7b62cde5cf813603d5cc87c41fe2c443b42d2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501456"
---
# <a name="issearchonlyitem-element-search-connector-schema"></a><span data-ttu-id="711a0-104">Elemento isSearchOnlyItem (esquema do conector de pesquisa)</span><span class="sxs-lookup"><span data-stu-id="711a0-104">isSearchOnlyItem Element (Search Connector Schema)</span></span>

<span data-ttu-id="711a0-105">O elemento booliano <isSearchOnlyItem> especifica se o provedor de pesquisa dá suporte ao modo de procura, além do modo de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="711a0-105">The Boolean <isSearchOnlyItem> element specifies whether the search provider supports browse mode in addition to search mode.</span></span> <span data-ttu-id="711a0-106">Esse elemento é opcional e não tem nenhum elemento filho e nenhum atributo.</span><span class="sxs-lookup"><span data-stu-id="711a0-106">This element is optional and has no child elements and no attributes.</span></span>

## <a name="syntax"></a><span data-ttu-id="711a0-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="711a0-107">Syntax</span></span>


```
<!-- isSearchOnlyItem -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
            <xs:element name="isSearchOnlyItem" type="xs:boolean" default="false" minOccurs="0"/>
            ...
        </xs:all>
        <xs:attribute name="publisher" type="xs:string"/>
        <xs:attribute name="product" type="xs:string"/>
    </xs:complexType>
```



## <a name="element-information"></a><span data-ttu-id="711a0-108">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="711a0-108">Element Information</span></span>



| <span data-ttu-id="711a0-109">Elemento pai</span><span class="sxs-lookup"><span data-stu-id="711a0-109">Parent Element</span></span>                                                                                                   | <span data-ttu-id="711a0-110">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="711a0-110">Child Elements</span></span> |
|------------------------------------------------------------------------------------------------------------------|----------------|
| [<span data-ttu-id="711a0-111">Elemento searchConnectorDescriptionType (esquema do conector de pesquisa)</span><span class="sxs-lookup"><span data-stu-id="711a0-111">searchConnectorDescriptionType Element (Search Connector Schema)</span></span>](search-schema-searchconnectordescription.md) |                |



 

## <a name="remarks"></a><span data-ttu-id="711a0-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="711a0-112">Remarks</span></span>

<span data-ttu-id="711a0-113">O valor `true` indica que o local do conector de pesquisa não pode ser procurado pelos usuários.</span><span class="sxs-lookup"><span data-stu-id="711a0-113">The value `true` indicates that the search connector location cannot be browsed by users.</span></span> <span data-ttu-id="711a0-114">O valor `false` indica que os usuários podem procurar o local do conector de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="711a0-114">The value `false` indicates that users can browse the search connector location.</span></span>

## <a name="example"></a><span data-ttu-id="711a0-115">Exemplo</span><span class="sxs-lookup"><span data-stu-id="711a0-115">Example</span></span>


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="http://schemas.microsoft.com/windows/2009/searchConnector">
    ...
    <isSearchOnlyItem>true</isSearchOnlyItem>
    ...
</searchConnectionDescription>
```



 

 



