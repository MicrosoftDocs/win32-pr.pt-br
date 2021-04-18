---
title: Formatos de entrada de vídeo
description: Formatos de entrada de vídeo
ms.assetid: 0f1ec15d-328e-4c07-bf58-fd4ecb483549
keywords:
- SDK do Windows Media Format, formatos de entrada de vídeo
- ASF (Advanced Systems Format), formatos de entrada de vídeo
- ASF (formato de sistemas avançados), formatos de entrada de vídeo
- formatos de entrada de vídeo
- SDK do Windows Media Format, formatos de vídeo
- ASF (Advanced Systems Format), formatos de vídeo
- ASF (formato de sistemas avançados), formatos de vídeo
- formatos de vídeo
- Codec do Windows Media Video 9, formatos de entrada de vídeo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c5113ee3cbd9c9235104f858968db20ebc29e3a
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/25/2020
ms.locfileid: "105781084"
---
# <a name="video-input-formats"></a><span data-ttu-id="198b9-112">Formatos de entrada de vídeo</span><span class="sxs-lookup"><span data-stu-id="198b9-112">Video Input Formats</span></span>

<span data-ttu-id="198b9-113">O gravador aceita os seguintes formatos de vídeo como entrada a ser compactada usando o codec do Windows Media Video 9:</span><span class="sxs-lookup"><span data-stu-id="198b9-113">The writer accepts the following video formats as input to be compressed using the Windows Media Video 9 codec:</span></span>

-   <span data-ttu-id="198b9-114">WMMEDIASUBTYPE \_ IYUV</span><span class="sxs-lookup"><span data-stu-id="198b9-114">WMMEDIASUBTYPE\_IYUV</span></span>
-   <span data-ttu-id="198b9-115">WMMEDIASUBTYPE \_ I420</span><span class="sxs-lookup"><span data-stu-id="198b9-115">WMMEDIASUBTYPE\_I420</span></span>
-   <span data-ttu-id="198b9-116">WMMEDIASUBTYPE \_ YV12</span><span class="sxs-lookup"><span data-stu-id="198b9-116">WMMEDIASUBTYPE\_YV12</span></span>
-   <span data-ttu-id="198b9-117">WMMEDIASUBTYPE \_ YUY2</span><span class="sxs-lookup"><span data-stu-id="198b9-117">WMMEDIASUBTYPE\_YUY2</span></span>
-   <span data-ttu-id="198b9-118">WMMEDIASUBTYPE \_ UYVY</span><span class="sxs-lookup"><span data-stu-id="198b9-118">WMMEDIASUBTYPE\_UYVY</span></span>
-   <span data-ttu-id="198b9-119">WMMEDIASUBTYPE \_ YVYU</span><span class="sxs-lookup"><span data-stu-id="198b9-119">WMMEDIASUBTYPE\_YVYU</span></span>
-   <span data-ttu-id="198b9-120">WMMEDIASUBTYPE \_ YVU9</span><span class="sxs-lookup"><span data-stu-id="198b9-120">WMMEDIASUBTYPE\_YVU9</span></span>
-   <span data-ttu-id="198b9-121">WMMEDIASUBTYPE \_ RGB32</span><span class="sxs-lookup"><span data-stu-id="198b9-121">WMMEDIASUBTYPE\_RGB32</span></span>
-   <span data-ttu-id="198b9-122">WMMEDIASUBTYPE \_ RGB24</span><span class="sxs-lookup"><span data-stu-id="198b9-122">WMMEDIASUBTYPE\_RGB24</span></span>
-   <span data-ttu-id="198b9-123">WMMEDIASUBTYPE \_ RGB565</span><span class="sxs-lookup"><span data-stu-id="198b9-123">WMMEDIASUBTYPE\_RGB565</span></span>
-   <span data-ttu-id="198b9-124">WMMEDIASUBTYPE \_ RGB555</span><span class="sxs-lookup"><span data-stu-id="198b9-124">WMMEDIASUBTYPE\_RGB555</span></span>
-   <span data-ttu-id="198b9-125">WMMEDIASUBTYPE \_ RGB8</span><span class="sxs-lookup"><span data-stu-id="198b9-125">WMMEDIASUBTYPE\_RGB8</span></span>

<span data-ttu-id="198b9-126">Você sempre deve usar [**IWMWriter:: GetInputFormatCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriter-getinputformatcount) e [**IWMWriter:: GetInputFormat**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-getinputformat) para enumerar os formatos de entrada disponíveis e obter o objeto de propriedades de mídia de entrada para o formato desejado.</span><span class="sxs-lookup"><span data-stu-id="198b9-126">You should always use [**IWMWriter::GetInputFormatCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriter-getinputformatcount) and [**IWMWriter::GetInputFormat**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-getinputformat) to enumerate the available input formats and to obtain the input media properties object for the desired format.</span></span> <span data-ttu-id="198b9-127">Os objetos de propriedades de mídia de entrada de vídeo devem ser alterados para refletir o tamanho do quadro e a taxa de quadros da mídia de entrada.</span><span class="sxs-lookup"><span data-stu-id="198b9-127">Video input media properties objects must be changed to reflect the frame size and frame rate of your input media.</span></span>

## <a name="related-topics"></a><span data-ttu-id="198b9-128">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="198b9-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="198b9-129">**Identificadores de tipo de mídia**</span><span class="sxs-lookup"><span data-stu-id="198b9-129">**Media Type Identifiers**</span></span>](media-type-identifiers.md)
</dt> <dt>

[<span data-ttu-id="198b9-130">**Tipos de mídia**</span><span class="sxs-lookup"><span data-stu-id="198b9-130">**Media Types**</span></span>](media-types.md)
</dt> </dl>

 

 




