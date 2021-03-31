---
title: Lendo áudio de multicanal
description: Lendo áudio de multicanal
ms.assetid: 9d577c5c-7275-493e-8a77-318c264b59b3
keywords:
- Windows Media Format SDK, lendo áudio multicanal
- ASF (Advanced Systems Format), lendo áudio de multicanal
- ASF (formato de sistemas avançados), lendo áudio de multicanal
- ASF (Advanced Systems Format), áudio multicanal
- ASF (formato de sistemas avançados), áudio de multicanal
- codecs, lendo áudio de multicanal
- áudio de multicanal, lendo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59da950eb4218ad87995ed80e22de4de302f8e42
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103641638"
---
# <a name="reading-multichannel-audio"></a><span data-ttu-id="4aca4-110">Lendo áudio de multicanal</span><span class="sxs-lookup"><span data-stu-id="4aca4-110">Reading Multichannel Audio</span></span>

<span data-ttu-id="4aca4-111">O codec Windows Media Audio 9 Professional pode codificar áudio multicanal (mais de dois canais).</span><span class="sxs-lookup"><span data-stu-id="4aca4-111">The Windows Media Audio 9 Professional codec can encode multichannel audio (more than two channels).</span></span> <span data-ttu-id="4aca4-112">Ao ler um arquivo com áudio multicanal, você deve configurar a saída corretamente ou o áudio será entregue em uma qualidade menor e em estéreo.</span><span class="sxs-lookup"><span data-stu-id="4aca4-112">When reading a file with multichannel audio, you must configure the output properly or the audio will be delivered at a lower quality and in stereo.</span></span> <span data-ttu-id="4aca4-113">Para definir uma saída para entrega de áudio multicanal, você deve definir duas configurações de saída: g \_ wszEnableDiscreteOutput e g \_ wszSpeakerConfig.</span><span class="sxs-lookup"><span data-stu-id="4aca4-113">To set an output for multichannel audio delivery, you must set two output settings: g\_wszEnableDiscreteOutput and g\_wszSpeakerConfig.</span></span>

<span data-ttu-id="4aca4-114">A definição \_ de g wszEnableDiscreteOutput como **true** define o codec para fornecer saída de áudio de alta definição.</span><span class="sxs-lookup"><span data-stu-id="4aca4-114">Setting g\_wszEnableDiscreteOutput to **TRUE** sets the codec to deliver high-definition audio output.</span></span> <span data-ttu-id="4aca4-115">Áudio de alta definição é codificado pelo codec do Windows Media Audio 9 com amostras de 24 bits em estéreo ou vários canais.</span><span class="sxs-lookup"><span data-stu-id="4aca4-115">High-definition audio is encoded by the Windows Media Audio 9 codec with 24-bit samples in stereo or multiple channels.</span></span> <span data-ttu-id="4aca4-116">Se essa configuração for **falsa**, somente a saída estéreo de 16 bits será entregue.</span><span class="sxs-lookup"><span data-stu-id="4aca4-116">If this setting is **FALSE**, only 16-bit stereo output will be delivered.</span></span>

<span data-ttu-id="4aca4-117">O número de alto-falantes no computador de jogo é definido com g \_ wszSpeakerConfig.</span><span class="sxs-lookup"><span data-stu-id="4aca4-117">The number of speakers on the playing computer is set with g\_wszSpeakerConfig.</span></span> <span data-ttu-id="4aca4-118">Essa configuração é um valor **DWORD** definido como uma das constantes de alto-falante DirectSound listadas na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="4aca4-118">This setting is a **DWORD** value set to one of the DirectSound speaker constants listed in the following table.</span></span> <span data-ttu-id="4aca4-119">Para resolver esses nomes de constantes para seu compilador, você deve incluir dsound. h.</span><span class="sxs-lookup"><span data-stu-id="4aca4-119">To resolve these constant names for your compiler, you must include dsound.h.</span></span>



