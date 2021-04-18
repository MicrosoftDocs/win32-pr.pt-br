---
title: Configurando fluxos de vídeo
description: Configurando fluxos de vídeo
ms.assetid: caffdfc1-3c35-4b7b-8643-5a9095cc11f6
keywords:
- fluxos, configurando fluxos de vídeo
- codecs, configurando fluxos de vídeo
- fluxos de vídeo, configurando
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9d2389026dc1061064c5e687da60c3350ad94a4
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "105781362"
---
# <a name="configuring-video-streams"></a><span data-ttu-id="3604a-106">Configurando fluxos de vídeo</span><span class="sxs-lookup"><span data-stu-id="3604a-106">Configuring Video Streams</span></span>

<span data-ttu-id="3604a-107">Os fluxos de vídeo são mais flexíveis em sua configuração do que os fluxos de áudio.</span><span class="sxs-lookup"><span data-stu-id="3604a-107">Video streams are more flexible in their configuration than audio streams.</span></span> <span data-ttu-id="3604a-108">Isso ocorre porque as propriedades dos quadros que compõem o vídeo podem variar muito de um arquivo para o outro.</span><span class="sxs-lookup"><span data-stu-id="3604a-108">This is because the properties of the frames that make up the video can vary widely from one file to the next.</span></span> <span data-ttu-id="3604a-109">Ao recuperar o formato de codec para o codec que você está usando, você deve definir os valores a seguir para objetos de configuração de fluxo de vídeo.</span><span class="sxs-lookup"><span data-stu-id="3604a-109">When you retrieve the codec format for the codec you are using, you must set the following values for video stream configuration objects.</span></span>



| <span data-ttu-id="3604a-110">Valor</span><span class="sxs-lookup"><span data-stu-id="3604a-110">Value</span></span>                                 | <span data-ttu-id="3604a-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="3604a-111">Description</span></span>                                                                                                                                                                                                                                                                 |
|---------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3604a-112">Taxa de bits</span><span class="sxs-lookup"><span data-stu-id="3604a-112">Bit rate</span></span>                              | <span data-ttu-id="3604a-113">Chame [**IWMStreamConfig:: settaxa de bits**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig-setbitrate) para definir como o valor desejado.</span><span class="sxs-lookup"><span data-stu-id="3604a-113">Call [**IWMStreamConfig::SetBitrate**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig-setbitrate) to set to the desired value.</span></span> <span data-ttu-id="3604a-114">O codec de vídeo tentará compactar a mídia para atender às suas especificações.</span><span class="sxs-lookup"><span data-stu-id="3604a-114">The video codec will try to compress the media to meet your specifications.</span></span> <span data-ttu-id="3604a-115">Se os valores forem muito baixos, o vídeo compactado resultante será muito degradado.</span><span class="sxs-lookup"><span data-stu-id="3604a-115">If your values are too low, the resulting compressed video will be very degraded.</span></span>           |
| <span data-ttu-id="3604a-116">Janela de buffer</span><span class="sxs-lookup"><span data-stu-id="3604a-116">Buffer window</span></span>                         | <span data-ttu-id="3604a-117">Chame [**IWMStreamConfig:: SetBufferWindow**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig-setbufferwindow) para definir o valor desejado.</span><span class="sxs-lookup"><span data-stu-id="3604a-117">Call [**IWMStreamConfig::SetBufferWindow**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig-setbufferwindow) to set to the desired value.</span></span> <span data-ttu-id="3604a-118">O codec de vídeo tentará compactar a mídia para atender às suas especificações.</span><span class="sxs-lookup"><span data-stu-id="3604a-118">The video codec will try to compress the media to meet your specifications.</span></span> <span data-ttu-id="3604a-119">Se os valores forem muito baixos, o vídeo compactado resultante será muito degradado.</span><span class="sxs-lookup"><span data-stu-id="3604a-119">If your values are too low, the resulting compressed video will be very degraded.</span></span> |
| <span data-ttu-id="3604a-120">**WMVIDEOINFOHEADER.rcSource**</span><span class="sxs-lookup"><span data-stu-id="3604a-120">**WMVIDEOINFOHEADER.rcSource**</span></span>        | <span data-ttu-id="3604a-121">O canto superior esquerdo deve ser definido como 0, 0.</span><span class="sxs-lookup"><span data-stu-id="3604a-121">The upper left corner must be set to 0,0.</span></span> <span data-ttu-id="3604a-122">O canto inferior direito deve ser definido para as dimensões do quadro.</span><span class="sxs-lookup"><span data-stu-id="3604a-122">The lower right corner must be set to the frame dimensions.</span></span> <span data-ttu-id="3604a-123">Por exemplo, em um fluxo de 640x480, essas configurações seriam 0, 0640480.</span><span class="sxs-lookup"><span data-stu-id="3604a-123">For example, in a 640x480 stream, these settings would be 0,0,640,480.</span></span>                                                                                                |
| <span data-ttu-id="3604a-124">**WMVIDEOINFOHEADER.rcTarget**</span><span class="sxs-lookup"><span data-stu-id="3604a-124">**WMVIDEOINFOHEADER.rcTarget**</span></span>        | <span data-ttu-id="3604a-125">Deve corresponder a **rcSource**.</span><span class="sxs-lookup"><span data-stu-id="3604a-125">Must match **rcSource**.</span></span>                                                                                                                                                                                                                                                    |
| <span data-ttu-id="3604a-126">**WMVIDEOINFOHEADER.dwBitRate**</span><span class="sxs-lookup"><span data-stu-id="3604a-126">**WMVIDEOINFOHEADER.dwBitRate**</span></span>       | <span data-ttu-id="3604a-127">Deve corresponder à taxa de bits definida para o fluxo.</span><span class="sxs-lookup"><span data-stu-id="3604a-127">Must match the bit rate set for the stream.</span></span>                                                                                                                                                                                                                                 |
| <span data-ttu-id="3604a-128">**WMVIDEOINFOHEADER. AvgTimePerFrame**</span><span class="sxs-lookup"><span data-stu-id="3604a-128">**WMVIDEOINFOHEADER.AvgTimePerFrame**</span></span> | <span data-ttu-id="3604a-129">Defina para o tempo aproximado por quadro.</span><span class="sxs-lookup"><span data-stu-id="3604a-129">Set to the approximate time per frame.</span></span>                                                                                                                                                                                                                                      |
| <span data-ttu-id="3604a-130">**BITMAPINFOHEADER. bilargura**</span><span class="sxs-lookup"><span data-stu-id="3604a-130">**BITMAPINFOHEADER.biWidth**</span></span>          | <span data-ttu-id="3604a-131">Defina para a largura, em pixels, do tamanho do quadro desejado.</span><span class="sxs-lookup"><span data-stu-id="3604a-131">Set to the width, in pixels, of the desired frame size.</span></span>                                                                                                                                                                                                                     |
| <span data-ttu-id="3604a-132">**BITMAPINFOHEADER. biHeight**</span><span class="sxs-lookup"><span data-stu-id="3604a-132">**BITMAPINFOHEADER.biHeight**</span></span>         | <span data-ttu-id="3604a-133">Defina para a altura, em pixels, do tamanho do quadro desejado.</span><span class="sxs-lookup"><span data-stu-id="3604a-133">Set to the height, in pixels, of the desired frame size.</span></span>                                                                                                                                                                                                                    |



 

