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
# <a name="indexing-prioritization-and-rowset-events-in-windows-7"></a>Priorização de indexação e eventos de conjunto de linhas no Windows 7

Este tópico descreve a introdução da priorização de indexação e eventos de conjunto de linhas para o Windows 7.

Este tópico é organizado da seguinte maneira:

-   [Priorização de indexação e eventos de conjunto de linhas](#indexing-prioritization-and-rowset-events)
    -   [Exemplos de IRowsetPriorization](#irowsetpriorization-examples)
    -   [Eventos de IRowsetPrioritization](#indexing-prioritization-and-rowset-events-in-windows-7)
-   [Recursos adicionais](#additional-resources)
-   [Tópicos relacionados](#related-topics)

## <a name="indexing-prioritization-and-rowset-events"></a>Priorização de indexação e eventos de conjunto de linhas

No Windows 7? e posterior, há uma pilha de prioridade dentro da qual o contexto de qualquer consulta específica, o cliente pode solicitar que os escopos usados nessa consulta sejam priorizados acima dos itens normais.

Essa pilha de priorização tem as seguintes características:

-   Os itens na pilha podem ter prioridade em primeiro plano, alta ou baixa:
    -   **Primeiro plano**: a lógica de retirada é ignorada e a indexação continua tão rápida quanto o computador permite.
    -   **Alta**: a priorização foi solicitada com retirada.
    -   **Baixo**: a priorização foi solicitada, não a despesa de outros escopos na pilha, mas acima da indexação não priorizada.
-   Qualquer solicitação de prioridade alta ou de primeiro plano reduto a consulta solicitante para a parte superior da pilha automaticamente.
-   Somente o item na parte superior da pilha pode ter prioridade de primeiro plano.
-   Uma consulta com prioridade de primeiro plano que é reduzida em prioridade recebe um evento notificando que ele perdeu a prioridade de primeiro plano e se tornou uma prioridade alta com retirada.

A pilha de prioridade define uma prioridade geral dos itens que são processados no indexador da seguinte maneira:

-   As notificações de alta prioridade não têm retirada e normalmente são enviadas apenas para um pequeno número de itens. Por exemplo, o Windows Explorer usa essa prioridade para operações de mecanismo de cópia pequena.
-   A pilha de prioridade é a parte superior da pilha, tem retirada e é a última consulta de prioridade solicitada.
-   Segunda consulta na pilha.
-   Terceira consulta na pilha.
-   Quarta consulta na pilha e assim por diante.
-   Itens de prioridade normais.
-   Itens excluídos.
    > [!Note]  
    > Os itens dentro de cada grupo são priorizados internamente por meio de semânticas por item mais antigas.

     

### <a name="irowsetpriorization-examples"></a>Exemplos de IRowsetPriorization

A API principal para o trabalho de priorização está disponível por meio da interface a seguir, que pode ser chamada consultando o conjunto de linhas retornado:


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



A priorização do conjunto de linhas funciona da seguinte maneira:

1.  [**IRowsetPrioritization**](/windows/desktop/api/Searchapi/nn-searchapi-irowsetprioritization) é adquirido com o [método IUnknown:: QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) em um conjunto de linhas do indexador. **DBPROP \_ ENABLEROWSETEVENTS** deve ser definido como **true** com o método OLE DB [ICommandProperties:: SetProperties](/previous-versions/windows/desktop/ms711497(v=vs.85)) antes de executar a consulta a fim de usar a priorização do conjunto de linhas.
2.  [**IRowsetPrioritization:: SetScopePriority**](/windows/desktop/api/Searchapi/nf-searchapi-irowsetprioritization-setscopepriority) define a priorização para os escopos que pertencem à consulta e o intervalo no qual o evento de estatísticas de escopo é gerado quando há documentos pendentes a serem indexados dentro dos escopos de consulta. Esse evento será gerado se o nível de prioridade for definido como padrão.
3.  [**IRowsetPrioritization:: GetScopeStatistics**](/windows/desktop/api/Searchapi/nf-searchapi-irowsetprioritization-getscopestatistics) pode ser usado para obter o número de itens indexados no escopo, o número de documentos pendentes a serem adicionados no escopo e o número de documentos que precisam ser indexados novamente dentro desse escopo.

### <a name="irowsetprioritization-events"></a>Eventos de IRowsetPrioritization

Há três eventos de conjunto de linhas em [**IRowsetEvents:: OnRowsetEvent**](/windows/desktop/api/Searchapi/nf-searchapi-irowsetevents-onrowsetevent) na enumeração de [**\_ tipo ROWSETEVENT**](/windows/win32/api/searchapi/ne-searchapi-rowsetevent_type) :


```
    // This method allows for future notifications of various actions about your rowset or items within
    // eventType:                               - An identifier of the particular event being sent
    // pVarEventData:                           - The expected value of the EventData for each event type
    //      ROWSETEVENT_TYPE_DATAEXPIRED        - VT_EMPTY
    //      ROWSETEVENT_TYPE_FOREGROUNDLOST     - VT_EMPTY
    //      ROWSETEVENT_TYPE_SCOPESTATISTICS    - VT_VECTOR | VT_UI4 - 3 elements (0 = indexed items, 1 = outstanding adds, 2 = oustanding modifies)

    HRESULT OnRowsetEvent( [in] ROWSETEVENT_TYPE eventType, [in] REFPROPVARIANT eventData );
```



Os eventos do conjunto de linhas são os seguintes:

-   O evento **ROWSETEVENT de \_ tipo \_ dataexpired** indica que os dados que fazem backup do conjunto de linhas expiraram e que um novo conjunto de linhas deve ser solicitado.
-   O evento de **tipo de conjunto de linhas \_ \_ FOREGROUNDLOST** indica que um item que tinha prioridade de primeiro plano na pilha de priorização foi rebaixado, pois outra pessoa priorize a si mesmo à frente dessa consulta.
-   O evento **ROWSETEVENT do \_ tipo \_ SCOPESTATISTICS** fornece as mesmas informações disponíveis na chamada do método [**IRowsetPrioritization:: GetScopeStatistics**](/windows/desktop/api/Searchapi/nf-searchapi-irowsetprioritization-getscopestatistics) , mas por meio de um mecânico de push, da seguinte maneira:
    -   O evento ocorrerá se a API de priorização tiver sido usada para solicitar um nível de priorização não padrão e uma frequência de evento de estatísticas diferente de zero.
    -   O evento surge somente quando as estatísticas realmente mudam e o intervalo especificado no [**IRowsetPrioritization**](/windows/desktop/api/Searchapi/nn-searchapi-irowsetprioritization) expirou (o intervalo não garante a frequência do evento).
    -   Esse evento é garantido para gerar um estado de "Retorno zero" (zero itens restantes a serem adicionados, zero modificações restantes), desde que um evento diferente de zero tenha sido gerado.
    -   O indexador pode processar itens sem enviar esse evento, se a fila for desocupada antes da frequência de eventos de estatísticas.

## <a name="additional-resources"></a>Recursos adicionais

Confira os seguintes recursos relacionados à priorização e aos conjuntos de linhas:

-   Interface
    -   [**IRowsetEvents**](/windows/desktop/api/Searchapi/nn-searchapi-irowsetevents)
    -   [**IRowsetPrioritization**](/windows/desktop/api/Searchapi/nn-searchapi-irowsetprioritization)
-   Enumerações:
    -   [**PRIORIZAr \_ sinalizadores**](/windows/win32/api/searchapi/ne-searchapi-tagprioritize_flags)
    -   [**nível de prioridade \_**](/windows/win32/api/searchapi/ne-searchapi-priority_level)
    -   [**ROWSETEVENT \_ ITEMSTATE**](/windows/win32/api/searchapi/ne-searchapi-rowsetevent_itemstate)
    -   [**tipo de ROWSETEVENT \_**](/windows/win32/api/searchapi/ne-searchapi-rowsetevent_type)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Pesquisa do Windows 7](./-search-3x-wds-overview.md)
</dt> <dt>

[Novo para pesquisa do Windows 7](new-for-windows-7-search.md)
</dt> <dt>

[Bibliotecas de shell do Windows no Windows 7](-search-win7-development-scenarios.md)
</dt> </dl>

 

 