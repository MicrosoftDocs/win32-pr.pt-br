---
title: Configurando fluxos de vídeo para busca de desempenho
description: Configurando fluxos de vídeo para busca de desempenho
ms.assetid: 2df507f9-60a5-4489-b3db-7fe15604e625
keywords:
- fluxos, configurando fluxos de vídeo
- codecs, configurando fluxos de vídeo
- fluxos de vídeo, configurando
- fluxos de vídeo, desempenho
- desempenho, fluxos de vídeo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33b4fc68e0b3a91cf135d29dc7123d5af88db84c
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "103640130"
---
# <a name="configuring-video-streams-for-seeking-performance"></a><span data-ttu-id="89299-108">Configurando fluxos de vídeo para busca de desempenho</span><span class="sxs-lookup"><span data-stu-id="89299-108">Configuring Video Streams for Seeking Performance</span></span>

<span data-ttu-id="89299-109">Alguns aplicativos de reprodução executam muitas buscas em fluxos individuais.</span><span class="sxs-lookup"><span data-stu-id="89299-109">Some playback applications perform a lot of seeking on individual streams.</span></span> <span data-ttu-id="89299-110">A busca é uma área em que o desempenho pode variar muito dependendo das configurações do fluxo.</span><span class="sxs-lookup"><span data-stu-id="89299-110">Seeking is an area where performance can vary greatly depending upon the settings of the stream.</span></span> <span data-ttu-id="89299-111">Se você souber que seu conteúdo precisa ser otimizado para busca rápida, você pode personalizar sua configuração de fluxo para melhorar o desempenho.</span><span class="sxs-lookup"><span data-stu-id="89299-111">If you know your content needs to be optimized for quick seeking, you can tailor your stream configuration to improve performance.</span></span>

<span data-ttu-id="89299-112">O maior fator que afeta a velocidade das operações de busca em vídeo é o espaçamento dos quadros-chave.</span><span class="sxs-lookup"><span data-stu-id="89299-112">The biggest factor affecting the speed of seeking operations in video is the spacing of the key frames.</span></span> <span data-ttu-id="89299-113">Como cada quadro entre os quadros-chave precisa ser reconstruído com base nos quadros que vier antes dele, quadros-chave amplamente espaçados resultam em tempos de busca mais longos.</span><span class="sxs-lookup"><span data-stu-id="89299-113">Because every frame between key frames needs to be reconstructed based on the frames that come before it, widely spaced key frames result longer seek times.</span></span> <span data-ttu-id="89299-114">Por exemplo, se um fluxo de vídeo com 30 quadros por segundo tiver um espaçamento máximo de quadro de chave de 10 segundos, haverá quadros potencialmente 300 entre quadros-chave.</span><span class="sxs-lookup"><span data-stu-id="89299-114">For example, if a video stream with 30 frames per second has a maximum key-frame spacing of 10 seconds, there are potentially 300 frames between key frames.</span></span> <span data-ttu-id="89299-115">Se você buscar até o último [*quadro Delta*](wmformat-glossary.md), 299 quadros precisarão ser reconstruídos para que o quadro seja descompactado.</span><span class="sxs-lookup"><span data-stu-id="89299-115">If you seek to the last [*delta frame*](wmformat-glossary.md), 299 frames have to be reconstructed for the frame to be decompressed.</span></span> <span data-ttu-id="89299-116">Se cada reconstrução de quadro levou 0,01 segundo, a busca levaria quase 3 segundos.</span><span class="sxs-lookup"><span data-stu-id="89299-116">If each frame reconstruction took .01 second, the seek would take almost 3 seconds.</span></span> <span data-ttu-id="89299-117">Se você quiser aumentar a eficiência de busca, reduzir o espaçamento de quadro-chave pode ajudar.</span><span class="sxs-lookup"><span data-stu-id="89299-117">If you want to increase the efficiency of seeking, lowering the key-frame spacing can help.</span></span> <span data-ttu-id="89299-118">No entanto, se você definir os quadros-chave muito próximos juntos, poderá perder a qualidade.</span><span class="sxs-lookup"><span data-stu-id="89299-118">However, if you set the key frames too close together, you can lose quality.</span></span>

