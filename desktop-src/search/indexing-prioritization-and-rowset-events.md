---
description: Descreve a introdução da priorização de indexação e eventos de conjunto de linhas para o Windows 7.
ms.assetid: 6cdfb7d3-f849-432c-960f-912e5024c583
title: Priorização de indexação e eventos de conjunto de linhas no Windows 7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6610500a3c2fcd359f346e5239507fb15ad896d
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/10/2021
ms.locfileid: "105766290"
---
# <a name="indexing-prioritization-and-rowset-events-in-windows-7"></a><span data-ttu-id="70026-103">Priorização de indexação e eventos de conjunto de linhas no Windows 7</span><span class="sxs-lookup"><span data-stu-id="70026-103">Indexing Prioritization and Rowset Events in Windows 7</span></span>

<span data-ttu-id="70026-104">Este tópico descreve a introdução da priorização de indexação e eventos de conjunto de linhas para o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="70026-104">This topic outlines the introduction of indexing prioritization and rowset events for Windows 7.</span></span>

<span data-ttu-id="70026-105">Este tópico é organizado da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="70026-105">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="70026-106">Priorização de indexação e eventos de conjunto de linhas</span><span class="sxs-lookup"><span data-stu-id="70026-106">Indexing Prioritization and Rowset Events</span></span>](#indexing-prioritization-and-rowset-events)
    -   [<span data-ttu-id="70026-107">Exemplos de IRowsetPriorization</span><span class="sxs-lookup"><span data-stu-id="70026-107">IRowsetPriorization Examples</span></span>](#irowsetpriorization-examples)
    -   [<span data-ttu-id="70026-108">Eventos de IRowsetPrioritization</span><span class="sxs-lookup"><span data-stu-id="70026-108">IRowsetPrioritization Events</span></span>](#indexing-prioritization-and-rowset-events-in-windows-7)
-   [<span data-ttu-id="70026-109">Recursos adicionais</span><span class="sxs-lookup"><span data-stu-id="70026-109">Additional Resources</span></span>](#additional-resources)
-   [<span data-ttu-id="70026-110">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="70026-110">Related topics</span></span>](#related-topics)

## <a name="indexing-prioritization-and-rowset-events"></a><span data-ttu-id="70026-111">Priorização de indexação e eventos de conjunto de linhas</span><span class="sxs-lookup"><span data-stu-id="70026-111">Indexing Prioritization and Rowset Events</span></span>

<span data-ttu-id="70026-112">No Windows 7? e posterior, há uma pilha de prioridade dentro da qual o contexto de qualquer consulta específica, o cliente pode solicitar que os escopos usados nessa consulta sejam priorizados acima dos itens normais.</span><span class="sxs-lookup"><span data-stu-id="70026-112">In Windows 7?and later, there is a priority stack within which the context of any particular query, the client can request that the scopes used in that query be prioritized above that of normal items.</span></span>

<span data-ttu-id="70026-113">Essa pilha de priorização tem as seguintes características:</span><span class="sxs-lookup"><span data-stu-id="70026-113">This prioritization stack has the following characteristics:</span></span>

-   <span data-ttu-id="70026-114">Os itens na pilha podem ter prioridade em primeiro plano, alta ou baixa:</span><span class="sxs-lookup"><span data-stu-id="70026-114">Items in the stack can have foreground, high, or low priority:</span></span>
    -   <span data-ttu-id="70026-115">**Primeiro plano**: a lógica de retirada é ignorada e a indexação continua tão rápida quanto o computador permite.</span><span class="sxs-lookup"><span data-stu-id="70026-115">**Foreground**: Backoff logic is skipped and indexing proceeds as fast as the machine allows.</span></span>
    -   <span data-ttu-id="70026-116">**Alta**: a priorização foi solicitada com retirada.</span><span class="sxs-lookup"><span data-stu-id="70026-116">**High**: Prioritization has been requested with backoff.</span></span>
    -   <span data-ttu-id="70026-117">**Baixo**: a priorização foi solicitada, não a despesa de outros escopos na pilha, mas acima da indexação não priorizada.</span><span class="sxs-lookup"><span data-stu-id="70026-117">**Low**: Prioritization has been requested, not at the expense of other scopes on the stack, but above non-prioritized indexing.</span></span>
-   <span data-ttu-id="70026-118">Qualquer solicitação de prioridade alta ou de primeiro plano reduto a consulta solicitante para a parte superior da pilha automaticamente.</span><span class="sxs-lookup"><span data-stu-id="70026-118">Any request for high or foreground priority bumps the requesting query to the top of the stack automatically.</span></span>
-   <span data-ttu-id="70026-119">Somente o item na parte superior da pilha pode ter prioridade de primeiro plano.</span><span class="sxs-lookup"><span data-stu-id="70026-119">Only the item on top of the stack can have foreground priority.</span></span>
-   <span data-ttu-id="70026-120">Uma consulta com prioridade de primeiro plano que é reduzida em prioridade recebe um evento notificando que ele perdeu a prioridade de primeiro plano e se tornou uma prioridade alta com retirada.</span><span class="sxs-lookup"><span data-stu-id="70026-120">A query with foreground priority that is bumped down in priority receives an event notifying it that it has lost foreground priority and has become a high priority with backoff.</span></span>

<span data-ttu-id="70026-121">A pilha de prioridade define uma prioridade geral dos itens que são processados no indexador da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="70026-121">The priority stack sets an overall priority of items that are processed in the indexer as follows:</span></span>

-   <span data-ttu-id="70026-122">As notificações de alta prioridade não têm retirada e normalmente são enviadas apenas para um pequeno número de itens.</span><span class="sxs-lookup"><span data-stu-id="70026-122">High Priority notifications have no backoff, and are typically sent only for a small number of items.</span></span> <span data-ttu-id="70026-123">Por exemplo, o Windows Explorer usa essa prioridade para operações de mecanismo de cópia pequena.</span><span class="sxs-lookup"><span data-stu-id="70026-123">For example, Windows Explorer uses this priority for small copy engine operations.</span></span>
-   <span data-ttu-id="70026-124">A pilha de prioridade é a parte superior da pilha, tem retirada e é a última consulta de prioridade solicitada.</span><span class="sxs-lookup"><span data-stu-id="70026-124">Priority Stack is top of the stack, has backoff, and is the last requested priority query.</span></span>
-   <span data-ttu-id="70026-125">Segunda consulta na pilha.</span><span class="sxs-lookup"><span data-stu-id="70026-125">Second query in the stack.</span></span>
-   <span data-ttu-id="70026-126">Terceira consulta na pilha.</span><span class="sxs-lookup"><span data-stu-id="70026-126">Third query in the stack.</span></span>
-   <span data-ttu-id="70026-127">Quarta consulta na pilha e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="70026-127">Fourth query in the stack, and so forth.</span></span>
-   <span data-ttu-id="70026-128">Itens de prioridade normais.</span><span class="sxs-lookup"><span data-stu-id="70026-128">Normal Priority items.</span></span>
-   <span data-ttu-id="70026-129">Itens excluídos.</span><span class="sxs-lookup"><span data-stu-id="70026-129">Deleted items.</span></span>
    > [!Note]  
    > <span data-ttu-id="70026-130">Os itens dentro de cada grupo são priorizados internamente por meio de semânticas por item mais antigas.</span><span class="sxs-lookup"><span data-stu-id="70026-130">Items within each group are prioritized internally through the older per-item semantics.</span></span>

     

### <a name="irowsetpriorization-examples"></a><span data-ttu-id="70026-131">Exemplos de IRowsetPriorization</span><span class="sxs-lookup"><span data-stu-id="70026-131">IRowsetPriorization Examples</span></span>

<span data-ttu-id="70026-132">A API principal para o trabalho de priorização está disponível por meio da interface a seguir, que pode ser chamada consultando o conjunto de linhas retornado:</span><span class="sxs-lookup"><span data-stu-id="70026-132">The primary API for prioritization work is available through the following interface, which can be called by querying the returned rowset:</span></span>


```
typedef [v1_enum] enum
{
    PRIORITY_LEVEL_FOREGROUND           = 0,    // process items in the scope first as quickly as possible
    PRIORITY_LEVEL_HIGH                 = 1,    // process items in the scope first at the normal rate
    PRIORITY_LEVEL_LOW                  = 2,    // process items in this scope before those at the normal rate, but after any other prioritization requests
    PRIORITY_LEVEL_DEFAULT              = 3     // process items at the normal indexer rate
} PRIORITY_LEVEL;


[
    object,
    uuid(IRowsetPrioritization_GUID),
    pointer_default(unique)
]
interface IRowsetPrioritization : IUnknown
{
    // Sets or retrieves the current indexer prioritization level for the scope specified by
    // this query.

    HRESULT SetScopePriority( [in] PRIORITY_LEVEL priority, [in] DWORD scopeStatisticsEventFrequency );
    HRESULT GetScopePriority( [out] PRIORITY_LEVEL * priority, [out] DWORD * scopeStatisticsEventFrequency );

    // Gets information describing the scope specified by this query:
    // indexedDocumentCount     -   The total number of documents currently indexed in the scope
    // oustandingAddCount       -   The total number of documents yet to be indexed in the scope (those not yet included in indexedDocumentCount)
    // oustandingModifyCount    -   The total number of documents indexed in the scope that need to be re-indexed (included in indexedDocumentCount)
    
    HRESULT GetScopeStatistics( [out] DWORD * indexedDocumentCount, [out] DWORD * oustandingAddCount, [out] DWORD * oustandingModifyCount );
};
```



<span data-ttu-id="70026-133">A priorização do conjunto de linhas funciona da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="70026-133">Rowset prioritization works as follows:</span></span>

1.  <span data-ttu-id="70026-134">[**IRowsetPrioritization**](/windows/desktop/api/Searchapi/nn-searchapi-irowsetprioritization) é adquirido com o [método IUnknown:: QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) em um conjunto de linhas do indexador.</span><span class="sxs-lookup"><span data-stu-id="70026-134">[**IRowsetPrioritization**](/windows/desktop/api/Searchapi/nn-searchapi-irowsetprioritization) is acquired with [IUnknown::QueryInterface Method](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) on an indexer rowset.</span></span> <span data-ttu-id="70026-135">**DBPROP \_ ENABLEROWSETEVENTS** deve ser definido como **true** com o método OLE DB [ICommandProperties:: SetProperties](/previous-versions/windows/desktop/ms711497(v=vs.85)) antes de executar a consulta a fim de usar a priorização do conjunto de linhas.</span><span class="sxs-lookup"><span data-stu-id="70026-135">**DBPROP\_ENABLEROWSETEVENTS** must be set to **TRUE** with the OLE DB [ICommandProperties::SetProperties](/previous-versions/windows/desktop/ms711497(v=vs.85)) method prior to executing the query in order to use rowset prioritization.</span></span>
2.  <span data-ttu-id="70026-136">[**IRowsetPrioritization:: SetScopePriority**](/windows/desktop/api/Searchapi/nf-searchapi-irowsetprioritization-setscopepriority) define a priorização para os escopos que pertencem à consulta e o intervalo no qual o evento de estatísticas de escopo é gerado quando há documentos pendentes a serem indexados dentro dos escopos de consulta.</span><span class="sxs-lookup"><span data-stu-id="70026-136">[**IRowsetPrioritization::SetScopePriority**](/windows/desktop/api/Searchapi/nf-searchapi-irowsetprioritization-setscopepriority) sets the prioritization for the scopes belonging to the query, and the interval the scope statistics event is raised when there are outstanding documents to be indexed within the query scopes.</span></span> <span data-ttu-id="70026-137">Esse evento será gerado se o nível de prioridade for definido como padrão.</span><span class="sxs-lookup"><span data-stu-id="70026-137">This event is raised if the priority level is set to default.</span></span>
3.  <span data-ttu-id="70026-138">[**IRowsetPrioritization:: GetScopeStatistics**](/windows/desktop/api/Searchapi/nf-searchapi-irowsetprioritization-getscopestatistics) pode ser usado para obter o número de itens indexados no escopo, o número de documentos pendentes a serem adicionados no escopo e o número de documentos que precisam ser indexados novamente dentro desse escopo.</span><span class="sxs-lookup"><span data-stu-id="70026-138">[**IRowsetPrioritization::GetScopeStatistics**](/windows/desktop/api/Searchapi/nf-searchapi-irowsetprioritization-getscopestatistics) can be used to get the number of indexed items in the scope, the number of outstanding documents to be added in the scope, and the number of documents that need to be re-indexed within this scope.</span></span>

### <a name="irowsetprioritization-events"></a><span data-ttu-id="70026-139">Eventos de IRowsetPrioritization</span><span class="sxs-lookup"><span data-stu-id="70026-139">IRowsetPrioritization Events</span></span>

<span data-ttu-id="70026-140">Há três eventos de conjunto de linhas em [**IRowsetEvents:: OnRowsetEvent**](/windows/desktop/api/Searchapi/nf-searchapi-irowsetevents-onrowsetevent) na enumeração de [**\_ tipo ROWSETEVENT**](/windows/win32/api/searchapi/ne-searchapi-rowsetevent_type) :</span><span class="sxs-lookup"><span data-stu-id="70026-140">There are three rowset events in [**IRowsetEvents::OnRowsetEvent**](/windows/desktop/api/Searchapi/nf-searchapi-irowsetevents-onrowsetevent) in the [**ROWSETEVENT\_TYPE**](/windows/win32/api/searchapi/ne-searchapi-rowsetevent_type) enumeration:</span></span>


```
    // This method allows for future notifications of various actions about your rowset or items within
    // eventType:                               - An identifier of the particular event being sent
    // pVarEventData:                           - The expected value of the EventData for each event type
    //      ROWSETEVENT_TYPE_DATAEXPIRED        - VT_EMPTY
    //      ROWSETEVENT_TYPE_FOREGROUNDLOST     - VT_EMPTY
    //      ROWSETEVENT_TYPE_SCOPESTATISTICS    - VT_VECTOR | VT_UI4 - 3 elements (0 = indexed items, 1 = outstanding adds, 2 = oustanding modifies)

    HRESULT OnRowsetEvent( [in] ROWSETEVENT_TYPE eventType, [in] REFPROPVARIANT eventData );
```



<span data-ttu-id="70026-141">Os eventos do conjunto de linhas são os seguintes:</span><span class="sxs-lookup"><span data-stu-id="70026-141">The rowset events are as follows:</span></span>

-   <span data-ttu-id="70026-142">O evento **ROWSETEVENT de \_ tipo \_ dataexpired** indica que os dados que fazem backup do conjunto de linhas expiraram e que um novo conjunto de linhas deve ser solicitado.</span><span class="sxs-lookup"><span data-stu-id="70026-142">The **ROWSETEVENT\_TYPE\_DATAEXPIRED** event indicates that data backing the rowset has expired, and that a new rowset should be requested.</span></span>
-   <span data-ttu-id="70026-143">O evento de **tipo de conjunto de linhas \_ \_ FOREGROUNDLOST** indica que um item que tinha prioridade de primeiro plano na pilha de priorização foi rebaixado, pois outra pessoa priorize a si mesmo à frente dessa consulta.</span><span class="sxs-lookup"><span data-stu-id="70026-143">The **ROWSET\_TYPE\_FOREGROUNDLOST** event indicates that an item that did have foreground priority in the prioritization stack has been demoted, because someone else prioritized themselves ahead of this query.</span></span>
-   <span data-ttu-id="70026-144">O evento **ROWSETEVENT do \_ tipo \_ SCOPESTATISTICS** fornece as mesmas informações disponíveis na chamada do método [**IRowsetPrioritization:: GetScopeStatistics**](/windows/desktop/api/Searchapi/nf-searchapi-irowsetprioritization-getscopestatistics) , mas por meio de um mecânico de push, da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="70026-144">The **ROWSETEVENT\_TYPE\_SCOPESTATISTICS** event gives you the same information available from the [**IRowsetPrioritization::GetScopeStatistics**](/windows/desktop/api/Searchapi/nf-searchapi-irowsetprioritization-getscopestatistics) method call, but through a push mechanic, as follows:</span></span>
    -   <span data-ttu-id="70026-145">O evento ocorrerá se a API de priorização tiver sido usada para solicitar um nível de priorização não padrão e uma frequência de evento de estatísticas diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="70026-145">The event arises if the prioritization API has been used to request a non-default prioritization level, and a non-zero statistics event frequency.</span></span>
    -   <span data-ttu-id="70026-146">O evento surge somente quando as estatísticas realmente mudam e o intervalo especificado no [**IRowsetPrioritization**](/windows/desktop/api/Searchapi/nn-searchapi-irowsetprioritization) expirou (o intervalo não garante a frequência do evento).</span><span class="sxs-lookup"><span data-stu-id="70026-146">The event arises only when statistics actually change, and the interval specified in the [**IRowsetPrioritization**](/windows/desktop/api/Searchapi/nn-searchapi-irowsetprioritization) has elapsed (the interval does not guarantee the frequency of the event).</span></span>
    -   <span data-ttu-id="70026-147">Esse evento é garantido para gerar um estado de "Retorno zero" (zero itens restantes a serem adicionados, zero modificações restantes), desde que um evento diferente de zero tenha sido gerado.</span><span class="sxs-lookup"><span data-stu-id="70026-147">This event is guaranteed to raise a "bounce zero" state (zero items remaining to be added, zero modifies remaining), provided that a non-zero event has been raised.</span></span>
    -   <span data-ttu-id="70026-148">O indexador pode processar itens sem enviar esse evento, se a fila for desocupada antes da frequência de eventos de estatísticas.</span><span class="sxs-lookup"><span data-stu-id="70026-148">The indexer may process items without sending this event, if the queue empties before the statistics event frequency.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="70026-149">Recursos adicionais</span><span class="sxs-lookup"><span data-stu-id="70026-149">Additional Resources</span></span>

<span data-ttu-id="70026-150">Confira os seguintes recursos relacionados à priorização e aos conjuntos de linhas:</span><span class="sxs-lookup"><span data-stu-id="70026-150">See the following resources related to prioritization and rowsets:</span></span>

-   <span data-ttu-id="70026-151">Interface</span><span class="sxs-lookup"><span data-stu-id="70026-151">Interfaces:</span></span>
    -   [<span data-ttu-id="70026-152">**IRowsetEvents**</span><span class="sxs-lookup"><span data-stu-id="70026-152">**IRowsetEvents**</span></span>](/windows/desktop/api/Searchapi/nn-searchapi-irowsetevents)
    -   [<span data-ttu-id="70026-153">**IRowsetPrioritization**</span><span class="sxs-lookup"><span data-stu-id="70026-153">**IRowsetPrioritization**</span></span>](/windows/desktop/api/Searchapi/nn-searchapi-irowsetprioritization)
-   <span data-ttu-id="70026-154">Enumerações:</span><span class="sxs-lookup"><span data-stu-id="70026-154">Enumerations:</span></span>
    -   [<span data-ttu-id="70026-155">**PRIORIZAr \_ sinalizadores**</span><span class="sxs-lookup"><span data-stu-id="70026-155">**PRIORITIZE\_FLAGS**</span></span>](/windows/win32/api/searchapi/ne-searchapi-tagprioritize_flags)
    -   [<span data-ttu-id="70026-156">**nível de prioridade \_**</span><span class="sxs-lookup"><span data-stu-id="70026-156">**PRIORITY\_LEVEL**</span></span>](/windows/win32/api/searchapi/ne-searchapi-priority_level)
    -   [<span data-ttu-id="70026-157">**ROWSETEVENT \_ ITEMSTATE**</span><span class="sxs-lookup"><span data-stu-id="70026-157">**ROWSETEVENT\_ITEMSTATE**</span></span>](/windows/win32/api/searchapi/ne-searchapi-rowsetevent_itemstate)
    -   [<span data-ttu-id="70026-158">**tipo de ROWSETEVENT \_**</span><span class="sxs-lookup"><span data-stu-id="70026-158">**ROWSETEVENT\_TYPE**</span></span>](/windows/win32/api/searchapi/ne-searchapi-rowsetevent_type)

## <a name="related-topics"></a><span data-ttu-id="70026-159">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="70026-159">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="70026-160">Pesquisa do Windows 7</span><span class="sxs-lookup"><span data-stu-id="70026-160">Windows 7 Search</span></span>](./-search-3x-wds-overview.md)
</dt> <dt>

[<span data-ttu-id="70026-161">Novo para pesquisa do Windows 7</span><span class="sxs-lookup"><span data-stu-id="70026-161">New for Windows 7 Search</span></span>](new-for-windows-7-search.md)
</dt> <dt>

[<span data-ttu-id="70026-162">Bibliotecas de shell do Windows no Windows 7</span><span class="sxs-lookup"><span data-stu-id="70026-162">Windows Shell Libraries in Windows 7</span></span>](-search-win7-development-scenarios.md)
</dt> </dl>

 

 