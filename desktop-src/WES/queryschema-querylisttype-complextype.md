---
title: Tipo complexo QueryListType
description: Define uma lista de consultas que podem conter um conjunto de seletores e supressers que são usados para incluir eventos em ou excluir eventos do conjunto de resultados.
ms.assetid: 3b9944e8-5913-4a77-a8fd-7efa43f3063f
keywords:
- Log de eventos do tipo complexo QueryListType
topic_type:
- apiref
api_name:
- QueryListType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 58cc6e83fb681f6244288088ea217097dd109c23
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105781297"
---
# <a name="querylisttype-complex-type"></a><span data-ttu-id="d6c14-104">Tipo complexo QueryListType</span><span class="sxs-lookup"><span data-stu-id="d6c14-104">QueryListType Complex Type</span></span>

<span data-ttu-id="d6c14-105">Define uma lista de consultas que podem conter um conjunto de seletores e supressers que são usados para incluir eventos em ou excluir eventos do conjunto de resultados.</span><span class="sxs-lookup"><span data-stu-id="d6c14-105">Defines a list of queries that can contain a set of selectors and suppressors that are used to include events in or exclude events from the result set.</span></span>

``` syntax
<xs:complexType name="QueryListType">
    <xs:sequence
        maxOccurs="unbounded"
    >
        <xs:element name="Query"
            type="QueryType"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="d6c14-106">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="d6c14-106">Child elements</span></span>



| <span data-ttu-id="d6c14-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="d6c14-107">Element</span></span>                                                  | <span data-ttu-id="d6c14-108">Type</span><span class="sxs-lookup"><span data-stu-id="d6c14-108">Type</span></span>                                                   | <span data-ttu-id="d6c14-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="d6c14-109">Description</span></span>                                                                                                                     |
|----------------------------------------------------------|--------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d6c14-110">**Consulta**</span><span class="sxs-lookup"><span data-stu-id="d6c14-110">**Query**</span></span>](queryschema-query-querylisttype-element.md) | [<span data-ttu-id="d6c14-111">**QueryType**</span><span class="sxs-lookup"><span data-stu-id="d6c14-111">**QueryType**</span></span>](queryschema-querytype-complextype.md) | <span data-ttu-id="d6c14-112">Define um conjunto de seletores e supressers que são usados para incluir eventos no ou excluir eventos do conjunto de resultados.</span><span class="sxs-lookup"><span data-stu-id="d6c14-112">Defines a set of selectors and suppressors that are used to include events in or exclude events from the result set.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="d6c14-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d6c14-113">Requirements</span></span>



| <span data-ttu-id="d6c14-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="d6c14-114">Requirement</span></span> | <span data-ttu-id="d6c14-115">Valor</span><span class="sxs-lookup"><span data-stu-id="d6c14-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="d6c14-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d6c14-116">Minimum supported client</span></span><br/> | <span data-ttu-id="d6c14-117">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d6c14-117">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="d6c14-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d6c14-118">Minimum supported server</span></span><br/> | <span data-ttu-id="d6c14-119">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="d6c14-119">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





