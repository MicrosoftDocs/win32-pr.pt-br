---
description: Interfaces de captura de vídeo
ms.assetid: a7ec6607-d6fe-4cf4-b3f2-8636c4d15982
title: Interfaces de captura de vídeo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7c88ab86833a3570789dee311b36d49f382c9cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105785332"
---
# <a name="video-capture-interfaces"></a><span data-ttu-id="6089a-103">Interfaces de captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="6089a-103">Video Capture Interfaces</span></span>

<span data-ttu-id="6089a-104">Essas interfaces dão suporte à captura de vídeo, usando os dispositivos WDM (Microsoft® Windows® Driver Model) ou os dispositivos Microsoft® Video para Windows® (VFW) herdados.</span><span class="sxs-lookup"><span data-stu-id="6089a-104">These interfaces support video capture, using Microsoft® Windows® Driver Model (WDM) devices or legacy Microsoft® Video for Windows® (VFW) devices.</span></span>



| <span data-ttu-id="6089a-105">Interface</span><span class="sxs-lookup"><span data-stu-id="6089a-105">Interface</span></span>                                                        | <span data-ttu-id="6089a-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="6089a-106">Description</span></span>                                                                                                  |
|------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6089a-107">**IAMAnalogVideoDecoder**</span><span class="sxs-lookup"><span data-stu-id="6089a-107">**IAMAnalogVideoDecoder**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iamanalogvideodecoder)           | <span data-ttu-id="6089a-108">Controle a digitalização de vídeo em uma placa de captura de vídeo WDM.</span><span class="sxs-lookup"><span data-stu-id="6089a-108">Control video digitization on a WDM video capture card.</span></span>                                                      |
| [<span data-ttu-id="6089a-109">**IAMBufferNegotiation**</span><span class="sxs-lookup"><span data-stu-id="6089a-109">**IAMBufferNegotiation**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iambuffernegotiation)             | <span data-ttu-id="6089a-110">Controle como um PIN aloca buffers.</span><span class="sxs-lookup"><span data-stu-id="6089a-110">Control how a pin allocates buffers.</span></span>                                                                         |
| [<span data-ttu-id="6089a-111">**IAMCopyCaptureFileProgress**</span><span class="sxs-lookup"><span data-stu-id="6089a-111">**IAMCopyCaptureFileProgress**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iamcopycapturefileprogress) | <span data-ttu-id="6089a-112">Interface de retorno de chamada para receber o progresso de uma operação de cópia de arquivo.</span><span class="sxs-lookup"><span data-stu-id="6089a-112">Callback interface to receive the progress of a file copy operation.</span></span>                                         |
| [<span data-ttu-id="6089a-113">**IAMCrossbar**</span><span class="sxs-lookup"><span data-stu-id="6089a-113">**IAMCrossbar**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iamcrossbar)                               | <span data-ttu-id="6089a-114">Crie uma conexão de hardware entre uma fonte de áudio ou vídeo WDM e um dispositivo de captura WDM.</span><span class="sxs-lookup"><span data-stu-id="6089a-114">Create a hardware connection between a WDM audio or video source and a WDM capture device.</span></span>                   |
| [<span data-ttu-id="6089a-115">**IAMDroppedFrames**</span><span class="sxs-lookup"><span data-stu-id="6089a-115">**IAMDroppedFrames**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iamdroppedframes)                     | <span data-ttu-id="6089a-116">Consulte um filtro de captura sobre o desempenho de captura.</span><span class="sxs-lookup"><span data-stu-id="6089a-116">Query a capture filter about capture performance.</span></span>                                                            |
| [<span data-ttu-id="6089a-117">**IAMStreamControl**</span><span class="sxs-lookup"><span data-stu-id="6089a-117">**IAMStreamControl**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iamstreamcontrol)                     | <span data-ttu-id="6089a-118">Controle as horas de início e de término de fluxos individuais.</span><span class="sxs-lookup"><span data-stu-id="6089a-118">Control the start and stop times of individual streams.</span></span>                                                      |
| [<span data-ttu-id="6089a-119">**IAMStreamConfig**</span><span class="sxs-lookup"><span data-stu-id="6089a-119">**IAMStreamConfig**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig)                       | <span data-ttu-id="6089a-120">Consulte e defina o formato de saída do filtro de captura.</span><span class="sxs-lookup"><span data-stu-id="6089a-120">Query and set the capture filter's output format.</span></span>                                                            |
| [<span data-ttu-id="6089a-121">**IAMVfwCaptureDialogs**</span><span class="sxs-lookup"><span data-stu-id="6089a-121">**IAMVfwCaptureDialogs**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iamvfwcapturedialogs)             | <span data-ttu-id="6089a-122">Exiba as caixas de diálogo fornecidas pelos drivers de captura do VFW.</span><span class="sxs-lookup"><span data-stu-id="6089a-122">Display the dialog boxes provided by VFW capture drivers.</span></span>                                                    |
| [<span data-ttu-id="6089a-123">**IAMVideoControl**</span><span class="sxs-lookup"><span data-stu-id="6089a-123">**IAMVideoControl**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iamvideocontrol)                       | <span data-ttu-id="6089a-124">Controle a imagem de um dispositivo de captura.</span><span class="sxs-lookup"><span data-stu-id="6089a-124">Control the picture from a capture device.</span></span>                                                                   |
| [<span data-ttu-id="6089a-125">**IAMVideoProcAmp**</span><span class="sxs-lookup"><span data-stu-id="6089a-125">**IAMVideoProcAmp**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iamvideoprocamp)                       | <span data-ttu-id="6089a-126">Ajuste as qualidades de um sinal de vídeo, como brilho, contraste, matiz, saturação, gama e nitidez.</span><span class="sxs-lookup"><span data-stu-id="6089a-126">Adjust the qualities of a video signal, such as brightness, contrast, hue, saturation, gamma, and sharpness.</span></span> |
| [<span data-ttu-id="6089a-127">**ICaptureGraphBuilder2**</span><span class="sxs-lookup"><span data-stu-id="6089a-127">**ICaptureGraphBuilder2**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2)           | <span data-ttu-id="6089a-128">Crie gráficos de filtro para captura de vídeo.</span><span class="sxs-lookup"><span data-stu-id="6089a-128">Build filter graphs for video capture.</span></span>                                                                       |
| [<span data-ttu-id="6089a-129">**IFileSinkFilter2**</span><span class="sxs-lookup"><span data-stu-id="6089a-129">**IFileSinkFilter2**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ifilesinkfilter2)                     | <span data-ttu-id="6089a-130">Especifique o nome e os atributos de um arquivo de saída.</span><span class="sxs-lookup"><span data-stu-id="6089a-130">Specify the name and attributes of an output file.</span></span>                                                           |



 

## <a name="related-topics"></a><span data-ttu-id="6089a-131">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="6089a-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6089a-132">Interfaces de controle de dispositivo externo</span><span class="sxs-lookup"><span data-stu-id="6089a-132">External Device Control Interfaces</span></span>](external-device-control-interfaces.md)
</dt> <dt>

[<span data-ttu-id="6089a-133">Captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="6089a-133">Video Capture</span></span>](video-capture.md)
</dt> </dl>

 

 