<span data-ttu-id="3604a-134">O conteúdo de vídeo não é reproduzido corretamente, a menos que esteja codificado para um tamanho que seja um múltiplo de quatro para largura e altura.</span><span class="sxs-lookup"><span data-stu-id="3604a-134">Video content does not play correctly unless it is encoded to a size that is a multiple of four for both width and height.</span></span> <span data-ttu-id="3604a-135">A exceção é um vídeo [*RGB*](wmformat-glossary.md) descompactado, que pode ser qualquer tamanho.</span><span class="sxs-lookup"><span data-stu-id="3604a-135">The exception is [*RGB*](wmformat-glossary.md) uncompressed video, which can be any size.</span></span> <span data-ttu-id="3604a-136">Se você tentar definir um tamanho que não seja um múltiplo de quatro, um dos seguintes erros será retornado pelo gravador:</span><span class="sxs-lookup"><span data-stu-id="3604a-136">If you try to set a size that is not a multiple of four, one of the following errors will be returned by the writer:</span></span>

-   <span data-ttu-id="3604a-137">\_formato de \_ \_ entrada inválido \_ do NS E</span><span class="sxs-lookup"><span data-stu-id="3604a-137">NS\_E\_INVALID\_INPUT\_FORMAT</span></span>
-   <span data-ttu-id="3604a-138">\_formato de saída NS E \_ inválido \_ \_</span><span class="sxs-lookup"><span data-stu-id="3604a-138">NS\_E\_INVALID\_OUTPUT\_FORMAT</span></span>
-   <span data-ttu-id="3604a-139">NS \_ E \_ INVALIDPROFILE</span><span class="sxs-lookup"><span data-stu-id="3604a-139">NS\_E\_INVALIDPROFILE</span></span>

