---
description: Capturar DV para RGB descompactado
ms.assetid: 02b54070-09c8-45ab-8a08-1493008a5e1f
title: Capturar DV para RGB descompactado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b471bb8be6bc560fda6d3466cebaef8c490cfb8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104087314"
---
# <a name="capture-dv-to-uncompressed-rgb"></a><span data-ttu-id="5d85d-103">Capturar DV para RGB descompactado</span><span class="sxs-lookup"><span data-stu-id="5d85d-103">Capture DV to Uncompressed RGB</span></span>

<span data-ttu-id="5d85d-104">Este exemplo mostra como capturar DV da camcorder e salvá-la em um arquivo como RGB descompactado durante a visualização.</span><span class="sxs-lookup"><span data-stu-id="5d85d-104">This example shows how to capture DV from the camcorder and save it to a file as uncompressed RGB while previewing.</span></span> <span data-ttu-id="5d85d-105">Use o gráfico de filtro mostrado no diagrama a seguir.</span><span class="sxs-lookup"><span data-stu-id="5d85d-105">Use the filter graph shown in the following diagram.</span></span>

![capturando RGB descompactado para o arquivo](images/dv-rgb-cap.png)

<span data-ttu-id="5d85d-107">O filtro de Splitter de DV divide o áudio/vídeo intercalado em fluxos de áudio e vídeo separados o vídeo codificado em DV vai para o filtro de [codificador de vídeo DV](dv-video-decoder-filter.md) , que gera vídeo RGB não compactado.</span><span class="sxs-lookup"><span data-stu-id="5d85d-107">The DV Splitter filter splits the interleaved audio/video into separate video and audio streams The DV-encoded video goes to the [DV Video Decoder](dv-video-decoder-filter.md) filter, which outputs uncompressed RGB video.</span></span> <span data-ttu-id="5d85d-108">O vídeo RGB é roteado por meio do filtro de monitoração inteligente para o filtro AVI Mux (para captura) e o processador de vídeo (para visualização).</span><span class="sxs-lookup"><span data-stu-id="5d85d-108">The RGB video is routed through the Smart Tee filter to the AVI Mux filter (for capture) and the video renderer (for preview).</span></span> <span data-ttu-id="5d85d-109">Enquanto isso, o fluxo de áudio do divisor de DV passa pelo filtro de t de PIN infinito para o AVI Mux e o processador de áudio.</span><span class="sxs-lookup"><span data-stu-id="5d85d-109">Meanwhile, the audio stream from the DV Splitter goes through the Infinite Pin Tee filter to the AVI Mux and the audio renderer.</span></span> <span data-ttu-id="5d85d-110">O Gerenciador de gráfico de filtro mantém todos esses fluxos sincronizados, usando os carimbos de data/hora nos exemplos e no relógio de referência do grafo.</span><span class="sxs-lookup"><span data-stu-id="5d85d-110">The Filter Graph Manager keeps all of these streams synchronized, using the time stamps on the samples and the graph reference clock.</span></span>

<span data-ttu-id="5d85d-111">Esse grafo pode parecer desnecessariamente complicado, mas garante que o fluxo de vídeo codificado em DV seja decodificado apenas uma vez, o que minimiza os requisitos de CPU.</span><span class="sxs-lookup"><span data-stu-id="5d85d-111">This graph might seem unnecessarily complicated, but it ensures that the DV-encoded video stream is decoded only once, which minimizes the CPU requirements.</span></span> <span data-ttu-id="5d85d-112">Além disso, observe que o vídeo passa pelo filtro de monitoração inteligente enquanto o áudio passa pelo filtro de t de PIN infinito.</span><span class="sxs-lookup"><span data-stu-id="5d85d-112">Also, note that the video goes through the Smart Tee filter while the audio goes through the Infinite Pin Tee filter.</span></span> <span data-ttu-id="5d85d-113">O monitor inteligente pode descartar quadros de visualização para melhorar o desempenho da captura, o que é desejável para vídeo, mas não para áudio, onde as amostras descartadas são altamente perceptíveis.</span><span class="sxs-lookup"><span data-stu-id="5d85d-113">The Smart Tee can drop preview frames to improve capture performance, which is desirable for video but not for audio, where dropped samples are highly noticeable.</span></span> <span data-ttu-id="5d85d-114">Além disso, como o áudio requer uma largura de banda muito menor do que o vídeo, há relativamente pouca chance de remover o áudio no arquivo.</span><span class="sxs-lookup"><span data-stu-id="5d85d-114">Also, because the audio requires much lower bandwidth than the video, there is relatively little chance of dropping audio in the file.</span></span>

