---
description: Habilita o processamento de vídeo avançado pelo leitor de origem, incluindo conversão de espaço de cor, desentrelaçamento, redimensionamento de vídeo e conversão de taxa de quadros.
ms.assetid: 1055CD55-4B25-4EEC-AF1B-C84C52287F8F
title: Atributo MF_SOURCE_READER_ENABLE_ADVANCED_VIDEO_PROCESSING (Mfreadwrite. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6978239c5c1c466c78a310b38b5d10bd41f9e004
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501637"
---
# <a name="mf_source_reader_enable_advanced_video_processing-attribute"></a><span data-ttu-id="92041-103">\_Leitor de origem MF \_ \_ habilitar atributo de \_ \_ processamento de vídeo avançado \_</span><span class="sxs-lookup"><span data-stu-id="92041-103">MF\_SOURCE\_READER\_ENABLE\_ADVANCED\_VIDEO\_PROCESSING attribute</span></span>

<span data-ttu-id="92041-104">Habilita o processamento de vídeo avançado pelo [leitor de origem](source-reader.md), incluindo conversão de espaço de cor, desentrelaçamento, redimensionamento de vídeo e conversão de taxa de quadros.</span><span class="sxs-lookup"><span data-stu-id="92041-104">Enables advanced video processing by the [Source Reader](source-reader.md), including color space conversion, deinterlacing, video resizing, and frame-rate conversion.</span></span>

## <a name="data-type"></a><span data-ttu-id="92041-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="92041-105">Data type</span></span>

<span data-ttu-id="92041-106">**Bool** armazenado como **UINT32**</span><span class="sxs-lookup"><span data-stu-id="92041-106">**BOOL** stored as **UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="92041-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="92041-107">Remarks</span></span>

<span data-ttu-id="92041-108">Se esse atributo for **true**, o leitor de origem poderá inserir um processador de vídeo no pipeline de processamento, que habilita os seguintes tipos de conversão de formato:</span><span class="sxs-lookup"><span data-stu-id="92041-108">If this attribute is **TRUE**, the Source Reader can insert a video processor into the processing pipeline, which enables the following types of format conversion:</span></span>

-   <span data-ttu-id="92041-109">Conversão de espaço de cor (YUV para RGB-32)</span><span class="sxs-lookup"><span data-stu-id="92041-109">Color space conversion (YUV to RGB-32)</span></span>
-   <span data-ttu-id="92041-110">Desentrelaçamento</span><span class="sxs-lookup"><span data-stu-id="92041-110">Deinterlacing</span></span>
-   <span data-ttu-id="92041-111">Redimensionamento de vídeo</span><span class="sxs-lookup"><span data-stu-id="92041-111">Video resizing</span></span>
-   <span data-ttu-id="92041-112">Conversão de taxa de quadros</span><span class="sxs-lookup"><span data-stu-id="92041-112">Frame-rate conversion</span></span>

<span data-ttu-id="92041-113">Se esse atributo for **true**, o atributo [MF \_ ReadWrite \_ Disable \_ Converters](mf-readwrite-disable-converters.md) deverá ser **false**.</span><span class="sxs-lookup"><span data-stu-id="92041-113">If this attribute is **TRUE**, the [MF\_READWRITE\_DISABLE\_CONVERTERS](mf-readwrite-disable-converters.md) attribute must be **FALSE**.</span></span>

<span data-ttu-id="92041-114">O leitor de origem procura por processadores de vídeo que estão registrados na categoria MFT, categoria do **\_ \_ \_ processador de vídeo** , incluindo MFTs que são registrados para o processo local.</span><span class="sxs-lookup"><span data-stu-id="92041-114">The Source Reader looks for video processors that are registered in the **MFT\_CATEGORY\_VIDEO\_PROCESSOR** category, including MFTs that are registered for the local process.</span></span> <span data-ttu-id="92041-115">(Consulte [**MFTRegisterLocal**](/windows/desktop/api/mfapi/nf-mfapi-mftregisterlocal) para obter mais informações sobre o registro local de MFTs.) O leitor de origem usa o XVP (processador de vídeo transcodificar) se nenhum outro processador de vídeo adequado for encontrado.</span><span class="sxs-lookup"><span data-stu-id="92041-115">(See [**MFTRegisterLocal**](/windows/desktop/api/mfapi/nf-mfapi-mftregisterlocal) for more information about local registration of MFTs.) The Source Reader uses the Transcode Video Processor (XVP) if no other suitable video processor is found.</span></span>

<span data-ttu-id="92041-116">O aplicativo especifica o tipo de saída desejado chamando [**IMFSourceReader:: SetCurrentMediaType**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-setcurrentmediatype).</span><span class="sxs-lookup"><span data-stu-id="92041-116">The application specifies the desired output type by calling [**IMFSourceReader::SetCurrentMediaType**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-setcurrentmediatype).</span></span> <span data-ttu-id="92041-117">Quando o leitor de origem configura o processador de vídeo, ele tenta corresponder os seguintes atributos do tipo de saída:</span><span class="sxs-lookup"><span data-stu-id="92041-117">When the Source Reader configures the video processor, it attempts to match the following attributes of the output type:</span></span>

-   <span data-ttu-id="92041-118">Taxa de quadros[( \_ \_ \_ taxa de quadros MF MT](mf-mt-frame-rate-attribute.md))</span><span class="sxs-lookup"><span data-stu-id="92041-118">Frame rate ([MF\_MT\_FRAME\_RATE](mf-mt-frame-rate-attribute.md))</span></span>
-   <span data-ttu-id="92041-119">Tamanho do quadro[( \_ \_ \_ tamanho do quadro MF MT](mf-mt-frame-size-attribute.md))</span><span class="sxs-lookup"><span data-stu-id="92041-119">Frame size ([MF\_MT\_FRAME\_SIZE](mf-mt-frame-size-attribute.md))</span></span>
-   <span data-ttu-id="92041-120">Modo entrelaçamento[( \_ \_ \_ modo de entrelaçamento MF MT](mf-mt-interlace-mode-attribute.md))</span><span class="sxs-lookup"><span data-stu-id="92041-120">Interlace mode ([MF\_MT\_INTERLACE\_MODE](mf-mt-interlace-mode-attribute.md))</span></span>
-   <span data-ttu-id="92041-121">Taxa de proporção de pixel (taxa de proporção de[ \_ \_ pixel \_ \_ MF MT](mf-mt-pixel-aspect-ratio-attribute.md))</span><span class="sxs-lookup"><span data-stu-id="92041-121">Pixel aspect ratio ([MF\_MT\_PIXEL\_ASPECT\_RATIO](mf-mt-pixel-aspect-ratio-attribute.md))</span></span>
-   <span data-ttu-id="92041-122">Subtipo ([ \_ \_ subtipo MF MT](mf-mt-subtype-attribute.md))</span><span class="sxs-lookup"><span data-stu-id="92041-122">Subtype ([MF\_MT\_SUBTYPE](mf-mt-subtype-attribute.md))</span></span>

<span data-ttu-id="92041-123">Esse atributo é semelhante ao [leitor de origem MF habilitar o atributo de \_ \_ \_ \_ \_ processamento de vídeo](mf-source-reader-enable-video-processing.md) , mas oferece as seguintes vantagens:</span><span class="sxs-lookup"><span data-stu-id="92041-123">This attribute is similar to the [MF\_SOURCE\_READER\_ENABLE\_VIDEO\_PROCESSING](mf-source-reader-enable-video-processing.md) attribute, but offers the following advantages:</span></span>

-   <span data-ttu-id="92041-124">Há suporte para uma maior variedade de conversões de formato.</span><span class="sxs-lookup"><span data-stu-id="92041-124">A greater range of format conversions is supported.</span></span>
-   <span data-ttu-id="92041-125">Os aplicativos podem registrar seus próprios conversores.</span><span class="sxs-lookup"><span data-stu-id="92041-125">Applications can register their own converters.</span></span>
-   <span data-ttu-id="92041-126">Algumas conversões podem ser executadas em hardware usando a GPU.</span><span class="sxs-lookup"><span data-stu-id="92041-126">Some conversions can be performed in hardware using the GPU.</span></span>

## <a name="requirements"></a><span data-ttu-id="92041-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="92041-127">Requirements</span></span>



| <span data-ttu-id="92041-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="92041-128">Requirement</span></span> | <span data-ttu-id="92041-129">Valor</span><span class="sxs-lookup"><span data-stu-id="92041-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="92041-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="92041-130">Minimum supported client</span></span><br/> | <span data-ttu-id="92041-131">Aplicativos de \[ aplicativos da área de trabalho do Windows 8 \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="92041-131">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="92041-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="92041-132">Minimum supported server</span></span><br/> | <span data-ttu-id="92041-133">Aplicativos do Windows Server 2012 \[ Desktop aplicativos \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="92041-133">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="92041-134">parâmetro</span><span class="sxs-lookup"><span data-stu-id="92041-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="92041-135"><dt>Mfreadwrite. h</dt></span><span class="sxs-lookup"><span data-stu-id="92041-135"><dt>Mfreadwrite.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="92041-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="92041-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="92041-137">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="92041-137">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="92041-138">Leitor de origem</span><span class="sxs-lookup"><span data-stu-id="92041-138">Source Reader</span></span>](source-reader.md)
</dt> <dt>

[<span data-ttu-id="92041-139">Atributos do leitor de origem</span><span class="sxs-lookup"><span data-stu-id="92041-139">Source Reader Attributes</span></span>](source-reader-attributes.md)
</dt> </dl>

 

 