| <span data-ttu-id="4aca4-120">Constante</span><span class="sxs-lookup"><span data-stu-id="4aca4-120">Constant</span></span>             | <span data-ttu-id="4aca4-121">Valor</span><span class="sxs-lookup"><span data-stu-id="4aca4-121">Value</span></span>      | <span data-ttu-id="4aca4-122">Descrição</span><span class="sxs-lookup"><span data-stu-id="4aca4-122">Description</span></span>                                                                  |
|----------------------|------------|------------------------------------------------------------------------------|
| <span data-ttu-id="4aca4-123">DSSPEAKER \_ directout</span><span class="sxs-lookup"><span data-stu-id="4aca4-123">DSSPEAKER\_DIRECTOUT</span></span> | <span data-ttu-id="4aca4-124">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4aca4-124">0x00000000</span></span> | <span data-ttu-id="4aca4-125">O áudio é transmitido diretamente, sem ser configurado para os alto-falantes.</span><span class="sxs-lookup"><span data-stu-id="4aca4-125">The audio is passed through directly, without being configured for speakers.</span></span> |
| <span data-ttu-id="4aca4-126">\_fone de ouvido DSSPEAKER</span><span class="sxs-lookup"><span data-stu-id="4aca4-126">DSSPEAKER\_HEADPHONE</span></span> | <span data-ttu-id="4aca4-127">0x00000001</span><span class="sxs-lookup"><span data-stu-id="4aca4-127">0x00000001</span></span> | <span data-ttu-id="4aca4-128">O computador cliente está equipado com fones de ouvido.</span><span class="sxs-lookup"><span data-stu-id="4aca4-128">The client computer is equipped with headphones.</span></span>                             |
| <span data-ttu-id="4aca4-129">DSSPEAKER \_ mono</span><span class="sxs-lookup"><span data-stu-id="4aca4-129">DSSPEAKER\_MONO</span></span>      | <span data-ttu-id="4aca4-130">0x00000002</span><span class="sxs-lookup"><span data-stu-id="4aca4-130">0x00000002</span></span> | <span data-ttu-id="4aca4-131">O computador cliente está equipado com um monaural palestrante.</span><span class="sxs-lookup"><span data-stu-id="4aca4-131">The client computer is equipped with a monaural speaker.</span></span>                     |
| <span data-ttu-id="4aca4-132">DSSPEAKER \_ Quad</span><span class="sxs-lookup"><span data-stu-id="4aca4-132">DSSPEAKER\_QUAD</span></span>      | <span data-ttu-id="4aca4-133">0x00000003</span><span class="sxs-lookup"><span data-stu-id="4aca4-133">0x00000003</span></span> | <span data-ttu-id="4aca4-134">O computador cliente está equipado com alto-falantes Quadraphonic.</span><span class="sxs-lookup"><span data-stu-id="4aca4-134">The client computer is equipped with quadraphonic speakers.</span></span>                  |
| <span data-ttu-id="4aca4-135">estéreo de DSSPEAKER \_</span><span class="sxs-lookup"><span data-stu-id="4aca4-135">DSSPEAKER\_STEREO</span></span>    | <span data-ttu-id="4aca4-136">0x00000004</span><span class="sxs-lookup"><span data-stu-id="4aca4-136">0x00000004</span></span> | <span data-ttu-id="4aca4-137">O computador cliente está equipado com alto-falantes estéreo.</span><span class="sxs-lookup"><span data-stu-id="4aca4-137">The client computer is equipped with stereo speakers.</span></span>                        |
| <span data-ttu-id="4aca4-138">\_surround DSSPEAKER</span><span class="sxs-lookup"><span data-stu-id="4aca4-138">DSSPEAKER\_SURROUND</span></span>  | <span data-ttu-id="4aca4-139">0x00000005</span><span class="sxs-lookup"><span data-stu-id="4aca4-139">0x00000005</span></span> | <span data-ttu-id="4aca4-140">O computador cliente está equipado com alto-falantes surround-sound.</span><span class="sxs-lookup"><span data-stu-id="4aca4-140">The client computer is equipped with four-channel surround-sound speakers.</span></span>   |
| <span data-ttu-id="4aca4-141">DSSPEAKER \_ 5POINT1</span><span class="sxs-lookup"><span data-stu-id="4aca4-141">DSSPEAKER\_5POINT1</span></span>   | <span data-ttu-id="4aca4-142">0x00000006</span><span class="sxs-lookup"><span data-stu-id="4aca4-142">0x00000006</span></span> | <span data-ttu-id="4aca4-143">O computador cliente é equipado com cinco alto-falantes e um subwoofer.</span><span class="sxs-lookup"><span data-stu-id="4aca4-143">The client computer is equipped with five speakers and a subwoofer.</span></span>          |
| <span data-ttu-id="4aca4-144">DSSPEAKER \_ 7POINT1</span><span class="sxs-lookup"><span data-stu-id="4aca4-144">DSSPEAKER\_7POINT1</span></span>   | <span data-ttu-id="4aca4-145">0x00000007</span><span class="sxs-lookup"><span data-stu-id="4aca4-145">0x00000007</span></span> | <span data-ttu-id="4aca4-146">O computador cliente está equipado com sete palestrantes e um subwoofer.</span><span class="sxs-lookup"><span data-stu-id="4aca4-146">The client computer is equipped with seven speakers and a subwoofer.</span></span>         |



 

<span data-ttu-id="4aca4-147">Para definir essas configurações, use [**IWMReaderAdvanced2:: SetOutputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setoutputsetting).</span><span class="sxs-lookup"><span data-stu-id="4aca4-147">To set these settings, use [**IWMReaderAdvanced2::SetOutputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setoutputsetting).</span></span>

