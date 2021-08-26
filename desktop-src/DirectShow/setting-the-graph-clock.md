---
description: Definindo o Graph relógio
ms.assetid: 23deab26-6c9a-4f94-b750-11c9b1a14ce3
title: Definindo o Graph relógio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ab93fcefe4ba88aa7724bf59b775c493313783b2f4ad3801925e16b9a1818c2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119904136"
---
# <a name="setting-the-graph-clock"></a>Definindo o Graph relógio

Quando você cria um grafo de filtro, o Gerenciador Graph Filtro escolhe automaticamente um relógio de referência para o grafo. Todos os filtros no grafo são sincronizados com o relógio de referência. Em particular, os filtros de renderização usam o relógio de referência para determinar a hora de apresentação de cada amostra.

Normalmente, não há motivo para um aplicativo substituir o filtro Graph opção do relógio de referência do Gerenciador. No entanto, você pode fazer isso chamando o método [**IMediaFilter::SetSyncSource**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-setsyncsource) no Gerenciador Graph Filtro. Esse método leva um ponteiro para a interface **IReferenceClock do** relógio. Chame o método enquanto o grafo é interrompido.

Se um filtro fornece um relógio, você pode obter o ponteiro **IReferenceClock** chamando **QueryInterface** no filtro. Como alternativa, você pode implementar um relógio de referência externo que não é fornecido por um filtro, desde que seu relógio externo implemente **IReferenceClock.** O exemplo a seguir mostra como especificar um relógio:


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



Este exemplo pressuprime que CreateMyPrivateClock é uma função definida pelo aplicativo que cria um relógio e retorna um ponteiro **IReferenceClock.**

Você também pode definir o grafo de filtro para ser executado sem relógio chamando **SetSyncSource** com o valor **NULL**. Se não houver relógio, o grafo será executado o mais rápido possível. Sem relógio, os filtros de renderização não aguardam o tempo de apresentação de um exemplo. Em vez disso, eles renderizarão cada amostra assim que chegar. Definir o grafo para ser executado sem um relógio será útil se você quiser processar dados rapidamente, em vez de visualizar em tempo real.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Tarefas DirectShow básicas](basic-directshow-tasks.md)
</dt> <dt>

[**Classe CBaseReferenceClock**](cbasereferenceclock.md)
</dt> <dt>

[Hora e relógios em DirectShow](time-and-clocks-in-directshow.md)
</dt> </dl>

 

 



