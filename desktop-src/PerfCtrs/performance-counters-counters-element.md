---
description: Identifica o nó raiz da seção de contadores de um manifesto de instrumentação.
ms.assetid: f16f432b-466f-4a3c-bc1b-e80b876a2511
title: Elemento Counters
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 11ced77890dba6d47f713642adf9b41d4b30f6a9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103828383"
---
# <a name="counters-element"></a><span data-ttu-id="59ca2-103">Elemento Counters</span><span class="sxs-lookup"><span data-stu-id="59ca2-103">counters Element</span></span>

<span data-ttu-id="59ca2-104">Identifica o nó raiz da seção de contadores de um manifesto de instrumentação.</span><span class="sxs-lookup"><span data-stu-id="59ca2-104">Identifies the root node of the counters section of an instrumentation manifest.</span></span>

``` syntax
<xs:element name="counters"
    type="man:counters"
>
    <xs:key name="uniqueprovGUID">
        <xs:selector
            xpath="./man:provider"
         />
        <xs:field
            xpath="@providerGuid"
         />
    </xs:key>
    <xs:key name="uniqueCounterSetGUID">
        <xs:selector
            xpath="./man:provider/man:counterSet"
         />
        <xs:field
            xpath="@guid"
         />
    </xs:key>
    <xs:key name="uniqueCounterSetURI">
        <xs:selector
            xpath="./man:provider/man:counterSet"
         />
        <xs:field
            xpath="@uri"
         />
    </xs:key>
    <xs:key name="uniqueCounterSetName">
        <xs:selector
            xpath="./man:provider/man:counterSet"
         />
        <xs:field
            xpath="@name"
         />
    </xs:key>
    <xs:key name="uniqueCounterSetSymbol">
        <xs:selector
            xpath="./man:provider/man:counterSet"
         />
        <xs:field
            xpath="@symbol"
         />
    </xs:key>
    <xs:unique name="uniqueCounterSymbol">
        <xs:selector
            xpath="./man:provider/man:counterSet/man:counter"
         />
        <xs:field
            xpath="@symbol"
         />
    </xs:unique>
    <xs:key name="uniqueCounterURI">
        <xs:selector
            xpath="./man:provider/man:counterSet/man:counter"
         />
        <xs:field
            xpath="@uri"
         />
    </xs:key>
</xs:element>
```

## <a name="remarks"></a><span data-ttu-id="59ca2-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="59ca2-105">Remarks</span></span>

<span data-ttu-id="59ca2-106">O nó pai deste elemento é o elemento de [**Instrumentação**](/windows/desktop/WES/eventmanifestschema-instrumentationtype-complextype) do manifesto.</span><span class="sxs-lookup"><span data-stu-id="59ca2-106">This element's parent node is the [**instrumentation**](/windows/desktop/WES/eventmanifestschema-instrumentationtype-complextype) element of the manifest.</span></span>

## <a name="requirements"></a><span data-ttu-id="59ca2-107">Requisitos</span><span class="sxs-lookup"><span data-stu-id="59ca2-107">Requirements</span></span>



| <span data-ttu-id="59ca2-108">Requisito</span><span class="sxs-lookup"><span data-stu-id="59ca2-108">Requirement</span></span> | <span data-ttu-id="59ca2-109">Valor</span><span class="sxs-lookup"><span data-stu-id="59ca2-109">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="59ca2-110">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="59ca2-110">Minimum supported client</span></span><br/> | <span data-ttu-id="59ca2-111">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="59ca2-111">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="59ca2-112">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="59ca2-112">Minimum supported server</span></span><br/> | <span data-ttu-id="59ca2-113">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="59ca2-113">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

