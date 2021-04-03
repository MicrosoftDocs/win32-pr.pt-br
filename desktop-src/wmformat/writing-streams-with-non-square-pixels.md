---
title: Gravando fluxos com pixels não quadrados
description: Gravando fluxos com pixels não quadrados
ms.assetid: 4af7dedc-e2b8-4dc2-add4-84424e93c297
keywords:
- Windows Media Format SDK, gravando fluxos de vídeo
- SDK do Windows Media Format, fluxos de vídeo
- SDK do Windows Media Format, pixels não quadrados
- SDK do Windows Media Format, pixels (não quadrado)
- ASF (Advanced Systems Format), gravando fluxos de vídeo
- ASF (formato de sistemas avançados), gravando fluxos de vídeo
- ASF (Advanced Systems Format), fluxos de vídeo
- ASF (formato de sistemas avançados), fluxos de vídeo
- ASF (Advanced Systems Format), pixels não quadrados
- ASF (formato de sistemas avançados), pixels não quadrados
- ASF (Advanced Systems Format), pixels (não quadrado)
- ASF (formato de sistemas avançados), pixels (não quadrado)
- gravando fluxos de vídeo
- fluxos de vídeo, gravando
- fluxos de vídeo, pixels não quadrados
- pixels não quadrados
- pixels (não quadrado)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1349840f151ab787ba0e0512cfab8fea08aacf1
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104007105"
---
# <a name="writing-streams-with-non-square-pixels"></a><span data-ttu-id="7d3dd-120">Gravando fluxos com pixels não quadrados</span><span class="sxs-lookup"><span data-stu-id="7d3dd-120">Writing Streams with Non-Square Pixels</span></span>

<span data-ttu-id="7d3dd-121">Há duas maneiras de criar fluxos de vídeo com pixels não quadrados que serão exibidos corretamente no Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="7d3dd-121">There are two ways to create video streams with non-square pixels that will be displayed correctly in Windows Media Player.</span></span> <span data-ttu-id="7d3dd-122">A primeira técnica envolve a definição de atributos de nível de fluxo no cabeçalho do arquivo.</span><span class="sxs-lookup"><span data-stu-id="7d3dd-122">The first technique involves setting stream-level attributes in the file header.</span></span> <span data-ttu-id="7d3dd-123">A segunda técnica envolve adicionar uma extensão de unidade de dados a um fluxo no perfil e, em seguida, definir um valor para ela em cada exemplo que é gravada.</span><span class="sxs-lookup"><span data-stu-id="7d3dd-123">The second technique involves adding a data unit extension to a stream in the profile, and then setting a value for it in every sample that is written.</span></span>

## <a name="to-use-stream-level-header-attributes-to-set-pixel-aspect-ratio"></a><span data-ttu-id="7d3dd-124">Para usar atributos de cabeçalho no nível de fluxo para definir a taxa de proporção de pixel</span><span class="sxs-lookup"><span data-stu-id="7d3dd-124">To Use Stream-level Header Attributes to Set Pixel Aspect Ratio</span></span>

1.  <span data-ttu-id="7d3dd-125">Configure o objeto gravador.</span><span class="sxs-lookup"><span data-stu-id="7d3dd-125">Set up the writer object.</span></span> <span data-ttu-id="7d3dd-126">Para obter mais informações, consulte [Writing ASF files](writing-asf-files.md).</span><span class="sxs-lookup"><span data-stu-id="7d3dd-126">For more information, see [Writing ASF Files](writing-asf-files.md).</span></span>
2.  <span data-ttu-id="7d3dd-127">Crie ou carregue um perfil com um ou mais fluxos de vídeo.</span><span class="sxs-lookup"><span data-stu-id="7d3dd-127">Create or load a profile with one or more video streams.</span></span> <span data-ttu-id="7d3dd-128">Para obter mais informações, consulte [para usar perfis com o gravador](to-use-profiles-with-the-writer.md).</span><span class="sxs-lookup"><span data-stu-id="7d3dd-128">For more information, see [To Use Profiles with the Writer](to-use-profiles-with-the-writer.md).</span></span>
3.  <span data-ttu-id="7d3dd-129">Chame [**IWMWriter:: setprofile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setprofile).</span><span class="sxs-lookup"><span data-stu-id="7d3dd-129">Call [**IWMWriter::SetProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setprofile).</span></span> <span data-ttu-id="7d3dd-130">(Sempre Chame esse método antes de definir qualquer atributo de cabeçalho.)</span><span class="sxs-lookup"><span data-stu-id="7d3dd-130">(Always call this method before setting any header attributes.)</span></span>
4.  <span data-ttu-id="7d3dd-131">Chame **QueryInterface** para obter a interface [**IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3) e chame [**AddAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-addattribute) duas vezes para adicionar [**AspectRatioX**](aspectratiox.md) e [**AspectRatioY**](aspectratioy.md) como atributos de nível de fluxo do fluxo de vídeo.</span><span class="sxs-lookup"><span data-stu-id="7d3dd-131">Call **QueryInterface** to obtain the [**IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3) interface and call [**AddAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-addattribute) twice to add [**AspectRatioX**](aspectratiox.md) and [**AspectRatioY**](aspectratioy.md) as stream-level attributes of the video stream.</span></span> <span data-ttu-id="7d3dd-132">Esses atributos são valores **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="7d3dd-132">These attributes are **DWORD** values.</span></span>
5.  <span data-ttu-id="7d3dd-133">Grave o arquivo.</span><span class="sxs-lookup"><span data-stu-id="7d3dd-133">Write the file.</span></span>

