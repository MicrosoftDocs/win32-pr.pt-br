---
description: Criando um filtro do VMR-9 Graph
ms.assetid: fd83a89c-f1b6-48a3-971e-04ae4ac14c66
title: Criando um filtro do VMR-9 Graph
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c86a76b2d4519299bbd9cde498ccf6a4bc33f0b819d3996faac794154d08c8bb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119689346"
---
# <a name="building-a-vmr-9-filter-graph"></a>Criando um filtro do VMR-9 Graph

Como o filtro de mixagem do vídeo 9 Filter (VMR-9) não é o renderizador de vídeo padrão, um aplicativo que usa o VMR-9 deve adicioná-lo explicitamente ao grafo e conectá-lo. Esta seção apresenta duas abordagens diferentes para a criação de gráficos de filtro com o VMR-9.

usando o construtor de Graph de captura

o construtor de Graph de captura é um objeto auxiliar para criar gráficos de filtro personalizados. Você pode usá-lo para criar gráficos do VMR-9 da seguinte maneira:

1.  crie e inicialize o construtor de Graph de captura, conforme descrito no tópico [sobre o construtor de Graph de captura](about-the-capture-graph-builder.md).
2.  Chame CoCreateInstance para criar o VMR-9:
    ```C++
    IBaseFilter *pVmr = NULL;
    hr = CoCreateInstance(CLSID_VideoMixingRenderer9, 0, 
        CLSCTX_INPROC_SERVER, IID_IBaseFilter, (void**)&pVmr);
    ```

    

3.  chame [**IFilterGraph:: addfilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) no filtro Graph Manager para adicionar o VMR-9 ao grafo de filtro:
    ```C++
    hr = pGraph->AddFilter(pVmr, L"VMR9");
    ```

    

4.  Chame [**IGraphBuilder:: AddSourceFilter**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-addsourcefilter) para adicionar um filtro de origem para o arquivo de vídeo:
    ```C++
    IBaseFilter *pSource;
    hr = pGraph->AddSourceFilter(L"C:\\Example.avi", L"Source1", &pSource);
    ```

    

5.  Chame o método [**ICaptureGraphBuilder2:: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) para renderizar o fluxo de vídeo para o VMR:
    ```C++
    hr = pBuild->RenderStream(0, 0, pSource, 0, pVmr);  
    ```

    

6.  Opcionalmente, chame RenderStream novamente para renderizar o fluxo de áudio:
    ```C++
    hr = pBuild->RenderStream(0, &MEDIATYPE_Audio, pSource, 0, NULL);
    ```

    

Você pode misturar vários fluxos de vídeo chamando AddSourceFilter e RenderStream para cada arquivo de origem.

usando o gerenciador de Graph de filtro

se preferir não usar o construtor de Graph de captura, você poderá criar um grafo do VMR-9 simplesmente usando métodos no Filter Graph Manager, da seguinte maneira:

1.  Crie o VMR-9 e adicione-o ao grafo, conforme mostrado no procedimento anterior.
2.  Use AddSourceFilter para adicionar um filtro de origem para o arquivo de vídeo, conforme mostrado no procedimento anterior.
3.  Se você quiser renderizar o áudio, crie uma instância do filtro de [renderizador DirectSound](directsound-renderer-filter.md) e adicione-o ao grafo de filtro.
4.  Use o método IBaseFilter:: EnumPins para localizar um PIN de saída no filtro de origem. Consulte [enumerando Pins](enumerating-pins.md) para obter detalhes.
5.  consulte o filtro Graph Manager para a interface IFilterGraph2.
6.  Chame [**IFilterGraph2:: RenderEx**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph2-renderex) com o \_ sinalizador am RenderEx \_ RENDERTOEXISTINGRENDERERS. Essa chamada renderiza o pino de saída, usando apenas os filtros de processador que já estão no grafo — nesse caso, o VMR-9 e o renderizador DirectSound. isso impede que a lógica de Conexão inteligente adicione o renderizador de vídeo padrão ao grafo, o que deixaria o VMR-9 desconectado.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[criando gráficos com o construtor de Graph de captura](building-graphs-with-the-capture-graph-builder.md)
</dt> </dl>

 

 



