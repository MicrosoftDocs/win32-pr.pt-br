---
title: Configurando fluxos de captura de tela
description: Configurando fluxos de captura de tela
ms.assetid: 974e679f-0bf6-412b-9e80-43370de7605a
keywords:
- fluxos, configurando fluxos de captura de tela
- codecs, configurando fluxos de captura de tela
- fluxos de captura de tela
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8200c4a6e733c2bb7f908b79cb73dbb2c3244dc4
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "103916968"
---
# <a name="configuring-screen-capture-streams"></a><span data-ttu-id="c5a69-106">Configurando fluxos de captura de tela</span><span class="sxs-lookup"><span data-stu-id="c5a69-106">Configuring Screen Capture Streams</span></span>

<span data-ttu-id="c5a69-107">Os fluxos que usam o codec de tela vídeo 9 do Windows Media® são configurados por aplicativos da mesma maneira que os fluxos de vídeo normais.</span><span class="sxs-lookup"><span data-stu-id="c5a69-107">Streams that use the Windows Media® Video 9 Screen codec are configured by applications in the same way as normal video streams.</span></span> <span data-ttu-id="c5a69-108">No entanto, se você definir o nível de complexidade do vídeo como 0, o gravador irá ignorar qualquer conjunto de valores de qualidade de vídeo com [**IWMVideoMediaProps:: setquality**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmvideomediaprops-setquality).</span><span class="sxs-lookup"><span data-stu-id="c5a69-108">However, if you set the video complexity level to 0, the writer will ignore any video quality value set with [**IWMVideoMediaProps::SetQuality**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmvideomediaprops-setquality).</span></span> <span data-ttu-id="c5a69-109">Para obter mais informações, consulte [obtendo bons resultados com o codec de tela do Windows Media Video 9](getting-good-results-with-the-windows-media-video-9-screen-codec.md).</span><span class="sxs-lookup"><span data-stu-id="c5a69-109">For more information, see [Getting Good Results with the Windows Media Video 9 Screen Codec](getting-good-results-with-the-windows-media-video-9-screen-codec.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="c5a69-110">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c5a69-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c5a69-111">**Configurando fluxos**</span><span class="sxs-lookup"><span data-stu-id="c5a69-111">**Configuring Streams**</span></span>](configuring-streams.md)
</dt> <dt>

[<span data-ttu-id="c5a69-112">**Configuração comum a todos os fluxos**</span><span class="sxs-lookup"><span data-stu-id="c5a69-112">**Configuration Common to All Streams**</span></span>](configuration-common-to-all-streams.md)
</dt> <dt>

[<span data-ttu-id="c5a69-113">**Configurando fluxos de vídeo**</span><span class="sxs-lookup"><span data-stu-id="c5a69-113">**Configuring Video Streams**</span></span>](configuring-video-streams.md)
</dt> </dl>

 

 