## <a name="to-use-data-unit-extensions-to-set-pixel-aspect-ratio"></a><span data-ttu-id="7d3dd-134">Para usar extensões de unidade de dados para definir a taxa de proporção de pixel</span><span class="sxs-lookup"><span data-stu-id="7d3dd-134">To Use Data Unit Extensions to Set Pixel Aspect Ratio</span></span>

<span data-ttu-id="7d3dd-135">**Antes de escrever:**</span><span class="sxs-lookup"><span data-stu-id="7d3dd-135">**Before writing:**</span></span>

1.  <span data-ttu-id="7d3dd-136">Configure o objeto gravador.</span><span class="sxs-lookup"><span data-stu-id="7d3dd-136">Set up the writer object.</span></span> <span data-ttu-id="7d3dd-137">Para obter mais informações, consulte [Writing ASF files](writing-asf-files.md).</span><span class="sxs-lookup"><span data-stu-id="7d3dd-137">For more information, see [Writing ASF Files](writing-asf-files.md).</span></span>
2.  <span data-ttu-id="7d3dd-138">Crie ou carregue um perfil com um ou mais fluxos de vídeo.</span><span class="sxs-lookup"><span data-stu-id="7d3dd-138">Create or load a profile with one or more video streams.</span></span> <span data-ttu-id="7d3dd-139">Para obter mais informações, consulte [para usar perfis com o gravador](to-use-profiles-with-the-writer.md).</span><span class="sxs-lookup"><span data-stu-id="7d3dd-139">For more information, see [To Use Profiles with the Writer](to-use-profiles-with-the-writer.md).</span></span>
3.  <span data-ttu-id="7d3dd-140">Para cada fluxo (de qualquer tipo de mídia) no perfil, chame [**IWMStreamConfig:: Setstreamname**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig-setstreamname) para especificar um nome exclusivo de sua escolha.</span><span class="sxs-lookup"><span data-stu-id="7d3dd-140">For each stream (of any media type) in the profile, call [**IWMStreamConfig::SetStreamName**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig-setstreamname) to specify a unique name of your choice.</span></span> <span data-ttu-id="7d3dd-141">Não dê ao mesmo nome dois fluxos.</span><span class="sxs-lookup"><span data-stu-id="7d3dd-141">Do not give two streams the same name.</span></span>
4.  <span data-ttu-id="7d3dd-142">Use [**IWMStreamConfig2:: AddDataUnitExtension**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-adddataunitextension) no fluxo de vídeo para adicionar uma extensão de unidade de dados para taxa de proporção de pixel.</span><span class="sxs-lookup"><span data-stu-id="7d3dd-142">Use [**IWMStreamConfig2::AddDataUnitExtension**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-adddataunitextension) on the video stream to add a data unit extension for pixel aspect ratio.</span></span>
5.  <span data-ttu-id="7d3dd-143">Chame [**IWMWriter:: setprofile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setprofile).</span><span class="sxs-lookup"><span data-stu-id="7d3dd-143">Call [**IWMWriter::SetProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setprofile).</span></span>
6.  <span data-ttu-id="7d3dd-144">Grave o arquivo.</span><span class="sxs-lookup"><span data-stu-id="7d3dd-144">Write the file.</span></span>

<span data-ttu-id="7d3dd-145">**Durante a gravação:**</span><span class="sxs-lookup"><span data-stu-id="7d3dd-145">**While writing:**</span></span>

-   <span data-ttu-id="7d3dd-146">Para cada exemplo, chame [**INSSBuffer3:: SetProperty**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer3-setproperty) e especifique a \_ Propriedade PixelAspectRatio do WM SampleExtensionGUID \_ juntamente com o valor correto.</span><span class="sxs-lookup"><span data-stu-id="7d3dd-146">For each sample, call [**INSSBuffer3::SetProperty**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer3-setproperty) and specify the WM\_SampleExtensionGUID\_PixelAspectRatio property along with the correct value.</span></span> <span data-ttu-id="7d3dd-147">Os valores de taxa de proporção são gravados como dois valores de dois dígitos concatenados.</span><span class="sxs-lookup"><span data-stu-id="7d3dd-147">Aspect ratio values are written as two concatenated two-digit values.</span></span> <span data-ttu-id="7d3dd-148">Por exemplo, 16:9 é escrito como 1609 ou 0x0649.</span><span class="sxs-lookup"><span data-stu-id="7d3dd-148">For example, 16:9 is written as 1609 or 0x0649.</span></span> <span data-ttu-id="7d3dd-149">Esse é sempre um valor de 2 bytes.</span><span class="sxs-lookup"><span data-stu-id="7d3dd-149">This is always a 2-byte value.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7d3dd-150">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="7d3dd-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7d3dd-151">**Para ler e gravar fluxos de vídeo com pixels não quadrados**</span><span class="sxs-lookup"><span data-stu-id="7d3dd-151">**To Read and Write Video Streams with Non-Square Pixels**</span></span>](to-read-and-write-video-streams-with-non-square-pixels.md)
</dt> </dl>

 

 




