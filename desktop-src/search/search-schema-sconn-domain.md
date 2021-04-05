---
description: O <domain> elemento opcional especifica a URL do serviço de pesquisa usado por este conector de pesquisa. Ele é exibido no painel de detalhes. Este elemento não tem elementos filho e nenhum atributo.
ms.assetid: 60a27b13-0bb0-4cf6-9dce-a3abc79ce623
title: Elemento Domain (esquema do conector de pesquisa)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94b57819cf485bccbe63e7560f3fcb92811d7969
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826903"
---
# <a name="domain-element-search-connector-schema"></a><span data-ttu-id="28090-105">Elemento Domain (esquema do conector de pesquisa)</span><span class="sxs-lookup"><span data-stu-id="28090-105">domain Element (Search Connector Schema)</span></span>

<span data-ttu-id="28090-106">O <domain> elemento opcional especifica a URL do serviço de pesquisa usado por este conector de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="28090-106">The optional <domain> element specifies the URL of the search service used by this search connector.</span></span> <span data-ttu-id="28090-107">Ele é exibido no painel de detalhes.</span><span class="sxs-lookup"><span data-stu-id="28090-107">It is displayed in the details pane.</span></span> <span data-ttu-id="28090-108">Este elemento não tem elementos filho e nenhum atributo.</span><span class="sxs-lookup"><span data-stu-id="28090-108">This element has no child elements and no attributes.</span></span>

## <a name="syntax"></a><span data-ttu-id="28090-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="28090-109">Syntax</span></span>


```
<!-- domain -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
            ...
            <xs:element name="domain" type="xs:string" minOccurs="0"/>
            ...
        </xs:all>
        <xs:attribute name="publisher" type="xs:string"/>
        <xs:attribute name="product" type="xs:string"/>
    </xs:complexType>
```



## <a name="element-information"></a><span data-ttu-id="28090-110">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="28090-110">Element Information</span></span>



| <span data-ttu-id="28090-111">Elemento pai</span><span class="sxs-lookup"><span data-stu-id="28090-111">Parent Element</span></span>                                                                                                   | <span data-ttu-id="28090-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="28090-112">Child Elements</span></span> |
|------------------------------------------------------------------------------------------------------------------|----------------|
| [<span data-ttu-id="28090-113">Elemento searchConnectorDescriptionType (esquema do conector de pesquisa)</span><span class="sxs-lookup"><span data-stu-id="28090-113">searchConnectorDescriptionType Element (Search Connector Schema)</span></span>](search-schema-searchconnectordescription.md) |                |



 

## <a name="remarks"></a><span data-ttu-id="28090-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="28090-114">Remarks</span></span>

<span data-ttu-id="28090-115">A URL deve ser o domínio de nível superior para o provedor de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="28090-115">The URL should be the top-level domain for the search provider.</span></span> <span data-ttu-id="28090-116">Por exemplo, https://www.example.com.</span><span class="sxs-lookup"><span data-stu-id="28090-116">For example, https://www.example.com.</span></span>

## <a name="example"></a><span data-ttu-id="28090-117">Exemplo</span><span class="sxs-lookup"><span data-stu-id="28090-117">Example</span></span>


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="https://schemas.adventureworks.com/searchConnector">
    ...
    <domain>https://www.adventureworks.com</domain>
    ...
</searchConnectionDescription>
```



 

 



