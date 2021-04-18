---
description: O <propertyStore> elemento especifica um conjunto de uma ou mais propriedades usadas por essa biblioteca. Esse elemento é opcional e não tem atributos.
ms.assetid: 19532C1F-686F-4c14-8BA8-0043E77BE594
title: Elemento propertyStore (esquema de biblioteca)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ad3b2c15180d6859ea54dea63ec7fc46b7e636c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104968092"
---
# <a name="propertystore-element-library-schema"></a><span data-ttu-id="8173b-104">Elemento propertyStore (esquema de biblioteca)</span><span class="sxs-lookup"><span data-stu-id="8173b-104">propertyStore Element (Library Schema)</span></span>

<span data-ttu-id="8173b-105">O <propertyStore> elemento especifica um conjunto de uma ou mais propriedades usadas por essa biblioteca.</span><span class="sxs-lookup"><span data-stu-id="8173b-105">The <propertyStore> element specifies a set of one or more properties used by this library.</span></span> <span data-ttu-id="8173b-106">Esse elemento é opcional e não tem atributos.</span><span class="sxs-lookup"><span data-stu-id="8173b-106">This element is optional and has no attributes.</span></span>

## <a name="syntax"></a><span data-ttu-id="8173b-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="8173b-107">Syntax</span></span>

``` syntax
<!-- propertyStore -->
<xs:element name="propertyStore" minOccurs="0">
    <xs:complexType>
        <xs:complexContent>
            <!-- properties are extensions of propertyStoreType -->
            <xs:extension base="propertyStoreType"/>        
        </xs:complexContent>
    </xs:complexType>
</xs:element>
```

## <a name="element-information"></a><span data-ttu-id="8173b-108">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="8173b-108">Element Information</span></span>



| <span data-ttu-id="8173b-109">Elemento pai</span><span class="sxs-lookup"><span data-stu-id="8173b-109">Parent Element</span></span>                                                               | <span data-ttu-id="8173b-110">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="8173b-110">Child Elements</span></span>                                                   |
|------------------------------------------------------------------------------|------------------------------------------------------------------|
| [<span data-ttu-id="8173b-111">Elemento libraryDescription (esquema de biblioteca)</span><span class="sxs-lookup"><span data-stu-id="8173b-111">libraryDescription Element (Library Schema)</span></span>](schema-librarydescription.md) | [<span data-ttu-id="8173b-112">Elemento Property (esquema de biblioteca)</span><span class="sxs-lookup"><span data-stu-id="8173b-112">property Element (Library Schema)</span></span>](schema-library-property.md) |



 

## <a name="remarks"></a><span data-ttu-id="8173b-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="8173b-113">Remarks</span></span>

<span data-ttu-id="8173b-114">O <propertyStore> elemento pode ter um ou mais <property> elementos filho.</span><span class="sxs-lookup"><span data-stu-id="8173b-114">The <propertyStore> element can have one or more <property> child elements.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8173b-115">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="8173b-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8173b-116">Esquema de descrição da biblioteca</span><span class="sxs-lookup"><span data-stu-id="8173b-116">Library Description Schema</span></span>](library-schema-entry.md)
</dt> <dt>

[<span data-ttu-id="8173b-117">Esquema de descrição do conector de pesquisa</span><span class="sxs-lookup"><span data-stu-id="8173b-117">Search Connector Description Schema</span></span>](../search/search-sconn-desc-schema-entry.md)
</dt> </dl>

 

 
