---
description: O opcional <description> o elemento Especifica uma descrição para este conector de pesquisa. Este elemento não tem elementos filho e nenhum atributo.
ms.assetid: 0e9d806c-7dfd-4e7f-8843-15a4e22f317f
title: Elemento Description (esquema do conector de pesquisa)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a9d82fd6ad3ae45c4a8c3700c4822387a81880d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296233"
---
# <a name="description-element-search-connector-schema"></a><span data-ttu-id="09657-105">Elemento Description (esquema do conector de pesquisa)</span><span class="sxs-lookup"><span data-stu-id="09657-105">description Element (Search Connector Schema)</span></span>

<span data-ttu-id="09657-106">O opcional</span><span class="sxs-lookup"><span data-stu-id="09657-106">The optional</span></span> <description> <span data-ttu-id="09657-107">o elemento Especifica uma descrição para este conector de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="09657-107">element specifies a description for this search connector.</span></span> <span data-ttu-id="09657-108">Este elemento não tem elementos filho e nenhum atributo.</span><span class="sxs-lookup"><span data-stu-id="09657-108">This element has no child elements and no attributes.</span></span>

## <a name="syntax"></a><span data-ttu-id="09657-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="09657-109">Syntax</span></span>


```
<!-- description -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
            ...
            <xs:element name="description" type="xs:string" minOccurs="0"/>
            ...
        </xs:all>
        <xs:attribute name="publisher" type="xs:string"/>
        <xs:attribute name="product" type="xs:string"/>
    </xs:complexType>
```



## <a name="element-information"></a><span data-ttu-id="09657-110">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="09657-110">Element Information</span></span>



| <span data-ttu-id="09657-111">Elemento pai</span><span class="sxs-lookup"><span data-stu-id="09657-111">Parent Element</span></span>                                                                                                   | <span data-ttu-id="09657-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="09657-112">Child Elements</span></span> |
|------------------------------------------------------------------------------------------------------------------|----------------|
| [<span data-ttu-id="09657-113">Elemento searchConnectorDescriptionType (esquema do conector de pesquisa)</span><span class="sxs-lookup"><span data-stu-id="09657-113">searchConnectorDescriptionType Element (Search Connector Schema)</span></span>](search-schema-searchconnectordescription.md) |                |



 

## <a name="remarks"></a><span data-ttu-id="09657-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="09657-114">Remarks</span></span>

<span data-ttu-id="09657-115">A descrição deve ser amigável para o usuário, pois pode ser usada em dicas de ferramenta.</span><span class="sxs-lookup"><span data-stu-id="09657-115">The description should be user-friendly as it may be used in tooltips.</span></span>

## <a name="example"></a><span data-ttu-id="09657-116">Exemplo</span><span class="sxs-lookup"><span data-stu-id="09657-116">Example</span></span>


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="https://schemas.adventureworks.com/searchConnector">
    ...
    <description>Search AdventureWorks.com</description>
    ...
</searchConnectionDescription>
```



 

 



