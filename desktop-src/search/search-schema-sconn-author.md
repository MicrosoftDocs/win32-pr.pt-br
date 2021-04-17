---
description: O <author> elemento opcional especifica o autor dessa biblioteca. Este elemento não tem elementos filho e nenhum atributo.
ms.assetid: c91042d5-9564-463a-9104-97b927027fc9
title: Elemento Author (esquema do conector de pesquisa)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74a2facbf4e3fa743b4dbe56a1c83eb57509c067
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105790314"
---
# <a name="author-element-search-connector-schema"></a><span data-ttu-id="94128-104">Elemento Author (esquema do conector de pesquisa)</span><span class="sxs-lookup"><span data-stu-id="94128-104">author Element (Search Connector Schema)</span></span>

<span data-ttu-id="94128-105">O <author> elemento opcional especifica o autor dessa biblioteca.</span><span class="sxs-lookup"><span data-stu-id="94128-105">The optional <author> element specifies the author of this library.</span></span> <span data-ttu-id="94128-106">Este elemento não tem elementos filho e nenhum atributo.</span><span class="sxs-lookup"><span data-stu-id="94128-106">This element has no child elements and no attributes.</span></span>

## <a name="syntax"></a><span data-ttu-id="94128-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="94128-107">Syntax</span></span>


```
<!-- author -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
            ...
            <xs:element name="author" type="xs:string" minOccurs="0"/>
            ...
        </xs:all>
        <xs:attribute name="publisher" type="xs:string"/>
        <xs:attribute name="product" type="xs:string"/>
    </xs:complexType>
```



## <a name="element-information"></a><span data-ttu-id="94128-108">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="94128-108">Element Information</span></span>



| <span data-ttu-id="94128-109">Elemento pai</span><span class="sxs-lookup"><span data-stu-id="94128-109">Parent Element</span></span>                                                                                                   | <span data-ttu-id="94128-110">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="94128-110">Child Elements</span></span> |
|------------------------------------------------------------------------------------------------------------------|----------------|
| [<span data-ttu-id="94128-111">Elemento searchConnectorDescriptionType (esquema do conector de pesquisa)</span><span class="sxs-lookup"><span data-stu-id="94128-111">searchConnectorDescriptionType Element (Search Connector Schema)</span></span>](search-schema-searchconnectordescription.md) |                |



 

## <a name="example"></a><span data-ttu-id="94128-112">Exemplo</span><span class="sxs-lookup"><span data-stu-id="94128-112">Example</span></span>


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="https://schemas.adventureworks.com/searchConnector">
    ...
    <author>Joe Smith</author>
    ...
</searchConnectionDescription>
```



 

 



