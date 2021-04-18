---
description: MSYUV é um codec de conversor de espaço de cores YUV a RGB.
ms.assetid: 77b00937-ac63-4b23-b546-c0896b3c57ba
title: Codec de conversor de espaço de cores MSYUV
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 838e7cd749042b2fb97adaf0b2b4cd0378a81c07
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105796263"
---
# <a name="msyuv-color-space-converter-codec"></a><span data-ttu-id="5e220-103">Codec de conversor de espaço de cores MSYUV</span><span class="sxs-lookup"><span data-stu-id="5e220-103">MSYUV Color Space Converter Codec</span></span>

<span data-ttu-id="5e220-104">MSYUV é um codec de conversor de espaço de cores YUV a RGB.</span><span class="sxs-lookup"><span data-stu-id="5e220-104">MSYUV is a YUV-to-RGB color space converter codec.</span></span> <span data-ttu-id="5e220-105">Ele permite a reprodução de dados de origem de vídeo em formatos YUV em clientes cujo adaptador de vídeo não pode ser usado para conversões de YUV para RGB no hardware.</span><span class="sxs-lookup"><span data-stu-id="5e220-105">It enables playback of video source data in YUV formats on clients whose video display adapter cannot be used for YUV-to-RGB conversions in hardware.</span></span> <span data-ttu-id="5e220-106">O codec participa de gráficos de filtro por meio do filtro de wrapper do [descompactador AVI](avi-decompressor-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="5e220-106">The codec participates in filter graphs through the [AVI Decompressor](avi-decompressor-filter.md) wrapper filter.</span></span>

<span data-ttu-id="5e220-107">Câmeras de conferência digital com interfaces USB ou 1394 podem produzir dados de imagem em vários formatos YUV.</span><span class="sxs-lookup"><span data-stu-id="5e220-107">Digital conferencing cameras with 1394 or USB interfaces can produce image data in various YUV formats.</span></span> <span data-ttu-id="5e220-108">Se o hardware de vídeo não oferecer suporte à conversão de YUV para RGB integrada ou se o recurso de conversão de hardware não puder ser usado por algum outro motivo, os dados de imagem YUV deverão ser convertidos para o formato RGB antes de serem enviados para o processador de vídeo.</span><span class="sxs-lookup"><span data-stu-id="5e220-108">If the display hardware does not support on-board YUV-to-RGB conversion, or if the hardware conversion capability cannot be used for some other reason, then the YUV image data must be converted to RGB format before it is sent to the Video Renderer.</span></span>

<span data-ttu-id="5e220-109">Devido ao requisito do [processador de vídeo](video-renderer-filter.md)para um tipo de entrada RGB no momento da conexão, esse filtro pode ser inserido em um grafo upstream do processador de vídeo durante a criação automática de grafo.</span><span class="sxs-lookup"><span data-stu-id="5e220-109">Because of the [Video Renderer](video-renderer-filter.md)'s requirement for an RGB input type at connection time, this filter might be inserted into a graph upstream from the Video Renderer during automatic graph building.</span></span> <span data-ttu-id="5e220-110">Especificamente, se o construtor de gráficos detectar um formato YUV no tipo de mídia do pino de saída do filtro upstream, o construtor de grafo irá inserir o descompactador AVI, que carregará o codec MSYUV e o configurará inicialmente para executar a conversão em RGB.</span><span class="sxs-lookup"><span data-stu-id="5e220-110">Specifically, if the Graph Builder detects a YUV format in the media type of the upstream filter's output pin, the Graph Builder will insert the AVI Decompressor, which will then load the MSYUV codec and configure it initially to perform the conversion to RGB.</span></span> <span data-ttu-id="5e220-111">Depois que o grafo passa pela primeira vez para um estado de execução ou pausado, o filtro de processamento de vídeo pode detectar se o adaptador de vídeo pode executar a conversão em hardware.</span><span class="sxs-lookup"><span data-stu-id="5e220-111">After the graph first transitions to a run or paused state, the Video Renderer filter can detect whether the video display adapter can perform the conversion in hardware.</span></span> <span data-ttu-id="5e220-112">Se puder, o descompactador AVI será notificado e reconfigurará o MSYUV para operar no "modo de passagem", o que faz com que o codec ignore a conversão e copie os dados de imagem YUV diretamente em uma superfície de sobreposição do DirectDraw na memória de vídeo.</span><span class="sxs-lookup"><span data-stu-id="5e220-112">If it can, then the AVI Decompressor is notified and it reconfigures MSYUV to operate in "pass-through mode," which causes the codec to skip the conversion and copy the YUV image data directly onto a DirectDraw overlay surface in video memory.</span></span>

<span data-ttu-id="5e220-113">Como os renderizadores de mixagem de vídeo (VMR-7 e VMR-9) nunca usam GDI, eles não exigem um tipo RGB no momento da conexão e o conversor de espaço de cor MSYUV nunca é inserido antes do VMR em um grafo.</span><span class="sxs-lookup"><span data-stu-id="5e220-113">Because the Video Mixing Renderers (VMR-7 and VMR-9) never use GDI, they do not require an RGB type at connect time, and the MSYUV Color Space Converter is never inserted before the VMR in a graph.</span></span>

<span data-ttu-id="5e220-114">MSYUV converte os formatos YUV empacotados em RGB, conforme mostrado na lista a seguir:</span><span class="sxs-lookup"><span data-stu-id="5e220-114">MSYUV converts packed YUV formats to RGB, as shown in the following list:</span></span>

-   <span data-ttu-id="5e220-115">Formatos de entrada: UYVY, YUY2, YVYU</span><span class="sxs-lookup"><span data-stu-id="5e220-115">Input formats: UYVY, YUY2, YVYU</span></span>
-   <span data-ttu-id="5e220-116">Formatos de saída: RGB 8, RGB 16, RGB 24, RGB 32</span><span class="sxs-lookup"><span data-stu-id="5e220-116">Output formats: RGB 8, RGB 16, RGB 24, RGB 32</span></span>

<span data-ttu-id="5e220-117">O codec do conversor de espaço de cores MSYUV é um codec de VCM (Gerenciador de compactação de vídeo).</span><span class="sxs-lookup"><span data-stu-id="5e220-117">The MSYUV Color Space Converter Codec is a Video Compression Manager (VCM) codec.</span></span> <span data-ttu-id="5e220-118">Ele é usado no DirectShow por meio do filtro de [descompactação AVI](avi-decompressor-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="5e220-118">It is used in DirectShow through the [AVI Decompressor](avi-decompressor-filter.md) filter.</span></span> <span data-ttu-id="5e220-119">Para um conversor de cores de uso mais geral, use o [**DSP do conversor de cores**](../medfound/colorconverter.md).</span><span class="sxs-lookup"><span data-stu-id="5e220-119">For a more general-purpose color converter, use the [**Color Converter DSP**](../medfound/colorconverter.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5e220-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5e220-120">Requirements</span></span>



| <span data-ttu-id="5e220-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="5e220-121">Requirement</span></span> | <span data-ttu-id="5e220-122">Valor</span><span class="sxs-lookup"><span data-stu-id="5e220-122">Value</span></span> |
|----------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="5e220-123">DLL</span><span class="sxs-lookup"><span data-stu-id="5e220-123">DLL</span></span><br/> | <dl> <span data-ttu-id="5e220-124"><dt>Msyuv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5e220-124"><dt>Msyuv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5e220-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="5e220-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5e220-126">Filtros do DirectShow</span><span class="sxs-lookup"><span data-stu-id="5e220-126">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 
