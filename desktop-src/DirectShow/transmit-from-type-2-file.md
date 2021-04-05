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
# <a name="transmit-from-type-2-file"></a><span data-ttu-id="f1dea-103">Transmitir do arquivo do tipo 2</span><span class="sxs-lookup"><span data-stu-id="f1dea-103">Transmit from Type-2 File</span></span>

<span data-ttu-id="f1dea-104">Para transmitir um arquivo de tipo 2 durante a visualização, use o gráfico de filtro mostrado no diagrama a seguir.</span><span class="sxs-lookup"><span data-stu-id="f1dea-104">To transmit a type-2 file while previewing, use the filter graph shown in the following diagram.</span></span>

![transmissão de tipo 2 com visualização](images/dv2-transmit.png)

<span data-ttu-id="f1dea-106">Um arquivo tipo 2 tem dois fluxos, um fluxo de áudio e um fluxo de vídeo codificado por DV.</span><span class="sxs-lookup"><span data-stu-id="f1dea-106">A type-2 file has two streams, one audio stream and one DV-encoded video stream.</span></span> <span data-ttu-id="f1dea-107">Esse grafo usa o filtro [DV Muxer](dv-muxer-filter.md) para combinar os fluxos de áudio e vídeo.</span><span class="sxs-lookup"><span data-stu-id="f1dea-107">This graph uses the [DV Muxer](dv-muxer-filter.md) filter to combine the audio and video streams.</span></span> <span data-ttu-id="f1dea-108">Ele envia o fluxo intercalado para o filtro MSDV, mas divide o fluxo novamente para visualização.</span><span class="sxs-lookup"><span data-stu-id="f1dea-108">It sends the interleaved stream to the MSDV filter, but splits the stream again for preview.</span></span>

<span data-ttu-id="f1dea-109">Compile este grafo da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="f1dea-109">Build this graph as follows:</span></span>


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



<span data-ttu-id="f1dea-110">Esse código faz várias chamadas para **RenderStream**:</span><span class="sxs-lookup"><span data-stu-id="f1dea-110">This code makes several calls to **RenderStream**:</span></span>

<span data-ttu-id="f1dea-111">Os dois primeiros conectam o filtro de origem ao divisor AVI e ao divisor AVI ao MUX DV.</span><span class="sxs-lookup"><span data-stu-id="f1dea-111">The first two connect the source filter to the AVI Splitter and the AVI Splitter to the DV Mux.</span></span> <span data-ttu-id="f1dea-112">Na primeira chamada, o construtor do grafo de captura adiciona automaticamente o divisor AVI ao grafo e conecta um dos pinos de saída do divisor AVI ao MUX DV.</span><span class="sxs-lookup"><span data-stu-id="f1dea-112">In the first call, the Capture Graph Builder automatically adds the AVI Splitter to the graph and connects one of the AVI Splitter's output pins to the DV Mux.</span></span> <span data-ttu-id="f1dea-113">Na segunda chamada, o construtor do grafo de captura localiza o segundo pino de saída do divisor AVI e conecta-o ao MUX DV.</span><span class="sxs-lookup"><span data-stu-id="f1dea-113">In the second call, the Capture Graph Builder finds the AVI Splitter's second output pin and connects that to the DV Mux.</span></span>

<span data-ttu-id="f1dea-114">A terceira chamada para **RenderStream** conecta o Muxer DV ao filtro de t de PIN infinito.</span><span class="sxs-lookup"><span data-stu-id="f1dea-114">The third call to **RenderStream** connects the DV Muxer to the Infinite Pin Tee filter.</span></span> <span data-ttu-id="f1dea-115">A próxima chamada conecta um fluxo do "t" de PIN infinito ao filtro de captura MSDV.</span><span class="sxs-lookup"><span data-stu-id="f1dea-115">The next call connects one stream from the Infinite Pin Tee to the MSDV capture filter.</span></span> <span data-ttu-id="f1dea-116">Esse fluxo é transmitido para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f1dea-116">This stream is transmitted to the device.</span></span> <span data-ttu-id="f1dea-117">A última chamada para **RenderStream** compila a seção de visualização do grafo.</span><span class="sxs-lookup"><span data-stu-id="f1dea-117">The last call to **RenderStream** builds the preview section of the graph.</span></span>

<span data-ttu-id="f1dea-118">Se você não quiser Visualizar durante a transmissão, poderá omitir o "t" de PIN infinito e simplesmente conectar o MUX DV ao filtro MSDV:</span><span class="sxs-lookup"><span data-stu-id="f1dea-118">If you do not want to preview while transmitting, you can omit the Infinite Pin Tee, and simply connect the DV Mux to the MSDV filter:</span></span>


```C++
hr = pBuilder->RenderStream(0, 0, pDVMux, 0, pDV);
```



## <a name="related-topics"></a><span data-ttu-id="f1dea-119">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f1dea-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f1dea-120">Vídeo digital no DirectShow</span><span class="sxs-lookup"><span data-stu-id="f1dea-120">Digital Video in DirectShow</span></span>](digital-video-in-directshow.md)
</dt> </dl>

 

 



