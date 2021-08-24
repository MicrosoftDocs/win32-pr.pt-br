---
description: Modelo de pull
ms.assetid: b5246dfe-e6ee-4b91-bfe3-2ec8b8723938
title: Modelo de pull
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9832f719e21d85fd09fbf92303e404290d7d99efd6953ace398f77167d0263a1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119747886"
---
# <a name="pull-model"></a>Modelo de pull

Na interface [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) , o filtro upstream determina quais dados enviar e envia os dados para o filtro downstream. Para alguns filtros, um modelo de *pull* é mais apropriado. Aqui, o filtro downstream solicita dados do filtro upstream. Os exemplos ainda viajam downstream, do pino de saída para o pino de entrada, mas o filtro downstream inicia o fluxo de dados. Esse tipo de conexão usa a interface [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) .

O uso típico para o modelo de pull está na reprodução de arquivo. Por exemplo, em um grafo de reprodução AVI, o filtro de [origem de arquivo assíncrono](file-source--async--filter.md) executa operações genéricas de leitura de arquivo e entrega os dados como um fluxo de bytes, sem informações de formato. O filtro [AVI Splitter](avi-splitter-filter.md) lê os cabeçalhos AVI e analisa o fluxo em exemplos de vídeo e áudio. O divisor AVI pode determinar quais dados precisam ser melhores do que o filtro de origem de arquivo assíncrono e, portanto, usa **IAsyncReader** em vez de **IMemInputPin**.

Para solicitar dados do pino de saída, o pino de entrada chama um dos seguintes métodos:

-   [**IAsyncReader:: solicitação**](/windows/desktop/api/Strmif/nf-strmif-iasyncreader-request)
-   [**IAsyncReader::SyncRead**](/windows/desktop/api/Strmif/nf-strmif-iasyncreader-syncread)
-   [**IAsyncReader:: SyncReadAligned**](/windows/desktop/api/Strmif/nf-strmif-iasyncreader-syncreadaligned).

O primeiro método é assíncrono, para dar suporte a várias leituras sobrepostas. Os outros são síncronos.

Teoricamente, qualquer filtro pode dar suporte a **IAsyncReader**, mas, na prática, ele foi projetado para filtros de origem que se conectam a filtros do analisador. O analisador age muito como um filtro de origem no modelo de push. Quando ele pausa, ele cria um thread de streaming que efetua pull de dados da conexão **IAsyncReader** e o envia por push para o downstream. Os Pins de saída usam **IMemInputPin** e o restante do grafo usa o modelo Push padrão.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Flow de dados no filtro Graph](data-flow-in-the-filter-graph.md)
</dt> </dl>

 

 



