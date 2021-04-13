---
description: Sobre vídeo digital no DirectShow
ms.assetid: 0570bf7c-c38d-4ada-9593-27b9be117893
title: Sobre vídeo digital no DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8f4ae0253754583bb89132289db87f0aad673d6
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104560709"
---
# <a name="about-digital-video-in-directshow"></a><span data-ttu-id="b0ae2-103">Sobre vídeo digital no DirectShow</span><span class="sxs-lookup"><span data-stu-id="b0ae2-103">About Digital Video in DirectShow</span></span>

<span data-ttu-id="b0ae2-104">O vídeo digital (DV) pode ser capturado de uma câmera DV, armazenada em um arquivo no computador do usuário ou armazenada em fita usando um gravador de fita de vídeo (VTR).</span><span class="sxs-lookup"><span data-stu-id="b0ae2-104">Digital video (DV) can be captured from a DV camera, stored in a file on the user's computer, or stored on tape using a video tape recorder (VTR).</span></span> <span data-ttu-id="b0ae2-105">Portanto, as operações que um aplicativo pode executar em um fluxo de DV incluem:</span><span class="sxs-lookup"><span data-stu-id="b0ae2-105">Thus, the operations that an application might perform on a DV stream include:</span></span>

-   <span data-ttu-id="b0ae2-106">Capture o vídeo ao vivo de uma câmera de vídeo digital.</span><span class="sxs-lookup"><span data-stu-id="b0ae2-106">Capture live video from a DV camera.</span></span>
-   <span data-ttu-id="b0ae2-107">Transmita dados DV da fita VTR para o computador.</span><span class="sxs-lookup"><span data-stu-id="b0ae2-107">Transmit DV data from VTR tape to the computer.</span></span>
-   <span data-ttu-id="b0ae2-108">Transmita dados DV do computador para o VTR.</span><span class="sxs-lookup"><span data-stu-id="b0ae2-108">Transmit DV data from the computer to the VTR.</span></span>
-   <span data-ttu-id="b0ae2-109">Ler dados de DV de um arquivo.</span><span class="sxs-lookup"><span data-stu-id="b0ae2-109">Read DV data from a file.</span></span>
-   <span data-ttu-id="b0ae2-110">Gravar dados DV em um arquivo.</span><span class="sxs-lookup"><span data-stu-id="b0ae2-110">Write DV data to a file.</span></span>
-   <span data-ttu-id="b0ae2-111">Renderizar o áudio e o vídeo em um fluxo de DV.</span><span class="sxs-lookup"><span data-stu-id="b0ae2-111">Render the audio and video in a DV stream.</span></span>

<span data-ttu-id="b0ae2-112">O DirectShow fornece os seguintes filtros de DV:</span><span class="sxs-lookup"><span data-stu-id="b0ae2-112">DirectShow provides the following DV filters:</span></span>

