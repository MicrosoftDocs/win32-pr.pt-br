---
description: Transmitir do arquivo do tipo 2
ms.assetid: c14c1798-aeff-44d8-a2e4-2fe4c146dfb9
title: Transmitir do arquivo do tipo 2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96e15cb0b3aae5b5119739f327a84204730c9d05
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103921921"
---
# <a name="transmit-from-type-2-file"></a>Transmitir do arquivo do tipo 2

Para transmitir um arquivo de tipo 2 durante a visualização, use o gráfico de filtro mostrado no diagrama a seguir.

![transmissão de tipo 2 com visualização](images/dv2-transmit.png)

Um arquivo tipo 2 tem dois fluxos, um fluxo de áudio e um fluxo de vídeo codificado por DV. Esse grafo usa o filtro [DV Muxer](dv-muxer-filter.md) para combinar os fluxos de áudio e vídeo. Ele envia o fluxo intercalado para o filtro MSDV, mas divide o fluxo novamente para visualização.

Compile este grafo da seguinte maneira:


```C++
// Add the DV Mux filter to the graph.
IBaseFilter *pDVMux;
hr = CoCreateInstance(CLSID_DVMux, 0, CLSCTX_INPROC_SERVER
    IID_IBaseFilter, reinterpret_cast<void**>)(&pDVMux));
hr = pGraph->AddFilter(pDVMux, L"DV Mux");

// Add the File Source filter to the graph.
IBaseFilter *pFileSource;
hr = pGraph->AddSourceFilter(L"C:\\Example2.avi", L"Source", 
    &pFileSource);

hr = pBuilder->RenderStream(0, 0, pFileSource, 0, pDVMux);
hr = pBuilder->RenderStream(0, 0, pFileSource, 0, pDVMux);

// Add the Infinite Pin Tee filter to the graph.
IBaseFilter *pTee;
hr = CoCreateInstance(CLSID_InfTee, 0, CLSCTX_INPROC_SERVER
    IID_IBaseFilter, reinterpret_cast<void**>)(&pTee));
hr = pGraph->AddFilter(pTee, L"Tee");

hr = pBuilder->RenderStream(0, 0, pDVMux, 0, pTee);
hr = pBuilder->RenderStream(0, 0, pTee, 0, pDV);
hr = pBuilder->RenderStream(0, &MEDIATYPE_Interleaved, pTee, 0, 0);
```



Esse código faz várias chamadas para **RenderStream**:

Os dois primeiros conectam o filtro de origem ao divisor AVI e ao divisor AVI ao MUX DV. Na primeira chamada, o construtor do grafo de captura adiciona automaticamente o divisor AVI ao grafo e conecta um dos pinos de saída do divisor AVI ao MUX DV. Na segunda chamada, o construtor do grafo de captura localiza o segundo pino de saída do divisor AVI e conecta-o ao MUX DV.

A terceira chamada para **RenderStream** conecta o Muxer DV ao filtro de t de PIN infinito. A próxima chamada conecta um fluxo do "t" de PIN infinito ao filtro de captura MSDV. Esse fluxo é transmitido para o dispositivo. A última chamada para **RenderStream** compila a seção de visualização do grafo.

Se você não quiser Visualizar durante a transmissão, poderá omitir o "t" de PIN infinito e simplesmente conectar o MUX DV ao filtro MSDV:


```C++
hr = pBuilder->RenderStream(0, 0, pDVMux, 0, pDV);
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Vídeo digital no DirectShow](digital-video-in-directshow.md)
</dt> </dl>

 

 



