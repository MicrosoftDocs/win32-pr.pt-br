---
description: Configurando o relógio do grafo
ms.assetid: 23deab26-6c9a-4f94-b750-11c9b1a14ce3
title: Configurando o relógio do grafo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfe98c8dce1ab5f94664fbe1406c682e5d4e50b8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105779230"
---
# <a name="setting-the-graph-clock"></a>Configurando o relógio do grafo

Quando você cria um gráfico de filtro, o Gerenciador do grafo de filtro escolhe automaticamente um relógio de referência para o grafo. Todos os filtros no grafo são sincronizados com o relógio de referência. Em particular, os filtros de renderização usam o relógio de referência para determinar o tempo de apresentação de cada exemplo.

Normalmente, não há motivo para um aplicativo substituir a opção do relógio de referência do Gerenciador de grafo de filtro. No entanto, você pode fazer isso chamando o método [**IMediaFilter:: Setsincronizate**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-setsyncsource) no Gerenciador do grafo de filtro. Esse método usa um ponteiro para a interface **IReferenceClock** do relógio. Chame o método enquanto o grafo estiver parado.

Se um filtro fornecer um relógio, você poderá obter o ponteiro **IReferenceClock** chamando **QueryInterface** no filtro. Como alternativa, você pode implementar um relógio de referência externa que não é fornecido por um filtro, desde que o relógio externo implemente **IReferenceClock**. O exemplo a seguir mostra como especificar um relógio:


```C++
IGraphBuilder *pGraph = 0;
IReferenceClock *pClock = 0;

CoCreateInstance(CLSID_FilterGraph, NULL, CLSCTX_INPROC_SERVER, 
    IID_IGraphBuilder, (void **)&pGraph);

// Build the graph.
pGraph->RenderFile(L"C:\\Example.avi", 0);

// Create your clock.
hr = CreateMyPrivateClock(&pClock);
if (SUCCEEDED(hr))
{
    // Set the graph clock.
    IMediaFilter *pMediaFilter = 0;
    pGraph->QueryInterface(IID_IMediaFilter, (void**)&pMediaFilter);
    pMediaFilter->SetSyncSource(pClock);
    pClock->Release();
    pMediaFilter->Release();
}
```



Este exemplo pressupõe que CreateMyPrivateClock é uma função definida pelo aplicativo que cria um relógio e retorna um ponteiro **IReferenceClock** .

Você também pode definir o grafo de filtro para ser executado sem nenhum relógio, chamando **Setsincronizate** com o valor **NULL**. Se não houver nenhum relógio, o grafo será executado o mais rápido possível. Sem nenhum relógio, os filtros de processador não aguardam o tempo de apresentação de um exemplo. Em vez disso, eles renderizam cada exemplo assim que chega. Definir o grafo para ser executado sem um relógio será útil se você quiser processar dados rapidamente, em vez de visualizá-los em tempo real.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Tarefas básicas do DirectShow](basic-directshow-tasks.md)
</dt> <dt>

[**Classe CBaseReferenceClock**](cbasereferenceclock.md)
</dt> <dt>

[Tempo e relógios no DirectShow](time-and-clocks-in-directshow.md)
</dt> </dl>

 

 