<span data-ttu-id="5d85d-115">Você deve criar esse gráfico uma seção por vez, mas o método RenderStream ainda pode ajudar.</span><span class="sxs-lookup"><span data-stu-id="5d85d-115">You must build this graph one section at a time, but the RenderStream method can still help.</span></span> <span data-ttu-id="5d85d-116">Use o seguinte código:</span><span class="sxs-lookup"><span data-stu-id="5d85d-116">Use the following code:</span></span>


```C++
// Build the file-writing section of the graph.
hr = pBuilder->SetOutputFileName(&MEDIASUBTYPE_Avi, 
    OLESTR("C:\\Example3.avi"), &pMux, 0);

// MSDV to DV splitter.
IBaseFilter *pDVSplit;  // Create the DV Splitter (CLSID_DVSplitter)
hr = pBuilder->RenderStream(0, &MEDIATYPE_Interleaved, pDV, 0, pDVSplit);

// Splitter to DV Decoder to Smart Tee.
IBaseFilter *pDVDec; // Create the DV Decoder (CLSID_DVVideoCodec)
IBaseFilter *pSmartTee; // Create the Smart Tee (CLSID_SmartTee)
hr = pBuilder->RenderStream(0, &MEDIATYPE_Video, pDVSplit, pDVDec,
    pSmartTee);

// Smart Tee (video) to Avi Mux.
IPin *pPin1;
hr = pBuilder->FindPin(pSmartTee, PINDIR_OUTPUT, 0, 0, TRUE, 0, &pPin1);
hr = pBuilder->RenderStream(0, 0, pPin1, 0, pMux);

// Smart Tee to preview.
IPin *pPin2;
hr = pBuilder->FindPin(pSmartTee, PINDIR_OUTPUT, 0, 0, TRUE, 1, &pPin2);
hr = pBuilder->RenderStream(0, 0, pPin2, 0, pMux);

// DV Splitter (audio) to Infinite Tee to Avi Mux.
IBaseFilter *pTee; // Create the Infinite Pin Tee (CLSID_InfTee)
hr = pBuilder->RenderStream(0, &MEDIATYPE_Audio, pDVSplit, pTee, pMux);

// Infinite Pin Tee to preview.
hr = pBuilder->RenderStream(0, 0, pTee, 0, 0);
```



<span data-ttu-id="5d85d-117">Você deve criar os filtros de visor DV, decodificador de vídeo DV, monitoração inteligente e de t PIN infinito e adicionar cada um ao gráfico de filtro.</span><span class="sxs-lookup"><span data-stu-id="5d85d-117">You must create the DV Splitter, DV Video Decoder, Smart Tee, and Infinite Pin Tee filters, and add each one to the filter graph.</span></span> <span data-ttu-id="5d85d-118">(Para fins de brevidade, essas etapas são omitidas do código anterior.) Este exemplo usa o método [**ICaptureGraphBuilder2:: FindPin**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findpin) para localizar os Pins de captura e visualização no filtro de "inteligente"; a captura sempre é o pino de saída 0 e a visualização é o pino de saída 1.</span><span class="sxs-lookup"><span data-stu-id="5d85d-118">(For brevity, these steps are omitted from the previous code.) This example uses the [**ICaptureGraphBuilder2::FindPin**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findpin) method to find the capture and preview pins on the Smart Tee filter; capture is always output pin 0, and preview is output pin 1.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5d85d-119">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="5d85d-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5d85d-120">Vídeo digital no DirectShow</span><span class="sxs-lookup"><span data-stu-id="5d85d-120">Digital Video in DirectShow</span></span>](digital-video-in-directshow.md)
</dt> </dl>

 

 