<span data-ttu-id="4aca4-148">Por fim, para que os canais sejam impressos de forma discreta, sem dobra para estéreo, você deve definir o tipo de mídia correto na saída seguindo estas etapas:</span><span class="sxs-lookup"><span data-stu-id="4aca4-148">Finally, for the channels to be output discretely, with no fold-down to stereo, you must set the correct media type on the output by following these steps:</span></span>

1.  <span data-ttu-id="4aca4-149">Chame [**IWMReader:: GetOutputFormatCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreader-getoutputformatcount) para obter o número de formatos com suporte para a saída de áudio relevante.</span><span class="sxs-lookup"><span data-stu-id="4aca4-149">Call [**IWMReader::GetOutputFormatCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreader-getoutputformatcount) to get the number of supported formats for the relevant audio output.</span></span> <span data-ttu-id="4aca4-150">Os índices de formato de saída são baseados em zero.</span><span class="sxs-lookup"><span data-stu-id="4aca4-150">Output format indexes are zero-based.</span></span>
2.  <span data-ttu-id="4aca4-151">Para cada formato com suporte, chame [**IWMReader:: GetOutputFormat**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-getoutputformat) para recuperar a interface [**IWMOutputMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmoutputmediaprops) no objeto de propriedades de mídia de saída.</span><span class="sxs-lookup"><span data-stu-id="4aca4-151">For each supported format, call [**IWMReader::GetOutputFormat**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-getoutputformat) to retrieve the [**IWMOutputMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmoutputmediaprops) interface on the output media properties object.</span></span>
3.  <span data-ttu-id="4aca4-152">Chame [**IWMMediaProps:: GetMediaType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmediaprops-getmediatype) para recuperar o tipo de mídia.</span><span class="sxs-lookup"><span data-stu-id="4aca4-152">Call [**IWMMediaProps::GetMediaType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmediaprops-getmediatype) to retrieve the media type.</span></span>
4.  <span data-ttu-id="4aca4-153">Se o tipo de mídia recuperado for o tipo de multicanal desejado, defina-o chamando [**IWMReader:: SetOutputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-setoutputprops).</span><span class="sxs-lookup"><span data-stu-id="4aca4-153">If the retrieved media type is the desired multichannel type, then set it by calling [**IWMReader::SetOutputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-setoutputprops).</span></span>

<span data-ttu-id="4aca4-154">Depois de definir a saída discreta e a configuração do alto-falante, os formatos de saída enumerados pelo leitor devem incluir formatos multicanal que usam a estrutura [**WAVEFORMATEXTENSIBLE**](/previous-versions/windows/desktop/legacy/dd757721(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="4aca4-154">After you have set discrete output and the speaker configuration, the output formats enumerated by the reader should include multichannel formats that use the [**WAVEFORMATEXTENSIBLE**](/previous-versions/windows/desktop/legacy/dd757721(v=vs.85)) structure.</span></span> <span data-ttu-id="4aca4-155">Se você enumerar os formatos de saída antes de definir as propriedades, somente os formatos com 1 ou 2 canais e um máximo de 16 bits por canal serão incluídos.</span><span class="sxs-lookup"><span data-stu-id="4aca4-155">If you enumerate the output formats before setting the properties, only formats with 1 or 2 channels and a maximum of 16 bits per channel will be included.</span></span> <span data-ttu-id="4aca4-156">Assim como acontece com outros formatos de áudio, você deve usar apenas os formatos enumerados pelo leitor; Não configure seu próprio.</span><span class="sxs-lookup"><span data-stu-id="4aca4-156">As with other audio formats, you should use only the formats enumerated by the reader; do not configure your own.</span></span>

> [!Note]  
> <span data-ttu-id="4aca4-157">Você poderá produzir áudio multicanal somente se seu aplicativo estiver em execução no Microsoft Windows XP ou em uma versão posterior do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="4aca4-157">You can output multichannel audio only if your application is running on Microsoft Windows XP or a later version of Microsoft Windows.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="4aca4-158">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="4aca4-158">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4aca4-159">**Entradas, fluxos e saídas**</span><span class="sxs-lookup"><span data-stu-id="4aca4-159">**Inputs, Streams and Outputs**</span></span>](inputs-streams-and-outputs.md)
</dt> <dt>

[<span data-ttu-id="4aca4-160">**Lendo arquivos ASF**</span><span class="sxs-lookup"><span data-stu-id="4aca4-160">**Reading ASF Files**</span></span>](reading-asf-files.md)
</dt> <dt>

[<span data-ttu-id="4aca4-161">**Configurações de saída**</span><span class="sxs-lookup"><span data-stu-id="4aca4-161">**Output Settings**</span></span>](output-settings.md)
</dt> <dt>

[<span data-ttu-id="4aca4-162">**Trabalhando com High-Resolution áudio PCM**</span><span class="sxs-lookup"><span data-stu-id="4aca4-162">**Working with High-Resolution PCM Audio**</span></span>](working-with-high-resolution-pcm-audio.md)
</dt> </dl>

 

 