<span data-ttu-id="89299-119">Você pode definir o espaçamento máximo de quadro de chave chamando [**IWMVideoMediaProps:: SetMaxKeyFrameSpacing**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmvideomediaprops-setmaxkeyframespacing).</span><span class="sxs-lookup"><span data-stu-id="89299-119">You can set the maximum key-frame spacing by calling [**IWMVideoMediaProps::SetMaxKeyFrameSpacing**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmvideomediaprops-setmaxkeyframespacing).</span></span> <span data-ttu-id="89299-120">Os valores recomendados, com base na taxa de bits do fluxo, são listados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="89299-120">The recommended values, based on the bit rate of the stream, are listed in the following table.</span></span> <span data-ttu-id="89299-121">Esses valores fornecem um bom equilíbrio entre desempenho e qualidade de busca.</span><span class="sxs-lookup"><span data-stu-id="89299-121">These values provide a good balance of seeking performance and quality.</span></span> <span data-ttu-id="89299-122">O SDK não impõe nenhum limite no tempo entre os quadros-chave.</span><span class="sxs-lookup"><span data-stu-id="89299-122">The SDK does not enforce any limit on the time between key frames.</span></span> <span data-ttu-id="89299-123">Em geral, as vezes mais de 30 segundos podem afetar negativamente os tempos de busca quando o conteúdo é transmitido em uma rede e quando é reproduzido localmente.</span><span class="sxs-lookup"><span data-stu-id="89299-123">In general, times longer than 30 seconds can adversely affect seek times both when the content is streamed over a network, and when it is played back locally.</span></span>



| <span data-ttu-id="89299-124">Taxa de bits</span><span class="sxs-lookup"><span data-stu-id="89299-124">Bit rate</span></span>             | <span data-ttu-id="89299-125">Máximo sugerido de espaçamento de quadro de chave</span><span class="sxs-lookup"><span data-stu-id="89299-125">Suggested maximum key-frame spacing</span></span> |
|----------------------|-------------------------------------|
| <span data-ttu-id="89299-126">22 kbps a 300 kbps</span><span class="sxs-lookup"><span data-stu-id="89299-126">22 Kbps to 300 Kbps</span></span>  | <span data-ttu-id="89299-127">8 segundos</span><span class="sxs-lookup"><span data-stu-id="89299-127">8 seconds</span></span>                           |
| <span data-ttu-id="89299-128">300 kbps a 600 kbps</span><span class="sxs-lookup"><span data-stu-id="89299-128">300 Kbps to 600 Kbps</span></span> | <span data-ttu-id="89299-129">6 segundos</span><span class="sxs-lookup"><span data-stu-id="89299-129">6 seconds</span></span>                           |
| <span data-ttu-id="89299-130">600 kbps a 2 Mbps</span><span class="sxs-lookup"><span data-stu-id="89299-130">600 Kbps to 2 Mbps</span></span>   | <span data-ttu-id="89299-131">4 segundos</span><span class="sxs-lookup"><span data-stu-id="89299-131">4 seconds</span></span>                           |
| <span data-ttu-id="89299-132">2 Mbps e superior</span><span class="sxs-lookup"><span data-stu-id="89299-132">2 Mbps and higher</span></span>    | <span data-ttu-id="89299-133">3 Segundos</span><span class="sxs-lookup"><span data-stu-id="89299-133">3 seconds</span></span>                           |



 

<span data-ttu-id="89299-134">Para obter mais informações sobre como obter o melhor desempenho ao buscar arquivos de vídeo, consulte [obtendo o melhor desempenho de busca de vídeo](getting-the-best-video-seeking-performance.md).</span><span class="sxs-lookup"><span data-stu-id="89299-134">For more information about getting the best performance when seeking video files, see [Getting the Best Video Seeking Performance](getting-the-best-video-seeking-performance.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="89299-135">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="89299-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="89299-136">**Configurando fluxos**</span><span class="sxs-lookup"><span data-stu-id="89299-136">**Configuring Streams**</span></span>](configuring-streams.md)
</dt> </dl>

 

 




