---
description: Transmitir do arquivo type-1
ms.assetid: 5be2248b-7917-4c1b-9ae7-29e06779eac6
title: Transmitir do arquivo type-1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e62ce67627c350c24de1bf1ee96ba7804ac3f164264e167498c597e8136ea138
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119015524"
---
# <a name="transmit-from-type-1-file"></a>Transmitir do arquivo type-1

Para transmitir um arquivo type-1 durante a visualização do arquivo, use o grafo de filtro mostrado no diagrama a seguir.

![type-1 transmit with preview](images/dv1-transmit.png)

Os filtros neste grafo incluem:

-   O [divisor AVI](avi-splitter-filter.md) analisará o arquivo AVI. Para um arquivo DV type-1, o pino de saída fornece exemplos de DV intercalados.
-   O [filtro Infinite Pin Tee](infinite-pin-tee-filter.md) divide o DV intercalado em um fluxo de transmissão e em um fluxo de visualização. Ambos os fluxos contêm os mesmos dados intercalados. (Esse grafo usa o Pin Infinito Tee em vez do [Smart Tee,](smart-tee-filter.md)porque não há nenhum risco de soltar quadros ao ler de um arquivo, como há com a captura ao vivo.)
-   O [Divisor](dv-splitter-filter.md) de DV divide o fluxo intercalado em um fluxo de vídeo DV, que é decodificado pelo [Decodificador](dv-video-decoder-filter.md)de Vídeo DV e um fluxo de áudio. Ambos os fluxos são renderados para visualização.

Crie este grafo da seguinte forma:


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



1.  Chame [**IGraphBuilder::AddSourceFilter para**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-addsourcefilter) adicionar o filtro de origem ao grafo de filtro.
2.  Crie o Divisor AVI e o Pin Infinito Tee e adicione-os ao grafo.
3.  Chame [**ICaptureGraphBuilder2::RenderStream para**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) conectar o filtro de origem ao Divisor AVI. Especificando MEDIATYPE Intercalado para garantir que o método falhe se o arquivo de origem não for um arquivo DV do tipo \_ 1. Nesse caso, você pode fazer o back-out e tentar criar um grafo de transmissão do tipo 2.
4.  Chame **RenderStream novamente** para rotear o fluxo intercalado do divisor AVI para o Pin Infinito
5.  Chame RenderStream uma terceira vez para rotear um fluxo do Pin Infinito Tee para o filtro MSDV, para transmissão para o dispositivo.
6.  Chame **RenderStream** uma última vez para criar a seção de visualização do grafo.

Se você não quiser visualizar, basta conectar a origem do arquivo ao filtro MSDV:


```C++
hr = pBuilder->RenderStream(0, &MEDIATYPE_Interleaved, pFileSource, 0, pDV);
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Vídeo digital no DirectShow](digital-video-in-directshow.md)
</dt> </dl>

 

 



