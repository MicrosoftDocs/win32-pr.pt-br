---
description: O elemento booliano opcional <isIndexed> especifica se o local descrito pelo conector de pesquisa é indexado (local ou remotamente usando o Windows Search 4 ou superior).
ms.assetid: e72b5614-454c-481f-bc31-897d2dea8042
title: Elemento IsIndexed (esquema do conector de pesquisa)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f658f6b932f6241b7af84e763d564ca0a8f1b5f0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090044"
---
# <a name="isindexed-element-search-connector-schema"></a><span data-ttu-id="f0df1-103">Elemento IsIndexed (esquema do conector de pesquisa)</span><span class="sxs-lookup"><span data-stu-id="f0df1-103">isIndexed Element (Search Connector Schema)</span></span>

<span data-ttu-id="f0df1-104">O elemento booliano opcional <isIndexed> especifica se o local descrito pelo conector de pesquisa é indexado (local ou remotamente usando o Windows Search 4 ou superior).</span><span class="sxs-lookup"><span data-stu-id="f0df1-104">The optional Boolean <isIndexed> element specifies whether the location described by the search connector is indexed (either locally or remotely using Windows Search 4 or higher).</span></span> <span data-ttu-id="f0df1-105">O valor padrão é true para pastas locais.</span><span class="sxs-lookup"><span data-stu-id="f0df1-105">The default value is true for local folders.</span></span> <span data-ttu-id="f0df1-106">Este elemento não tem elementos filho e nenhum atributo.</span><span class="sxs-lookup"><span data-stu-id="f0df1-106">This element has no child elements and no attributes.</span></span>

## <a name="syntax"></a><span data-ttu-id="f0df1-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f0df1-107">Syntax</span></span>


```
<!-- isIndexed -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
            ...
            <xs:element name="isIndexed" type="xsIboolean" minOccurs="0"/>
            ...
        </xs:all>
        <xs:attribute name="publisher" type="xs:string"/>
        <xs:attribute name="product" type="xs:string"/>
    </xs:complexType>
```



## <a name="element-information"></a><span data-ttu-id="f0df1-108">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="f0df1-108">Element Information</span></span>



| <span data-ttu-id="f0df1-109">Elemento pai</span><span class="sxs-lookup"><span data-stu-id="f0df1-109">Parent Element</span></span>                                                                                                   | <span data-ttu-id="f0df1-110">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="f0df1-110">Child Elements</span></span> |
|------------------------------------------------------------------------------------------------------------------|----------------|
| [<span data-ttu-id="f0df1-111">Elemento searchConnectorDescriptionType (esquema do conector de pesquisa)</span><span class="sxs-lookup"><span data-stu-id="f0df1-111">searchConnectorDescriptionType Element (Search Connector Schema)</span></span>](search-schema-searchconnectordescription.md) |                |



 

## <a name="example"></a><span data-ttu-id="f0df1-112">Exemplo</span><span class="sxs-lookup"><span data-stu-id="f0df1-112">Example</span></span>


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="https://schemas.adventureworks.com/searchConnector">
    ...
    <isIndexed>false</isIndexed>
    ...
</searchConnectionDescription>
```



 

 



