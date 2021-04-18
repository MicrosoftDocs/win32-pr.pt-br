---
title: Usando fluxos de áudio e vídeo não compactados
description: Usando fluxos de áudio e vídeo não compactados
ms.assetid: 1a8fe604-bd99-4ba1-878f-8e1fd89483b3
keywords:
- fluxos, configurando fluxos de áudio e vídeo não compactados
- codecs, configurando fluxos de áudio e vídeo descompactados
- fluxos de vídeo, não compactados
- fluxos de áudio, não compactados
- fluxos de áudio e vídeo não compactados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d00d81bd0a9f8c53751e404a0cfb0e55d57d4242
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "105764218"
---
# <a name="using-uncompressed-audio-and-video-streams"></a><span data-ttu-id="90abd-108">Usando fluxos de áudio e vídeo não compactados</span><span class="sxs-lookup"><span data-stu-id="90abd-108">Using Uncompressed Audio and Video Streams</span></span>

<span data-ttu-id="90abd-109">Na maioria das circunstâncias, a mídia descompactada tem extremamente grandes requisitos de armazenamento e entrega, mas para alguns cenários de reprodução local, o nível de qualidade é importante o suficiente para garantir que não esteja usando a compactação.</span><span class="sxs-lookup"><span data-stu-id="90abd-109">Under most circumstances, uncompressed media has prohibitively large storage and delivery requirements, but for some local playback scenarios, the quality level is important enough to warrant not using compression..</span></span>

<span data-ttu-id="90abd-110">As configurações para um fluxo de mídia não compactado devem refletir as configurações da mídia de origem.</span><span class="sxs-lookup"><span data-stu-id="90abd-110">The settings for an uncompressed media stream should reflect the settings of the source media.</span></span> <span data-ttu-id="90abd-111">Ao configurar um fluxo descompactado, você deve calcular a taxa de bits da mídia e definir o fluxo adequadamente chamando [**IWMStreamConfig::**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig-setbitrate)setrateion.</span><span class="sxs-lookup"><span data-stu-id="90abd-111">When configuring an uncompressed stream, you must calculate the bit rate of the media and set the stream appropriately by calling [**IWMStreamConfig::SetBitrate**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig-setbitrate).</span></span> <span data-ttu-id="90abd-112">Como os fluxos não compactados não são viáveis para streaming, você sempre deve definir a janela de buffer para fluxos de mídia não compactados como zero chamando [**IWMStreamConfig:: SetBufferWindow**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig-setbufferwindow).</span><span class="sxs-lookup"><span data-stu-id="90abd-112">Because uncompressed streams are not viable for streaming, you should always set the buffer window for uncompressed media streams to zero by calling [**IWMStreamConfig::SetBufferWindow**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig-setbufferwindow).</span></span>

<span data-ttu-id="90abd-113">Os seguintes formatos de pixel têm suporte para fluxos de vídeo não compactados:</span><span class="sxs-lookup"><span data-stu-id="90abd-113">The following pixel formats are supported for uncompressed video streams:</span></span>

-   <span data-ttu-id="90abd-114">WMMEDIASUBTYPE \_ RGB555</span><span class="sxs-lookup"><span data-stu-id="90abd-114">WMMEDIASUBTYPE\_RGB555</span></span>
-   <span data-ttu-id="90abd-115">WMMEDIASUBTYPE \_ RGB24</span><span class="sxs-lookup"><span data-stu-id="90abd-115">WMMEDIASUBTYPE\_RGB24</span></span>
-   <span data-ttu-id="90abd-116">WMMEDIASUBTYPE \_ RGB32</span><span class="sxs-lookup"><span data-stu-id="90abd-116">WMMEDIASUBTYPE\_RGB32</span></span>
-   <span data-ttu-id="90abd-117">WMMEDIASUBTYPE \_ I420</span><span class="sxs-lookup"><span data-stu-id="90abd-117">WMMEDIASUBTYPE\_I420</span></span>
-   <span data-ttu-id="90abd-118">WMMEDIASUBTYPE \_ IYUV</span><span class="sxs-lookup"><span data-stu-id="90abd-118">WMMEDIASUBTYPE\_IYUV</span></span>
-   <span data-ttu-id="90abd-119">WMMEDIASUBTYPE \_ YV12</span><span class="sxs-lookup"><span data-stu-id="90abd-119">WMMEDIASUBTYPE\_YV12</span></span>
-   <span data-ttu-id="90abd-120">WMMEDIASUBTYPE \_ YUY2</span><span class="sxs-lookup"><span data-stu-id="90abd-120">WMMEDIASUBTYPE\_YUY2</span></span>
-   <span data-ttu-id="90abd-121">WMMEDIASUBTYPE \_ UYVY</span><span class="sxs-lookup"><span data-stu-id="90abd-121">WMMEDIASUBTYPE\_UYVY</span></span>
-   <span data-ttu-id="90abd-122">WMMEDIASUBTYPE \_ YVYU</span><span class="sxs-lookup"><span data-stu-id="90abd-122">WMMEDIASUBTYPE\_YVYU</span></span>

## <a name="related-topics"></a><span data-ttu-id="90abd-123">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="90abd-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="90abd-124">**Configuração comum a todos os fluxos**</span><span class="sxs-lookup"><span data-stu-id="90abd-124">**Configuration Common to All Streams**</span></span>](configuration-common-to-all-streams.md)
</dt> <dt>

[<span data-ttu-id="90abd-125">**Configurando fluxos de áudio**</span><span class="sxs-lookup"><span data-stu-id="90abd-125">**Configuring Audio Streams**</span></span>](configuring-audio-streams.md)
</dt> <dt>

[<span data-ttu-id="90abd-126">**Configurando fluxos**</span><span class="sxs-lookup"><span data-stu-id="90abd-126">**Configuring Streams**</span></span>](configuring-streams.md)
</dt> <dt>

[<span data-ttu-id="90abd-127">**Configurando fluxos de vídeo**</span><span class="sxs-lookup"><span data-stu-id="90abd-127">**Configuring Video Streams**</span></span>](configuring-video-streams.md)
</dt> </dl>

 

 




