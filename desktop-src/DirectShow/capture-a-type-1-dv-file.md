---
description: Capturar um arquivo DV tipo-1
ms.assetid: fba11e9b-4900-4b29-a0c9-702272cd7387
title: Capturar um arquivo DV tipo-1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8098669f124bdd4c0168e3549cd8eed8e1825c47
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104564955"
---
# <a name="capture-a-type-1-dv-file"></a>Capturar um arquivo DV tipo-1

Um arquivo AVI de tipo 1 DV contém um único fluxo intercalado. Para capturar um arquivo do tipo 1 durante a visualização, use o gráfico de filtro mostrado no diagrama a seguir.

![captura do tipo 1 com visualização](images/dv1-cap.png)

Os filtros neste grafo incluem:

-   O filtro de visões [inteligentes](smart-tee-filter.md) divide o DV intercalado em um fluxo de captura e um fluxo de visualização. Ambos os fluxos contêm os mesmos dados intercalados.
-   O [multiplexador AVI](avi-mux-filter.md) e o [gravador de arquivo](file-writer-filter.md) gravam o fluxo intercalado em disco.
-   O [divisor de DV](dv-splitter-filter.md) divide o fluxo intercalado em um fluxo de vídeo DV e um fluxo de áudio. Ambos os fluxos são renderizados para visualização.
-   O [decodificador de vídeo DV](dv-video-decoder-filter.md) decodifica o fluxo de vídeo DV para visualização.

Compile este grafo da seguinte maneira:


```C++
ICaptureGraphBuilder2 *pBuilder;  // Capture graph builder.
IBaseFilter           *pDV;       // DV capture filter (MSDV)
IBaseFilter           *pAviMux    // Avi Mux filter.

// Initialize pDV (not shown). 
// Create and initialize the Capture Graph Builder (not shown).

// Create the file-writing section of the graph.
hr = pBuilder->SetOutputFileName(&MEDIASUBTYPE_Avi, 
    OLESTR("C:\\Example1.avi"), &pAviMux, 0);

// Render the capture stream.
hr = pBuilder->RenderStream(&PIN_CATEGORY_CAPTURE, &MEDIATYPE_Interleaved, 
    pDV, 0, pAviMux);

// Render the preview stream.
hr = pBuilder->RenderStream(&PIN_CATEGORY_PREVIEW, &MEDIATYPE_Interleaved,
    pDV, 0, 0);

// Remember to release all interfaces.
```



1.  Chame [**ICaptureGraphBuilder2:: SetOutputFileName**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-setoutputfilename) para conectar o filtro AVI Mux ao filtro do gravador de arquivo.
2.  Chame [**ICaptureGraphBuilder2:: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) com a categoria de fixação fixar a \_ captura de categoria \_ para renderizar o fluxo de captura. O construtor do grafo de captura insere automaticamente o filtro de "t inteligente".
3.  Chame RenderStream novamente, mas com a categoria PIN Category de PIN \_ \_ Preview, para renderizar o fluxo de visualização. Ignore esta chamada se não quiser visualizar o vídeo.

Para ambas as chamadas para RenderStream, o tipo de mídia é \_ dicalado de MediaType, o que significa vídeo intercalado em DV. Nesse código, o construtor do grafo de captura adiciona automaticamente cada filtro necessário, exceto para o filtro de captura MSDV.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Vídeo digital no DirectShow](digital-video-in-directshow.md)
</dt> </dl>

 

 



