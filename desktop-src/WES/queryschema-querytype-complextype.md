---
title: Tipo de consulta complexo
description: Define um conjunto de consultas de seletor e supressor que são usadas para incluir eventos no ou excluir eventos do conjunto de resultados.
ms.assetid: 223d0127-f097-45f8-8511-1a56d9c41e84
keywords:
- QueryType tipo complexo EventLog
topic_type:
- apiref
api_name:
- QueryType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 50c0779b90a6f2e74a873b13d79c6e2083afd0ee
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085511"
---
# <a name="querytype-complex-type"></a><span data-ttu-id="fc997-104">Tipo de consulta complexo</span><span class="sxs-lookup"><span data-stu-id="fc997-104">QueryType Complex Type</span></span>

<span data-ttu-id="fc997-105">Define um conjunto de consultas de seletor e supressor que são usadas para incluir eventos no ou excluir eventos do conjunto de resultados.</span><span class="sxs-lookup"><span data-stu-id="fc997-105">Defines a set of selector and suppressor queries that are used to include events in or exclude events from the result set.</span></span>

``` syntax
<xs:complexType name="QueryType">
    <xs:choice
        maxOccurs="unbounded"
    >
        <xs:element name="Select">
            <xs:complexType
                mixed="true"
            >
                <xs:attribute name="Path"
                    type="anyURI"
                 />
            </xs:complexType>
        </xs:element>
        <xs:element name="Suppress">
            <xs:complexType
                mixed="true"
            >
                <xs:attribute name="Path"
                    type="anyURI"
                 />
            </xs:complexType>
        </xs:element>
    </xs:choice>
    <xs:attribute name="Id"
        type="long"
        use="optional"
     />
    <xs:attribute name="Path"
        type="anyURI"
        use="optional"
     />
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="fc997-106">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="fc997-106">Child elements</span></span>



| <span data-ttu-id="fc997-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="fc997-107">Element</span></span>                                                    | <span data-ttu-id="fc997-108">Type</span><span class="sxs-lookup"><span data-stu-id="fc997-108">Type</span></span> | <span data-ttu-id="fc997-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="fc997-109">Description</span></span>                                                                                                                                                                            |
|------------------------------------------------------------|------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="fc997-110">**Não**</span><span class="sxs-lookup"><span data-stu-id="fc997-110">**Select**</span></span>](queryschema-select-querytype-element.md)     |      | <span data-ttu-id="fc997-111">Uma consulta XPath que identifica os eventos a serem incluídos no conjunto de resultados da consulta.</span><span class="sxs-lookup"><span data-stu-id="fc997-111">An XPath query that identifies the events to include in the query result set.</span></span> <span data-ttu-id="fc997-112">Especifique o XPath no corpo de texto deste elemento.</span><span class="sxs-lookup"><span data-stu-id="fc997-112">Specify the XPath in the text body of this element.</span></span> <span data-ttu-id="fc997-113">O XPath é limitado a 32 expressões.</span><span class="sxs-lookup"><span data-stu-id="fc997-113">The XPath is limited to 32 expressions.</span></span><br/>   |
| [<span data-ttu-id="fc997-114">**Suprimir**</span><span class="sxs-lookup"><span data-stu-id="fc997-114">**Suppress**</span></span>](queryschema-suppress-querytype-element.md) |      | <span data-ttu-id="fc997-115">Uma consulta XPath que identifica os eventos a serem excluídos do conjunto de resultados da consulta.</span><span class="sxs-lookup"><span data-stu-id="fc997-115">An XPath query that identifies the events to exclude from the query result set.</span></span> <span data-ttu-id="fc997-116">Especifique o XPath no corpo de texto deste elemento.</span><span class="sxs-lookup"><span data-stu-id="fc997-116">Specify the XPath in the text body of this element.</span></span> <span data-ttu-id="fc997-117">O XPath é limitado a 32 expressões.</span><span class="sxs-lookup"><span data-stu-id="fc997-117">The XPath is limited to 32 expressions.</span></span><br/> |



## <a name="attributes"></a><span data-ttu-id="fc997-118">Atributos</span><span class="sxs-lookup"><span data-stu-id="fc997-118">Attributes</span></span>



| <span data-ttu-id="fc997-119">Nome</span><span class="sxs-lookup"><span data-stu-id="fc997-119">Name</span></span> | <span data-ttu-id="fc997-120">Tipo</span><span class="sxs-lookup"><span data-stu-id="fc997-120">Type</span></span>   | <span data-ttu-id="fc997-121">Descrição</span><span class="sxs-lookup"><span data-stu-id="fc997-121">Description</span></span>                                                                                                                                                                                         |
|------|--------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fc997-122">ID</span><span class="sxs-lookup"><span data-stu-id="fc997-122">Id</span></span>   | <span data-ttu-id="fc997-123">long</span><span class="sxs-lookup"><span data-stu-id="fc997-123">long</span></span>   | <span data-ttu-id="fc997-124">Um identificador que identifica exclusivamente essa consulta na lista de consultas.</span><span class="sxs-lookup"><span data-stu-id="fc997-124">An identifier that uniquely identifies this query in your list of queries.</span></span> <span data-ttu-id="fc997-125">O identificador é baseado em zero.</span><span class="sxs-lookup"><span data-stu-id="fc997-125">The identifier is zero-based.</span></span> <span data-ttu-id="fc997-126">Você deve especificar um identificador se sua lista de consulta contiver mais de uma consulta.</span><span class="sxs-lookup"><span data-stu-id="fc997-126">You must specify an identifier if your query list contains more than one query.</span></span><br/> |
| <span data-ttu-id="fc997-127">Caminho</span><span class="sxs-lookup"><span data-stu-id="fc997-127">Path</span></span> | <span data-ttu-id="fc997-128">anyURI</span><span class="sxs-lookup"><span data-stu-id="fc997-128">anyURI</span></span> | <span data-ttu-id="fc997-129">O nome do canal ou o caminho para o arquivo de log que contém os eventos.</span><span class="sxs-lookup"><span data-stu-id="fc997-129">The name of the channel or the path to the log file that contains the events.</span></span><br/>                                                                                                            |
| <span data-ttu-id="fc997-130">Caminho</span><span class="sxs-lookup"><span data-stu-id="fc997-130">Path</span></span> | <span data-ttu-id="fc997-131">anyURI</span><span class="sxs-lookup"><span data-stu-id="fc997-131">anyURI</span></span> | <span data-ttu-id="fc997-132">O nome do canal ou o caminho para o arquivo de log que contém os eventos.</span><span class="sxs-lookup"><span data-stu-id="fc997-132">The name of the channel or the path to the log file that contains the events.</span></span><br/>                                                                                                            |
| <span data-ttu-id="fc997-133">Caminho</span><span class="sxs-lookup"><span data-stu-id="fc997-133">Path</span></span> | <span data-ttu-id="fc997-134">anyURI</span><span class="sxs-lookup"><span data-stu-id="fc997-134">anyURI</span></span> | <span data-ttu-id="fc997-135">Não usado.</span><span class="sxs-lookup"><span data-stu-id="fc997-135">Not used.</span></span><br/>                                                                                                                                                                                |



## <a name="remarks"></a><span data-ttu-id="fc997-136">Comentários</span><span class="sxs-lookup"><span data-stu-id="fc997-136">Remarks</span></span>

<span data-ttu-id="fc997-137">A consulta deve ter pelo menos uma instrução SELECT.</span><span class="sxs-lookup"><span data-stu-id="fc997-137">The query must have at least one select statement.</span></span> <span data-ttu-id="fc997-138">Para cada instrução de supressão, deve haver pelo menos uma instrução SELECT que especifique o mesmo caminho.</span><span class="sxs-lookup"><span data-stu-id="fc997-138">For each suppress statement, there must be at least one select statement that specifies the same path.</span></span> <span data-ttu-id="fc997-139">Se a consulta SELECT e dissupressão retornar os mesmos eventos, a instrução suprimir terá precedência.</span><span class="sxs-lookup"><span data-stu-id="fc997-139">If the select and suppress query return the same events, the suppress statement takes precedence.</span></span> <span data-ttu-id="fc997-140">Se você selecionar eventos de várias fontes, os eventos serão retornados na ordem de carimbo de data/hora.</span><span class="sxs-lookup"><span data-stu-id="fc997-140">If you select events from multiple sources, the events are returned in time stamp order.</span></span> <span data-ttu-id="fc997-141">Se você usar o carimbo de data/hora do sistema e a taxa de eventos for alta, é possível que mais de um evento tenha o mesmo carimbo de data/hora.</span><span class="sxs-lookup"><span data-stu-id="fc997-141">If you use the system time stamp and the rate of events is high, it is possible that more than one event will have the same time stamp.</span></span> <span data-ttu-id="fc997-142">Quando isso ocorre, a ordenação de eventos se torna ambígua e os eventos podem aparecer fora de ordem.</span><span class="sxs-lookup"><span data-stu-id="fc997-142">When this occurs, the ordering of events becomes ambiguous and the events may appear out of order.</span></span>

<span data-ttu-id="fc997-143">Se você especificar um caminho para uma das consultas na lista de consultas, todas as consultas deverão especificar um caminho.</span><span class="sxs-lookup"><span data-stu-id="fc997-143">If you specify a path for one of the queries in the list of queries, all of the queries must specify a path.</span></span> <span data-ttu-id="fc997-144">Se você não especificar um caminho para todas as consultas, deverá especificar o caminho ao chamar a função [**EvtQuery**](/windows/desktop/api/WinEvt/nf-winevt-evtquery) ou [**EvtSubscribe**](/windows/desktop/api/WinEvt/nf-winevt-evtsubscribe) .</span><span class="sxs-lookup"><span data-stu-id="fc997-144">If you do not specify a path for all of the queries, you must specify the path when calling the [**EvtQuery**](/windows/desktop/api/WinEvt/nf-winevt-evtquery) or [**EvtSubscribe**](/windows/desktop/api/WinEvt/nf-winevt-evtsubscribe) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="fc997-145">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fc997-145">Requirements</span></span>



| <span data-ttu-id="fc997-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="fc997-146">Requirement</span></span> | <span data-ttu-id="fc997-147">Valor</span><span class="sxs-lookup"><span data-stu-id="fc997-147">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="fc997-148">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fc997-148">Minimum supported client</span></span><br/> | <span data-ttu-id="fc997-149">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="fc997-149">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="fc997-150">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fc997-150">Minimum supported server</span></span><br/> | <span data-ttu-id="fc997-151">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="fc997-151">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





