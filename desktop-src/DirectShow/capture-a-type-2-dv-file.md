---
description: Capturar um arquivo DV type-2
ms.assetid: c7d49c86-1b5d-43bf-98a5-78b297682375
title: Capturar um arquivo DV type-2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c944c84ed6cf04ec46de99a209a7b3d2942ae5157bc3ff9d14104da6615d03d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118158733"
---
# <a name="capture-a-type-2-dv-file"></a>Capturar um arquivo DV type-2

Um arquivo DV AVI type-2 tem dois fluxos, um que contém vídeo DV e outro que contém áudio. Para capturar um arquivo type-2 durante a visualização, use o grafo de filtro mostrado no diagrama a seguir.

![captura de tipo 2 com versão prévia](images/dv2-cap.png)

Esse grafo é quase o mesmo que o grafo para captura de tipo 1 (consulte [Capturar um arquivo DV type-1).](capture-a-type-1-dv-file.md) No entanto, o fluxo de captura passa pelo filtro [divisor DV](dv-splitter-filter.md) antes de alcançar o [filtro AVI Mux.](avi-mux-filter.md) Portanto, o AVI Mux recebe dois fluxos, um fluxo de áudio e um fluxo de vídeo codificado em DV.

Crie este grafo da seguinte forma:


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



1.  Crie o divisor DV e adicione-o ao grafo de filtro.
2.  Chame [**ICaptureGraphBuilder2::SetOutputFileName**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-setoutputfilename) para conectar o filtro AVI Mux ao filtro do File Writer.
3.  Chame [**ICaptureGraphBuilder2::RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) para conectar o filtro de captura MSDV ao Divisor dv. Essa chamada também conecta um dos pinos de saída do Divisor de DV ao AVI Mux.
4.  Chame RenderStream novamente para conectar o outro pino do Divisor de DV ao AVI Mux.
5.  Chame RenderStream uma terceira vez para renderizar o fluxo de visualização. Ignore esta etapa se não quiser visualizar o vídeo.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Vídeo digital no DirectShow](digital-video-in-directshow.md)
</dt> </dl>

 

 



