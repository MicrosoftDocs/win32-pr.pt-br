---
description: Threads e seções críticas
ms.assetid: e55acb06-03f4-4191-bffe-3196f41ef2c7
title: Threads e seções críticas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d13473a917ae49e80ec658b0d6187fdfdff80c6e3a080a229aca7ccbbe536c1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118651397"
---
# <a name="threads-and-critical-sections"></a>Threads e seções críticas

esta seção descreve a segmentação em filtros de DirectShow e as etapas que você deve seguir para evitar falhas ou deadlocks em um filtro personalizado.

Os exemplos nesta seção usam o pseudocódigo para ilustrar o código que você precisará escrever. eles supõem que um filtro personalizado está usando classes derivadas das classes base DirectShow, da seguinte maneira:

-   CMyInputPin: derivado de [**CBaseInputPin**](cbaseinputpin.md).
-   CMyOutputPin: derivado de [**CBaseOutputPin**](cbaseoutputpin.md).
-   CMyFilter: derivado de [**CBaseFilter**](cbasefilter.md).
-   CMyInputAllocator: o alocador do pino de entrada derivado de [**CMemAllocator**](cmemallocator.md). Nem todo filtro precisa de um alocador personalizado. Para muitos filtros, a classe **CMemAllocator** é suficiente.

Esta seção contém os seguintes tópicos.

-   [Os threads de streaming e aplicativo](the-streaming-and-application-threads.md)
-   [Pausando](pausing.md)
-   [Recebendo e entregando exemplos](receiving-and-delivering-samples.md)
-   [Entregando o fim do fluxo](delivering-the-end-of-stream.md)
-   [Liberando dados](flushing-data.md)
-   [Parando](stopping.md)
-   [Obtendo buffers](getting-buffers.md)
-   [threads de Streaming e o gerenciador de Graph de filtro](streaming-threads-and-the-filter-graph-manager.md)
-   [Resumo do encadeamento de filtro](summary-of-filter-threading.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Flow de dados para os desenvolvedores de filtro](data-flow-for-filter-developers.md)
</dt> <dt>

[gravando filtros de DirectShow](writing-directshow-filters.md)
</dt> </dl>

 

 



