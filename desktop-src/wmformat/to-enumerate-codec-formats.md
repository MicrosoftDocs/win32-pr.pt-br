---
title: Para enumerar formatos de codec
description: Para enumerar formatos de codec
ms.assetid: 4441b3f8-3edd-441f-8df8-6281937903e0
keywords:
- fluxos, enumerando formatos de codec
- codecs, enumerações
- fluxos, formatos de codec
- codecs, formatos
- codecs, interface IWMCodecInfo
- IWMCodecInfo, formatos de codec
- codecs, interface IWMCodecInfo3
- IWMCodecInfo3, formatos de codec
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93ea062723ec1480a82b45fd025fb7a8c37020d5
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/25/2020
ms.locfileid: "104007234"
---
# <a name="to-enumerate-codec-formats"></a><span data-ttu-id="e423f-111">Para enumerar formatos de codec</span><span class="sxs-lookup"><span data-stu-id="e423f-111">To Enumerate Codec Formats</span></span>

<span data-ttu-id="e423f-112">Um formato de codec é um objeto de configuração de fluxo populado com dados de um codec.</span><span class="sxs-lookup"><span data-stu-id="e423f-112">A codec format is a stream configuration object populated with data from a codec.</span></span> <span data-ttu-id="e423f-113">Cada formato de codec contém uma configuração de mídia com suporte do codec.</span><span class="sxs-lookup"><span data-stu-id="e423f-113">Each codec format contains a media configuration supported by the codec.</span></span> <span data-ttu-id="e423f-114">A maioria dos codecs de áudio dá suporte a um número finito de formatos, cada um dos quais é enumerado pelo codec e pode ser acessado usando os métodos de [**IWMCodecInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcodecinfo).</span><span class="sxs-lookup"><span data-stu-id="e423f-114">Most audio codecs support a finite number of formats, each of which is enumerated by the codec and can be accessed using the methods of [**IWMCodecInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcodecinfo).</span></span> <span data-ttu-id="e423f-115">Os codecs de vídeo, por outro lado, fornecem apenas um único formato.</span><span class="sxs-lookup"><span data-stu-id="e423f-115">Video codecs, on the other hand, provide only a single format.</span></span> <span data-ttu-id="e423f-116">Isso ocorre porque os fluxos de vídeo têm variáveis, como tamanho de quadro, que são mais flexíveis do que as configurações de um fluxo de áudio.</span><span class="sxs-lookup"><span data-stu-id="e423f-116">This is because video streams have variables, like frame size, that are more flexible than the settings of an audio stream.</span></span> <span data-ttu-id="e423f-117">Com um fluxo de vídeo, você deve preencher alguns dos valores de configuração de fluxo; as configurações de fluxo de áudio só devem ser editadas para atribuir um nome, um nome de conexão e um número de fluxo.</span><span class="sxs-lookup"><span data-stu-id="e423f-117">With a video stream, you must fill in some of the stream configuration values; audio stream configurations should only be edited to assign a name, connection name, and stream number.</span></span> <span data-ttu-id="e423f-118">Para obter mais informações, consulte [configuração comum a todos os fluxos](configuration-common-to-all-streams.md).</span><span class="sxs-lookup"><span data-stu-id="e423f-118">For more information, see [Configuration Common to All Streams](configuration-common-to-all-streams.md).</span></span>

<span data-ttu-id="e423f-119">Os formatos de codec enumerados dependem das configurações atuais de enumeração do codec, que são definidas usando [**IWMCodecInfo3:: SetCodecEnumerationSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmcodecinfo3-setcodecenumerationsetting).</span><span class="sxs-lookup"><span data-stu-id="e423f-119">The codec formats enumerated depend upon the current codec enumeration settings, which are set using [**IWMCodecInfo3::SetCodecEnumerationSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmcodecinfo3-setcodecenumerationsetting).</span></span> <span data-ttu-id="e423f-120">Atualmente, há suporte apenas para duas propriedades de codec: g \_ wszNumPasses, que especifica o número de passagens de codificação que o codec executará e g \_ wszVBREnabled, que especifica se o codec usará a codificação de taxa de bits variável.</span><span class="sxs-lookup"><span data-stu-id="e423f-120">Currently, only two codec properties are supported: g\_wszNumPasses, which specifies the number of encoding passes that the codec will perform, and g\_wszVBREnabled, which specifies whether the codec will use variable bit rate encoding.</span></span> <span data-ttu-id="e423f-121">O número máximo de passagens de codificação com suporte de qualquer um dos codecs é dois, portanto, há quatro configurações distintas para as quais você pode recuperar codecs, conforme mostrado na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="e423f-121">The maximum number of encoding passes supported by any of the codecs is two, so there are four distinct configurations for which you can retrieve codecs, as shown in the following table.</span></span>



