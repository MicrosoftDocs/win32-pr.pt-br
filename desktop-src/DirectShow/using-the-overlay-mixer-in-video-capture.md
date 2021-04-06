---
description: Usando o mixer de sobreposição na captura de vídeo
ms.assetid: 43468fa2-6dea-439d-9e24-f47a053ad561
title: Usando o mixer de sobreposição na captura de vídeo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72bff115d566654732e80c0bcb0f554c4ad96e65
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011319"
---
# <a name="using-the-overlay-mixer-in-video-capture"></a><span data-ttu-id="d0b70-103">Usando o mixer de sobreposição na captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="d0b70-103">Using the Overlay Mixer in Video Capture</span></span>

<span data-ttu-id="d0b70-104">Há certos tipos de vídeo que o filtro de [processador de vídeo](video-renderer-filter.md) não pode exibir por si só.</span><span class="sxs-lookup"><span data-stu-id="d0b70-104">There are certain kinds of video that the [Video Renderer](video-renderer-filter.md) filter cannot display by itself.</span></span> <span data-ttu-id="d0b70-105">Nessas situações, o processador de vídeo deve funcionar com o filtro de [mixer de sobreposição](overlay-mixer-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="d0b70-105">In these situations, the Video Renderer must work with the [Overlay Mixer](overlay-mixer-filter.md) filter.</span></span> <span data-ttu-id="d0b70-106">O mixer de sobreposição gerencia a renderização, enquanto o renderizador de vídeo gerencia a janela de vídeo.</span><span class="sxs-lookup"><span data-stu-id="d0b70-106">The Overlay Mixer manages the rendering, while the Video Renderer manages the video window.</span></span> <span data-ttu-id="d0b70-107">O mixer de sobreposição é necessário nas seguintes situações:</span><span class="sxs-lookup"><span data-stu-id="d0b70-107">The Overlay Mixer is needed in the following situations:</span></span>

-   <span data-ttu-id="d0b70-108">Pins da porta de vídeo (VP).</span><span class="sxs-lookup"><span data-stu-id="d0b70-108">Video port (VP) pins.</span></span> <span data-ttu-id="d0b70-109">Se o dispositivo de captura usar uma porta de vídeo, o mixer de sobreposição gerenciará a sobreposição de hardware.</span><span class="sxs-lookup"><span data-stu-id="d0b70-109">If the capture device uses a video port, the Overlay Mixer manages the hardware overlay.</span></span>
-   <span data-ttu-id="d0b70-110">Vídeo entrelaçado.</span><span class="sxs-lookup"><span data-stu-id="d0b70-110">Interlaced video.</span></span> <span data-ttu-id="d0b70-111">Para vídeo entrelaçado, o decodificador requer um formato [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) , ao qual o processador de vídeo não dá suporte.</span><span class="sxs-lookup"><span data-stu-id="d0b70-111">For interlaced video, the decoder requires a [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) format, which the Video Renderer does not support.</span></span>
-   <span data-ttu-id="d0b70-112">Legendas ocultas.</span><span class="sxs-lookup"><span data-stu-id="d0b70-112">Closed captions.</span></span> <span data-ttu-id="d0b70-113">O texto da legenda é renderizado como bitmaps de 8 bits por pixel, que o mixer de sobreposição sobrepõem no vídeo.</span><span class="sxs-lookup"><span data-stu-id="d0b70-113">The caption text is rendered as 8-bits-per-pixel bitmaps, which the Overlay Mixer overlays onto the video.</span></span>

<span data-ttu-id="d0b70-114">O método **RenderStream** do construtor do grafo de captura insere o mixer de sobreposição sempre que necessário.</span><span class="sxs-lookup"><span data-stu-id="d0b70-114">The Capture Graph Builder's **RenderStream** method inserts the Overlay Mixer whenever needed.</span></span> <span data-ttu-id="d0b70-115">Se você estiver criando o grafo sem usar o construtor de grafo de captura, no entanto, deverá verificar cada uma dessas situações e inserir o mixer de sobreposição por conta própria.</span><span class="sxs-lookup"><span data-stu-id="d0b70-115">If you are building the graph without using the Capture Graph Builder, however, you must check for each of these situations and insert the Overlay Mixer yourself.</span></span>

-   <span data-ttu-id="d0b70-116">\[! Fundamental\]</span><span class="sxs-lookup"><span data-stu-id="d0b70-116">\[!Important\]</span></span>  
    > <span data-ttu-id="d0b70-117">Se o dispositivo tiver um VP de PIN, você deverá conectar o mixer de sobreposição mesmo se não precisar da funcionalidade de visualização em seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="d0b70-117">If the device has a VP pin, you must connect the Overlay Mixer even if you do not need preview functionality in your application.</span></span> <span data-ttu-id="d0b70-118">Com uma porta de vídeo, o dispositivo de captura sempre envia os dados de vídeo para a sobreposição de hardware, portanto, o mixer de sobreposição é sempre necessário.</span><span class="sxs-lookup"><span data-stu-id="d0b70-118">With a video port, the capture device always sends the video data to the hardware overlay, so the Overlay Mixer is always needed.</span></span>

     

<span data-ttu-id="d0b70-119">Os filtros de processador de mixagem de vídeo (VMR-7 e VMR-9) dão suporte a vídeo entrelaçado e são capazes de misturar bitmaps de legenda oculta no vídeo primário.</span><span class="sxs-lookup"><span data-stu-id="d0b70-119">The Video Mixing Renderer filters (VMR-7 and VMR-9) both support interlaced video, and are able to mix closed caption bitmaps onto the primary video.</span></span> <span data-ttu-id="d0b70-120">Se você estiver usando o VMR para esses cenários, não será necessário usar o mixer de sobreposição.</span><span class="sxs-lookup"><span data-stu-id="d0b70-120">If you are using the VMR for those scenarios, then you do not need to use the Overlay Mixer.</span></span> <span data-ttu-id="d0b70-121">O VMR-9 não oferece suporte a conexões de VP de PIN.</span><span class="sxs-lookup"><span data-stu-id="d0b70-121">The VMR-9 does not support VP pin connections.</span></span> <span data-ttu-id="d0b70-122">O VMR-7 dá suporte a conexões de VP de PIN por meio do filtro do Gerenciador de porta de vídeo.</span><span class="sxs-lookup"><span data-stu-id="d0b70-122">The VMR-7 supports VP pin connections through the Video Port Manager filter.</span></span> <span data-ttu-id="d0b70-123">No entanto, você pode descobrir que alguns drivers não funcionam corretamente com o Gerenciador de porta de vídeo.</span><span class="sxs-lookup"><span data-stu-id="d0b70-123">However, you may find that some drivers do not work correctly with the Video Port Manager.</span></span> <span data-ttu-id="d0b70-124">Por esse motivo, o mixer de sobreposição ainda é recomendado para VP de pinos.</span><span class="sxs-lookup"><span data-stu-id="d0b70-124">For that reason, the Overlay Mixer is still recommended for VP pins.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d0b70-125">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="d0b70-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d0b70-126">Tópicos de captura avançada</span><span class="sxs-lookup"><span data-stu-id="d0b70-126">Advanced Capture Topics</span></span>](advanced-capture-topics.md)
</dt> <dt>

[<span data-ttu-id="d0b70-127">Pins de porta de vídeo</span><span class="sxs-lookup"><span data-stu-id="d0b70-127">Video Port Pins</span></span>](video-port-pins.md)
</dt> <dt>

[<span data-ttu-id="d0b70-128">Tipo de formato VideoInfo2</span><span class="sxs-lookup"><span data-stu-id="d0b70-128">VideoInfo2 Format Type</span></span>](videoinfo2-format-type.md)
</dt> </dl>

 

 