-   <span data-ttu-id="b0ae2-113">[Driver MSDV](msdv-driver.md).</span><span class="sxs-lookup"><span data-stu-id="b0ae2-113">[MSDV Driver](msdv-driver.md).</span></span> <span data-ttu-id="b0ae2-114">O driver MSDV controla um dispositivo DV, como uma camcorder.</span><span class="sxs-lookup"><span data-stu-id="b0ae2-114">The MSDV driver controls a DV device, such as a camcorder.</span></span> <span data-ttu-id="b0ae2-115">O dispositivo pode ter uma subunidade de câmera e uma subunidade VTR; MSDV controla ambas as subunidades.</span><span class="sxs-lookup"><span data-stu-id="b0ae2-115">The device may have a camera subunit and a VTR subunit; MSDV controls both subunits.</span></span> <span data-ttu-id="b0ae2-116">O driver MSDV aparece para aplicativos como um filtro do DirectShow.</span><span class="sxs-lookup"><span data-stu-id="b0ae2-116">The MSDV driver appears to applications as a DirectShow filter.</span></span>
-   <span data-ttu-id="b0ae2-117">Filtro de [Splitter de DV](dv-splitter-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="b0ae2-117">[DV Splitter](dv-splitter-filter.md) filter.</span></span> <span data-ttu-id="b0ae2-118">Os quadros de DV contêm áudio e vídeo no mesmo quadro.</span><span class="sxs-lookup"><span data-stu-id="b0ae2-118">DV frames contain audio and video in the same frame.</span></span> <span data-ttu-id="b0ae2-119">O filtro de Splitter de DV extrai os dados de áudio e os gera como um ou dois fluxos de áudio.</span><span class="sxs-lookup"><span data-stu-id="b0ae2-119">The DV Splitter filter extracts the audio data and outputs it as one or two audio streams.</span></span> <span data-ttu-id="b0ae2-120">Ele gera os dados originais como um fluxo de vídeo DV separado.</span><span class="sxs-lookup"><span data-stu-id="b0ae2-120">It outputs the original data as a separate DV video stream.</span></span>
-   <span data-ttu-id="b0ae2-121">Filtro de [decodificador de vídeo DV](dv-video-decoder-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="b0ae2-121">[DV Video Decoder](dv-video-decoder-filter.md) filter.</span></span> <span data-ttu-id="b0ae2-122">Decodifica vídeo DV em vídeo descompactado.</span><span class="sxs-lookup"><span data-stu-id="b0ae2-122">Decodes DV video into uncompressed video.</span></span>
-   <span data-ttu-id="b0ae2-123">Filtro de [codificador de vídeo DV](dv-video-encoder-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="b0ae2-123">[DV Video Encoder](dv-video-encoder-filter.md) filter.</span></span> <span data-ttu-id="b0ae2-124">Codifica vídeo descompactado para vídeo codificado em DV.</span><span class="sxs-lookup"><span data-stu-id="b0ae2-124">Encodes uncompressed video to DV-encoded video.</span></span>
-   <span data-ttu-id="b0ae2-125">[Muxer DV](dv-muxer-filter.md).</span><span class="sxs-lookup"><span data-stu-id="b0ae2-125">[DV Muxer](dv-muxer-filter.md).</span></span> <span data-ttu-id="b0ae2-126">Combina um fluxo de vídeo DV com um ou dois fluxos de áudio, para criar um fluxo de DV único intercalado.</span><span class="sxs-lookup"><span data-stu-id="b0ae2-126">Combines a DV video stream with one or two audio streams, to create a single interleaved DV stream.</span></span>

<span data-ttu-id="b0ae2-127">O separador de vídeo DV e o decodificador DV Video funcionam juntos.</span><span class="sxs-lookup"><span data-stu-id="b0ae2-127">The DV Splitter and DV Video Decoder work together.</span></span> <span data-ttu-id="b0ae2-128">O divisor usa o fluxo intercalado e gera fluxos de vídeo de áudio e DV separados.</span><span class="sxs-lookup"><span data-stu-id="b0ae2-128">The splitter takes the interleaved stream and outputs separate audio and DV video streams.</span></span> <span data-ttu-id="b0ae2-129">O decodificador converte o vídeo DV em vídeo descompactado.</span><span class="sxs-lookup"><span data-stu-id="b0ae2-129">The decoder converts the DV video to uncompressed video.</span></span> <span data-ttu-id="b0ae2-130">A imagem a seguir ilustra esse processo.</span><span class="sxs-lookup"><span data-stu-id="b0ae2-130">The following image illustrates this process.</span></span>

![divisor DV e codificador DV](images/dv-filters1.png)

<span data-ttu-id="b0ae2-132">O codificador de vídeo DV e o DV Muxer reverte o processo: o codificador converte vídeo descompactado em vídeo DV e o MUX combina áudio e vídeo DV para criar um fluxo intercalado único, conforme mostrado no diagrama a seguir.</span><span class="sxs-lookup"><span data-stu-id="b0ae2-132">The DV Video Encoder and the DV Muxer reverse the process: The encoder converts uncompressed video to DV video, and the mux combines audio and DV video to create a single interleaved stream, as shown in the following diagram.</span></span>

![codificador DV e DV Muxer](images/dv-filters2.png)

## <a name="related-topics"></a><span data-ttu-id="b0ae2-134">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b0ae2-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b0ae2-135">Vídeo digital no DirectShow</span><span class="sxs-lookup"><span data-stu-id="b0ae2-135">Digital Video in DirectShow</span></span>](digital-video-in-directshow.md)
</dt> </dl>

 

 