|                  | <span data-ttu-id="e423f-122">Fluxo de taxa de bits constante (CBR)</span><span class="sxs-lookup"><span data-stu-id="e423f-122">Constant bit rate (CBR) stream</span></span> | <span data-ttu-id="e423f-123">2-transmitir fluxo de CBR</span><span class="sxs-lookup"><span data-stu-id="e423f-123">2-pass CBR stream</span></span> | <span data-ttu-id="e423f-124">Fluxo de taxa de bits variável (VBR) com base na qualidade</span><span class="sxs-lookup"><span data-stu-id="e423f-124">Quality-based variable bit rate (VBR) stream</span></span> | <span data-ttu-id="e423f-125">Fluxo de VBR (restrito ou irrestrito) com base na taxa de bits</span><span class="sxs-lookup"><span data-stu-id="e423f-125">Bit-rate-based VBR stream (constrained or unconstrained)</span></span> |
|------------------|--------------------------------|-------------------|----------------------------------------------|----------------------------------------------------------|
| <span data-ttu-id="e423f-126">g \_ wszVBREnabled</span><span class="sxs-lookup"><span data-stu-id="e423f-126">g\_wszVBREnabled</span></span> | <span data-ttu-id="e423f-127">FALSE</span><span class="sxs-lookup"><span data-stu-id="e423f-127">FALSE</span></span>                          | <span data-ttu-id="e423f-128">FALSE</span><span class="sxs-lookup"><span data-stu-id="e423f-128">FALSE</span></span>             | <span data-ttu-id="e423f-129">TRUE</span><span class="sxs-lookup"><span data-stu-id="e423f-129">TRUE</span></span>                                         | <span data-ttu-id="e423f-130">TRUE</span><span class="sxs-lookup"><span data-stu-id="e423f-130">TRUE</span></span>                                                     |
| <span data-ttu-id="e423f-131">g \_ wszNumPasses</span><span class="sxs-lookup"><span data-stu-id="e423f-131">g\_wszNumPasses</span></span>  | <span data-ttu-id="e423f-132">1</span><span class="sxs-lookup"><span data-stu-id="e423f-132">1</span></span>                              | <span data-ttu-id="e423f-133">2</span><span class="sxs-lookup"><span data-stu-id="e423f-133">2</span></span>                 | <span data-ttu-id="e423f-134">1</span><span class="sxs-lookup"><span data-stu-id="e423f-134">1</span></span>                                            | <span data-ttu-id="e423f-135">2</span><span class="sxs-lookup"><span data-stu-id="e423f-135">2</span></span>                                                        |



 

<span data-ttu-id="e423f-136">Para enumerar os formatos com suporte para um codec, use [**IWMCodecInfo:: GetCodecFormatCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmcodecinfo-getcodecformatcount) para localizar o número de codecs com suporte.</span><span class="sxs-lookup"><span data-stu-id="e423f-136">To enumerate the formats supported for a codec, use [**IWMCodecInfo::GetCodecFormatCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmcodecinfo-getcodecformatcount) to find the number of supported codecs.</span></span> <span data-ttu-id="e423f-137">Em seguida, chame [**IWMCodecInfo:: GetCodecFormat**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmcodecinfo-getcodecformat) para cada formato.</span><span class="sxs-lookup"><span data-stu-id="e423f-137">Then call [**IWMCodecInfo::GetCodecFormat**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmcodecinfo-getcodecformat) for each format.</span></span> <span data-ttu-id="e423f-138">O formato indexa o intervalo de zero, para um menor que o número total de formatos com suporte.</span><span class="sxs-lookup"><span data-stu-id="e423f-138">The format indexes range from zero, to one less than the total number of supported formats.</span></span> <span data-ttu-id="e423f-139">Você pode recuperar uma descrição do formato chamando [**IWMCodecInfo2:: GetCodecFormatDesc**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmcodecinfo2-getcodecformatdesc).</span><span class="sxs-lookup"><span data-stu-id="e423f-139">You can retrieve a description of the format by calling [**IWMCodecInfo2::GetCodecFormatDesc**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmcodecinfo2-getcodecformatdesc).</span></span> <span data-ttu-id="e423f-140">Ao usar **GetCodecFormatDesc**, você não precisa usar **GetCodecFormat**, porque o objeto de configuração de fluxo é recuperado por ambos os métodos.</span><span class="sxs-lookup"><span data-stu-id="e423f-140">When using **GetCodecFormatDesc**, you do not need to use **GetCodecFormat**, because the stream configuration object is retrieved by both methods.</span></span> <span data-ttu-id="e423f-141">Os formatos de codec de vídeo não incluem uma descrição.</span><span class="sxs-lookup"><span data-stu-id="e423f-141">Video codec formats do not include a description.</span></span> <span data-ttu-id="e423f-142">Cada codec de vídeo tem apenas um formato que é usado para todos os fluxos desse tipo.</span><span class="sxs-lookup"><span data-stu-id="e423f-142">Each video codec has only one format that is used for all streams of that type.</span></span>

<span data-ttu-id="e423f-143">Ao recuperar um formato de codec, você obtém a interface [**IWMStreamConfig**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig) de um objeto de configuração de fluxo que contém as configurações de formato.</span><span class="sxs-lookup"><span data-stu-id="e423f-143">When you retrieve a codec format, you get the [**IWMStreamConfig**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig) interface of a stream configuration object containing the format settings.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e423f-144">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="e423f-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e423f-145">**Obtendo informações de configuração de fluxo de codecs**</span><span class="sxs-lookup"><span data-stu-id="e423f-145">**Getting Stream Configuration Information from Codecs**</span></span>](getting-stream-configuration-information-from-codecs.md)
</dt> </dl>

 

 




