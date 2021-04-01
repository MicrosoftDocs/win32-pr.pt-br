---
description: Capturar um arquivo DV tipo-2
ms.assetid: c7d49c86-1b5d-43bf-98a5-78b297682375
title: Capturar um arquivo DV tipo-2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b919928a4c02ce9e3f3f3e6fcf3d2cd376f880a8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103825547"
---
# <a name="capture-a-type-2-dv-file"></a>Capturar um arquivo DV tipo-2

Um arquivo AVI de tipo 2 DV tem dois fluxos, um que contém vídeo DV e outro que contém áudio. Para capturar um arquivo de tipo 2 durante a visualização, use o gráfico de filtro mostrado no diagrama a seguir.

![captura do tipo 2 com visualização](images/dv2-cap.png)

Esse grafo é quase o mesmo que o grafo para captura de tipo 1 (consulte [capturar um arquivo DV de tipo 1](capture-a-type-1-dv-file.md)). No entanto, o fluxo de captura passa pelo filtro de [Splitter de DV](dv-splitter-filter.md) antes de alcançar o filtro [AVI Mux](avi-mux-filter.md) . Portanto, o AVI Mux recebe dois fluxos, um fluxo de áudio e um fluxo de vídeo codificado em DV.

Compile este grafo da seguinte maneira:


```C++
ICaptureGraphBuilder2 *pBuilder;  // Capture graph builder.
IBaseFilter           *pDV;       // DV capture filter (MSDV)
IBaseFilter           *pAviMux    // Avi Mux filter.
IBaseFilter           *pDVSplit;  // DV Splitter

// Initialize pDV (not shown). 
// Create and initialize the Capture Graph Builder (not shown).

// Create the DV Splitter and add it to the filter graph.
hr = CoCreateInstance(CLSID_DVSplitter, 0, CLSCTX_INPROC_SERVER,
    IID_IBaseFilter, reinterpret_cast<void**>)(&pDVSplit));
hr = pGraph->AddFilter(pDVSplit, L"DV Splitter");

// Create the file-writing section of the graph.
hr = pBuilder->SetOutputFileName(&MEDIASUBTYPE_Avi,
    OLESTR("C:\\Example2.avi"), &pAviMux, 0);

// Connect the capture pin to the DV Splitter, and render one stream from
// the DV Splitter to the AVI Mux. 
hr = pBuilder->RenderStream(&PIN_CATEGORY_CAPTURE, &MEDIATYPE_Interleaved, 
    pDV, pDVSplit, pAviMux);

// Render the other stream from the DV splitter to the AVI Mux.
hr = pBuilder->RenderStream(0, 0, pDVSplit, 0, pAviMux);

// Render the preview stream.
hr = pBuilder->RenderStream(&PIN_CATEGORY_PREVIEW, &MEDIATYPE_Interleaved, 
    pDV, 0, 0);

// Remember to release all interfaces.
```



1.  Crie o divisor de DV e adicione-o ao grafo de filtro.
2.  Chame [**ICaptureGraphBuilder2:: SetOutputFileName**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-setoutputfilename) para conectar o filtro AVI Mux ao filtro do gravador de arquivo.
3.  Chame [**ICaptureGraphBuilder2:: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) para conectar o filtro de captura do MSDV ao divisor de DV. Essa chamada também conecta um dos Pins de saída do separador de DV ao multiplexador AVI.
4.  Chame RenderStream novamente para conectar o outro PIN do divisor de DV ao AVI Mux.
5.  Chame RenderStream uma terceira vez para renderizar o fluxo de visualização. Ignore esta etapa se não quiser visualizar o vídeo.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Vídeo digital no DirectShow](digital-video-in-directshow.md)
</dt> </dl>

 

 



