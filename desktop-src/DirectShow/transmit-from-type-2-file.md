---
description: Transmitir do arquivo Type-2
ms.assetid: c14c1798-aeff-44d8-a2e4-2fe4c146dfb9
title: Transmitir do arquivo Type-2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23d1d6dec7c68cba177923dea04205d8dbc26faa8ff98cf5d6e79659fced46fb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119315707"
---
# <a name="transmit-from-type-2-file"></a>Transmitir do arquivo Type-2

Para transmitir um arquivo type-2 durante a visualização, use o grafo de filtro mostrado no diagrama a seguir.

![type-2 transmit with preview](images/dv2-transmit.png)

Um arquivo type-2 tem dois fluxos, um fluxo de áudio e um fluxo de vídeo codificado em DV. Esse grafo usa o [filtro DV Muxer](dv-muxer-filter.md) para combinar os fluxos de áudio e vídeo. Ele envia o fluxo intercalado para o filtro MSDV, mas divide o fluxo novamente para visualização.

Crie este grafo da seguinte forma:


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



Esse código faz várias chamadas para **RenderStream:**

Os dois primeiros conectam o filtro de origem ao Divisor AVI e ao Divisor AVI ao DV Mux. Na primeira chamada, o Construtor Graph Capture adiciona automaticamente o Divisor AVI ao grafo e conecta um dos pinos de saída do divisor AVI ao DV Mux. Na segunda chamada, o Construtor Graph Capture localiza o segundo pino de saída do divisor AVI e conecta-o ao DV Mux.

A terceira chamada para **RenderStream** conecta o DV Muxer ao filtro Tee de Pino Infinito. A próxima chamada conecta um fluxo do Pin Infinito Tee ao filtro de captura MSDV. Esse fluxo é transmitido para o dispositivo. A última chamada para **RenderStream** cria a seção de visualização do grafo.

Se você não quiser visualizar durante a transmissão, poderá omitir o Pin Infinito Tee e simplesmente conectar o DV Mux ao filtro MSDV:


```C++
hr = pBuilder->RenderStream(0, 0, pDVMux, 0, pDV);
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Vídeo digital no DirectShow](digital-video-in-directshow.md)
</dt> </dl>

 

 



