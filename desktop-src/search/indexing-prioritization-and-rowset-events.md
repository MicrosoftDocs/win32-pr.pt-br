---
description: Descreve a introdução de priorização de indexação e eventos de conjuntos de linhas para Windows 7.
ms.assetid: 6cdfb7d3-f849-432c-960f-912e5024c583
title: Indexando eventos de priorização e de conjuntos de linhas Windows 7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92491300127c60ebdf2a265583fca77e77a09907b7f42b471f6d3d047a7f6aa4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117680497"
---
# <a name="indexing-prioritization-and-rowset-events-in-windows-7"></a>Indexando eventos de priorização e de conjuntos de linhas Windows 7

Este tópico descreve a introdução de priorização de indexação e eventos de conjuntos de linhas para Windows 7.

Este tópico é organizado da seguinte forma:

-   [Indexando eventos de priorização e de conjuntos de linhas](#indexing-prioritization-and-rowset-events)
    -   [Exemplos de IRowsetPriorization](#irowsetpriorization-examples)
    -   [Eventos IRowsetPrioritization](#indexing-prioritization-and-rowset-events-in-windows-7)
-   [Recursos adicionais](#additional-resources)
-   [Tópicos relacionados](#related-topics)

## <a name="indexing-prioritization-and-rowset-events"></a>Indexando eventos de priorização e de conjuntos de linhas

No Windows 7?e posterior, há uma pilha de prioridade na qual o contexto de qualquer consulta específica, o cliente pode solicitar que os escopos usados nessa consulta sejam priorizados acima do dos itens normais.

Essa pilha de priorização tem as seguintes características:

-   Os itens na pilha podem ter prioridade de primeiro plano, alta ou baixa:
    -   **Primeiro plano:** a lógica de backoff é ignorada e a indexação continua tão rápido quanto o computador permite.
    -   **Alta:** a priorização foi solicitada com o back-off.
    -   **Baixa:** a priorização foi solicitada, não às custas de outros escopos na pilha, mas acima da indexação não priorizada.
-   Qualquer solicitação de prioridade alta ou em primeiro plano eleda a consulta solicitando para o topo da pilha automaticamente.
-   Somente o item na parte superior da pilha pode ter prioridade de primeiro plano.
-   Uma consulta com prioridade de primeiro plano que é elevada em prioridade recebe um evento notificando-o de que ela perdeu a prioridade de primeiro plano e tornou-se uma prioridade alta com o backoff.

A pilha de prioridade define uma prioridade geral dos itens que são processados no indexador da seguinte maneira:

-   As notificações de Alta Prioridade não têm nenhum backoff e normalmente são enviadas apenas para um pequeno número de itens. Por exemplo, Windows Explorer usa essa prioridade para operações de mecanismo de cópia pequenas.
-   A Pilha de Prioridade é a parte superior da pilha, tem o back-off e é a última consulta de prioridade solicitada.
-   Segunda consulta na pilha.
-   Terceira consulta na pilha.
-   Quarta consulta na pilha e assim por diante.
-   Itens de Prioridade Normal.
-   Itens excluídos.
    > [!Note]  
    > Os itens dentro de cada grupo são priorizados internamente por meio da semântica por item mais antiga.

     

### <a name="irowsetpriorization-examples"></a>Exemplos de IRowsetPriorization

A API primária para o trabalho de priorização está disponível por meio da interface a seguir, que pode ser chamada consultando o conjuntos de linhas retornado:


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



A priorização do conjuntos de linhas funciona da seguinte forma:

1.  [**IRowsetPrioritization**](/windows/desktop/api/Searchapi/nn-searchapi-irowsetprioritization) é adquirido com o [Método IUnknown::QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) em um conjuntos de linhas do indexador. **DBPROP \_ ENABLEROWSETEVENTS** deve ser definido como **TRUE** com o método [OLE DB ICommandProperties::SetProperties](/previous-versions/windows/desktop/ms711497(v=vs.85)) antes de executar a consulta para usar a priorização do conjunto de linhas.
2.  [**IRowsetPrioritization::SetScopePriority**](/windows/desktop/api/Searchapi/nf-searchapi-irowsetprioritization-setscopepriority) define a priorização para os escopos que pertencem à consulta e o intervalo em que o evento de estatísticas de escopo é gerado quando há documentos pendentes a serem indexados dentro dos escopos de consulta. Esse evento será gerado se o nível de prioridade estiver definido como padrão.
3.  [**IRowsetPrioritization::GetScopeStatistics**](/windows/desktop/api/Searchapi/nf-searchapi-irowsetprioritization-getscopestatistics) pode ser usado para obter o número de itens indexados no escopo, o número de documentos pendentes a serem adicionados no escopo e o número de documentos que precisam ser indexados dentro desse escopo.

### <a name="irowsetprioritization-events"></a>Eventos IRowsetPrioritization

Há três eventos de conjuntos de linhas [**em IRowsetEvents::OnRowsetEvent**](/windows/desktop/api/Searchapi/nf-searchapi-irowsetevents-onrowsetevent) na [**enumeração ROWSETEVENT \_ TYPE:**](/windows/win32/api/searchapi/ne-searchapi-rowsetevent_type)


```
    // This method allows for future notifications of various actions about your rowset or items within
    // eventType:                               - An identifier of the particular event being sent
    // pVarEventData:                           - The expected value of the EventData for each event type
    //      ROWSETEVENT_TYPE_DATAEXPIRED        - VT_EMPTY
    //      ROWSETEVENT_TYPE_FOREGROUNDLOST     - VT_EMPTY
    //      ROWSETEVENT_TYPE_SCOPESTATISTICS    - VT_VECTOR | VT_UI4 - 3 elements (0 = indexed items, 1 = outstanding adds, 2 = oustanding modifies)

    HRESULT OnRowsetEvent( [in] ROWSETEVENT_TYPE eventType, [in] REFPROPVARIANT eventData );
```



Os eventos de conjuntos de linhas são os seguinte:

-   O **evento \_ \_ DATAEXPIRED DE TIPO ROWSETEVENT** indica que os dados que têm o back-back do conjuntos de linhas expiraram e que um novo conjuntos de linhas deve ser solicitado.
-   O **evento ROWSET \_ TYPE \_ FOREGROUNDLOST** indica que um item que tinha prioridade de primeiro plano na pilha de priorização foi rebaixado, porque outra pessoa se priorizou antes dessa consulta.
-   O **evento ROWSETEVENT \_ TYPE \_ SCOPESTATISTICS** fornece as mesmas informações disponíveis na chamada de método [**IRowsetPrioritization::GetScopeStatistics,**](/windows/desktop/api/Searchapi/nf-searchapi-irowsetprioritization-getscopestatistics) mas por meio de um push push, da seguinte maneira:
    -   O evento surgirá se a API de priorização tiver sido usada para solicitar um nível de priorização não padrão e uma frequência de evento de estatísticas diferente de zero.
    -   O evento surge apenas quando as estatísticas realmente mudam e o intervalo especificado na [**IRowsetPrioritization**](/windows/desktop/api/Searchapi/nn-searchapi-irowsetprioritization) foi decorrido (o intervalo não garante a frequência do evento).
    -   Esse evento tem a garantia de aumentar um estado de "salto zero" (zero itens restantes a serem adicionados, zero modificações restantes), desde que um evento não zero tenha sido gerado.
    -   O indexador pode processar itens sem enviar esse evento, se a fila for esvaziada antes da frequência do evento de estatísticas.

## <a name="additional-resources"></a>Recursos adicionais

Consulte os seguintes recursos relacionados à priorização e conjuntos de linhas:

-   Interfaces:
    -   [**IRowsetEvents**](/windows/desktop/api/Searchapi/nn-searchapi-irowsetevents)
    -   [**IRowsetPrioritization**](/windows/desktop/api/Searchapi/nn-searchapi-irowsetprioritization)
-   Enumerações:
    -   [**PRIORIZAR \_ SINALIZADORES**](/windows/win32/api/searchapi/ne-searchapi-tagprioritize_flags)
    -   [**NÍVEL DE \_ PRIORIDADE**](/windows/win32/api/searchapi/ne-searchapi-priority_level)
    -   [**ROWSETEVENT \_ ITEMSTATE**](/windows/win32/api/searchapi/ne-searchapi-rowsetevent_itemstate)
    -   [**TIPO \_ ROWSETEVENT**](/windows/win32/api/searchapi/ne-searchapi-rowsetevent_type)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Windows 7 Search](./-search-3x-wds-overview.md)
</dt> <dt>

[Novidades da Windows 7 Search](new-for-windows-7-search.md)
</dt> <dt>

[Windows Bibliotecas de shell no Windows 7](-search-win7-development-scenarios.md)
</dt> </dl>

 

 