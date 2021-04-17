---
description: O elemento booliano <supportsAdvancedQuerySyntax> especifica se o provedor de pesquisa dá suporte à sintaxe de consulta avançada. O padrão é falso. Esse elemento é opcional e não tem nenhum elemento filho e nenhum atributo.
ms.assetid: d4aef1f1-63c8-4e9a-9e22-5efbb8c523b2
title: Elemento supportsAdvancedQuerySyntax (esquema do conector de pesquisa)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39d31eb96615c952f703729fd9d22f2e5d27f38b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105763152"
---
# <a name="supportsadvancedquerysyntax-element-search-connector-schema"></a><span data-ttu-id="8ae5d-105">Elemento supportsAdvancedQuerySyntax (esquema do conector de pesquisa)</span><span class="sxs-lookup"><span data-stu-id="8ae5d-105">supportsAdvancedQuerySyntax Element (Search Connector Schema)</span></span>

<span data-ttu-id="8ae5d-106">O elemento booliano <supportsAdvancedQuerySyntax> especifica se o provedor de pesquisa dá suporte à [sintaxe de consulta avançada](-search-3x-advancedquerysyntax.md).</span><span class="sxs-lookup"><span data-stu-id="8ae5d-106">The Boolean <supportsAdvancedQuerySyntax> element specifies whether the search provider supports the [Advanced Query Syntax](-search-3x-advancedquerysyntax.md).</span></span> <span data-ttu-id="8ae5d-107">O padrão é falso.</span><span class="sxs-lookup"><span data-stu-id="8ae5d-107">The default is false.</span></span> <span data-ttu-id="8ae5d-108">Esse elemento é opcional e não tem nenhum elemento filho e nenhum atributo.</span><span class="sxs-lookup"><span data-stu-id="8ae5d-108">This element is optional and has no child elements and no attributes.</span></span>

## <a name="syntax"></a><span data-ttu-id="8ae5d-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="8ae5d-109">Syntax</span></span>


```
<!-- supportsAdvancedQuerySyntax -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
            ...
            <xs:element name="supportsAdvancedQuerySyntax" type="xs:boolean" default="false" minOccurs="0"/>
            ...
        </xs:all>
        <xs:attribute name="publisher" type="xs:string"/>
        <xs:attribute name="product" type="xs:string"/>
    </xs:complexType>
```



## <a name="element-information"></a><span data-ttu-id="8ae5d-110">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="8ae5d-110">Element Information</span></span>



| <span data-ttu-id="8ae5d-111">Elemento pai</span><span class="sxs-lookup"><span data-stu-id="8ae5d-111">Parent Element</span></span>                                                                                                   | <span data-ttu-id="8ae5d-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="8ae5d-112">Child Elements</span></span> |
|------------------------------------------------------------------------------------------------------------------|----------------|
| [<span data-ttu-id="8ae5d-113">Elemento searchConnectorDescriptionType (esquema do conector de pesquisa)</span><span class="sxs-lookup"><span data-stu-id="8ae5d-113">searchConnectorDescriptionType Element (Search Connector Schema)</span></span>](search-schema-searchconnectordescription.md) |                |



 

## <a name="remarks"></a><span data-ttu-id="8ae5d-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="8ae5d-114">Remarks</span></span>

<span data-ttu-id="8ae5d-115">O valor `true` indica que o provedor de pesquisa dá suporte à sintaxe de consulta avançada enviada em consultas de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="8ae5d-115">The value `true` indicates that the search provider supports Advanced Query Syntax sent in search queries.</span></span>

## <a name="example"></a><span data-ttu-id="8ae5d-116">Exemplo</span><span class="sxs-lookup"><span data-stu-id="8ae5d-116">Example</span></span>


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="http://schemas.microsoft.com/windows/2009/searchConnector">
    ...
    <supportsAdvancedQuerySyntax>true</supportsAdvancedQuerySyntax>
    ...
</searchConnectionDescription>
```



 

 