<span data-ttu-id="3604a-140">Se você estiver usando a codificação de taxa de bits variável, talvez seja necessário fazer outros ajustes.</span><span class="sxs-lookup"><span data-stu-id="3604a-140">If you are using variable bit rate encoding, you may need to make other adjustments.</span></span> <span data-ttu-id="3604a-141">Para obter mais informações, consulte [Configuring VBR streams](configuring-vbr-streams.md).</span><span class="sxs-lookup"><span data-stu-id="3604a-141">For more information, see [Configuring VBR Streams](configuring-vbr-streams.md).</span></span>

<span data-ttu-id="3604a-142">Alguns codecs de vídeo do Windows Media dão suporte a vários níveis de complexidade.</span><span class="sxs-lookup"><span data-stu-id="3604a-142">Some Windows Media Video codecs support multiple complexity levels.</span></span> <span data-ttu-id="3604a-143">Os níveis de complexidade determinam os algoritmos que o codec usará ao codificar um fluxo de vídeo.</span><span class="sxs-lookup"><span data-stu-id="3604a-143">Complexity levels determine the algorithms that the codec will use when encoding a video stream.</span></span> <span data-ttu-id="3604a-144">O uso de um nível de complexidade alta exigirá mais capacidade de processamento para codificação e decodificação.</span><span class="sxs-lookup"><span data-stu-id="3604a-144">Using a high complexity level will require more processing power for encoding and decoding.</span></span>

<span data-ttu-id="3604a-145">Cada codec que dá suporte às configurações de complexidade expõe as seguintes configurações que você pode recuperar com o método [**IWMCodecInfo3:: GetCodecProp**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmcodecinfo3-getcodecprop) .</span><span class="sxs-lookup"><span data-stu-id="3604a-145">Each codec that supports complexity settings exposes the following settings that you can retrieve with the [**IWMCodecInfo3::GetCodecProp**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmcodecinfo3-getcodecprop) method.</span></span>



| <span data-ttu-id="3604a-146">Configuração</span><span class="sxs-lookup"><span data-stu-id="3604a-146">Setting</span></span>                 | <span data-ttu-id="3604a-147">Descrição</span><span class="sxs-lookup"><span data-stu-id="3604a-147">Description</span></span>                                         |
|-------------------------|-----------------------------------------------------|
| <span data-ttu-id="3604a-148">g \_ wszComplexityMax</span><span class="sxs-lookup"><span data-stu-id="3604a-148">g\_wszComplexityMax</span></span>     | <span data-ttu-id="3604a-149">O nível de qualidade máximo suportado pelo codec.</span><span class="sxs-lookup"><span data-stu-id="3604a-149">The maximum quality level supported by the codec.</span></span>   |
| <span data-ttu-id="3604a-150">g \_ wszComplexityOffline</span><span class="sxs-lookup"><span data-stu-id="3604a-150">g\_wszComplexityOffline</span></span> | <span data-ttu-id="3604a-151">O nível de qualidade sugerido para reprodução offline.</span><span class="sxs-lookup"><span data-stu-id="3604a-151">The suggested quality level for offline playback.</span></span>   |
| <span data-ttu-id="3604a-152">g \_ wszComplexityLive</span><span class="sxs-lookup"><span data-stu-id="3604a-152">g\_wszComplexityLive</span></span>    | <span data-ttu-id="3604a-153">O nível de qualidade sugerido para reprodução de streaming.</span><span class="sxs-lookup"><span data-stu-id="3604a-153">The suggested quality level for streaming playback.</span></span> |



 

<span data-ttu-id="3604a-154">Para definir a complexidade de um fluxo de vídeo em um perfil, use o método [**IWMPropertyVault:: SetProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmpropertyvault-setproperty) usando a propriedade g \_ wszComplexity.</span><span class="sxs-lookup"><span data-stu-id="3604a-154">To set the complexity for a video stream in a profile, use the [**IWMPropertyVault::SetProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmpropertyvault-setproperty) method using the property g\_wszComplexity.</span></span> <span data-ttu-id="3604a-155">O valor definido deve ser menor ou igual à complexidade máxima com suporte para o codec.</span><span class="sxs-lookup"><span data-stu-id="3604a-155">The value you set must be less than or equal to the maximum supported complexity for the codec.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3604a-156">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="3604a-156">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3604a-157">**Configuração comum a todos os fluxos**</span><span class="sxs-lookup"><span data-stu-id="3604a-157">**Configuration Common to All Streams**</span></span>](configuration-common-to-all-streams.md)
</dt> <dt>

[<span data-ttu-id="3604a-158">**Configurando fluxos**</span><span class="sxs-lookup"><span data-stu-id="3604a-158">**Configuring Streams**</span></span>](configuring-streams.md)
</dt> <dt>

[<span data-ttu-id="3604a-159">**Configurações de complexidade do vídeo**</span><span class="sxs-lookup"><span data-stu-id="3604a-159">**Video Complexity Settings**</span></span>](video-complexity-settings.md)
</dt> </dl>

 

 




