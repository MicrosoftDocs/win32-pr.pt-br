---
description: Transmitir do arquivo do tipo-1
ms.assetid: 5be2248b-7917-4c1b-9ae7-29e06779eac6
title: Transmitir do arquivo do tipo-1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74e38ed3e549b6cd671248ba1df9b24df8fbfe3e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011170"
---
# <a name="transmit-from-type-1-file"></a>Transmitir do arquivo do tipo-1

Para transmitir um arquivo do tipo 1 durante a visualização do arquivo, use o gráfico de filtro mostrado no diagrama a seguir.

![tipo-1 transmissão com visualização](images/dv1-transmit.png)

Os filtros neste grafo incluem:

-   O [divisor AVI](avi-splitter-filter.md) analisa o arquivo avi. Para um arquivo DV tipo-1, o pino de saída entrega exemplos de DV intercalados.
-   O filtro de [t de PIN infinito](infinite-pin-tee-filter.md) divide o DV intercalado em um fluxo de transmissão e um fluxo de visualização. Ambos os fluxos contêm os mesmos dados intercalados. (Esse grafo usa o "t" de PIN infinito, em vez do ativo [inteligente](smart-tee-filter.md), porque não há nenhum risco de descartar quadros ao ler de um arquivo, pois há com a captura dinâmica.)
-   O [divisor de DV](dv-splitter-filter.md) divide o fluxo intercalado em um fluxo de vídeo DV, que é decodificado pelo [codificador de vídeo DV](dv-video-decoder-filter.md)e um fluxo de áudio. Ambos os fluxos são renderizados para visualização.

Compile este grafo da seguinte maneira:


```C++
ICaptureGraphBuilder2 *pBuilder;  // Capture graph builder.
IBaseFilter           *pDV;       // DV capture filter (MSDV)

// Initialize pDV (not shown). 
// Create and initialize the Capture Graph Builder (not shown).

// Add the Infinite Pin Tee filter to the graph.
IBaseFilter *pTee;
hr = CoCreateInstance(CLSID_InfTee, 0, CLSCTX_INPROC_SERVER
    IID_IBaseFilter, reinterpret_cast<void**>)(&pTee));
hr = pGraph->AddFilter(pTee, L"Tee");

// Add the File Source filter to the graph.
IBaseFilter *pFileSource;
hr = pGraph->AddSourceFilter(
    L"C:\\YourFileNameHere.avi",
    L"Source", 
    &pFileSource);

// Add the AVI Splitter filter to the graph.
IBaseFilter *pAviSplit;
hr = CoCreateInstance(CLSID_AviSplitter, 0, CLSCTX_INPROC_SERVER
    IID_IBaseFilter, reinterpret_cast<void**>)(&pAviSplit));
hr = pGraph->AddFilter(pAviSplit, L"AVI Splitter");

// Connect the file source to the AVI Splitter.
hr = pBuilder->RenderStream(0, 0, pFileSource, 0, pAviSplit);
if (FAILED(hr))
{
    // This is not an AVI file. 
}

// Connect the file source to the Infinite Pin Tee.
hr = pBuilder->RenderStream(0, &MEDIATYPE_Interleaved, pAviSplit, 0, pTee);
if (FAILED(hr))
{
    // This is not a type-1 DV file.
}

// Render one stream from the Infinite Pin Tee to MSDV, for transmit.
hr = pBuilder->RenderStream(0, 0, pTee, 0, pDV);

// Render another stream from the Infinite Pin Tee for preview.
hr = pBuilder->RenderStream(0, 0, pTee, 0, 0);
```



1.  Chame [**IGraphBuilder:: AddSourceFilter**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-addsourcefilter) para adicionar o filtro de origem ao grafo de filtro.
2.  Crie o separador AVI e o "t" de PIN infinito e adicione-os ao grafo.
3.  Chame [**ICaptureGraphBuilder2:: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) para conectar o filtro de origem ao divisor avi. Especificar MEDIATYPE \_ intercalado para garantir que o método falhe se o arquivo de origem não for um arquivo DV tipo-1. Nesse caso, você pode fazer backup e tentar criar um grafo de transmissão tipo 2 em vez disso.
4.  Chame **RenderStream** novamente para rotear o fluxo intercalado do separador AVI para o "t" de PIN infinito
5.  Chame o RenderStream uma terceira vez para rotear um fluxo do "t" de PIN infinito para o filtro MSDV, para transmitir para o dispositivo.
6.  Chame **RenderStream** uma última vez para criar a seção de visualização do grafo.

Se você não quiser a visualização, basta conectar a origem do arquivo ao filtro MSDV:


```C++
hr = pBuilder->RenderStream(0, &MEDIATYPE_Interleaved, pFileSource, 0, pDV);
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Vídeo digital no DirectShow](digital-video-in-directshow.md)
</dt> </dl>

 

 



