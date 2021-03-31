---
title: Para transcodificar conteúdo com recompactação inteligente
description: Para transcodificar conteúdo com recompactação inteligente
ms.assetid: 02398462-b0a4-4a17-84e3-4c6f9f26639f
keywords:
- SDK do Windows Media Format, transcodificação de conteúdo
- SDK do Windows Media Format, recompactação inteligente
- SDK do Windows Media Format, recompactação
- SDK do Windows Media Format, codecs de áudio do Windows Media
- Formato de sistema avançado (ASF), transcodificação de conteúdo
- ASF (formato de sistemas avançados), transcodificação de conteúdo
- Formato de sistema avançado (ASF), recompactação inteligente
- ASF (formato de sistemas avançados), recompactação inteligente
- Formato de sistema avançado (ASF), recompactação
- ASF (formato de sistemas avançados), recompactação
- Formato de sistema avançado (ASF), codecs de áudio do Windows Media
- ASF (formato de sistemas avançados), codecs de áudio do Windows Media
- transcodificação de conteúdo
- recompactação inteligente
- recompactação
- Codecs de áudio do Windows Media, transcodificação de conteúdo
- codecs, codecs de áudio do Windows Media
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a1317989ea9384d4a9747d712af1ce5c61d484c
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104293778"
---
# <a name="to-transcode-content-with-smart-recompression"></a><span data-ttu-id="4ceb9-120">Para transcodificar conteúdo com recompactação inteligente</span><span class="sxs-lookup"><span data-stu-id="4ceb9-120">To Transcode Content with Smart Recompression</span></span>

<span data-ttu-id="4ceb9-121">Você pode transcodificar o conteúdo de uma taxa de bits para outra usando o SDK do Windows Media Format.</span><span class="sxs-lookup"><span data-stu-id="4ceb9-121">You can transcode content from one bit rate to another using the Windows Media Format SDK.</span></span> <span data-ttu-id="4ceb9-122">Normalmente, isso envolve simplesmente decodificar o conteúdo e codificá-lo novamente para a taxa de bits desejada.</span><span class="sxs-lookup"><span data-stu-id="4ceb9-122">Normally, this involves simply decoding the content and encoding it again to the desired bit rate.</span></span> <span data-ttu-id="4ceb9-123">O codec Windows Media Audio 9 dá suporte à recompactação inteligente, o que permite transcodificação que atinge uma qualidade melhor do que o normal.</span><span class="sxs-lookup"><span data-stu-id="4ceb9-123">The Windows Media Audio 9 codec supports smart recompression, which enables transcoding that achieves better quality than normal.</span></span>

<span data-ttu-id="4ceb9-124">Para a recompactação inteligente, o fluxo de áudio original deve ser codificado com o codec de áudio do Windows Media.</span><span class="sxs-lookup"><span data-stu-id="4ceb9-124">For smart recompression, the original audio stream must be encoded with the Windows Media Audio codec.</span></span> <span data-ttu-id="4ceb9-125">Todas as versões do codec têm suporte, mas os codecs de áudio especializados (Windows Media Audio 9 Professional e Windows Media Audio 9 Voice) não são.</span><span class="sxs-lookup"><span data-stu-id="4ceb9-125">All versions of the codec are supported, but the specialized audio codecs (Windows Media Audio 9 Professional and Windows Media Audio 9 Voice) are not.</span></span> <span data-ttu-id="4ceb9-126">Se o áudio original foi codificado com o codec Windows Media Audio 9 sem perdas, não há necessidade de usar a recompactação inteligente, pois nenhuma informação foi perdida na codificação original.</span><span class="sxs-lookup"><span data-stu-id="4ceb9-126">If the original audio was encoded with the Windows Media Audio 9 Lossless codec, there is no need to use smart recompression, because no information was lost in the original encoding.</span></span>

<span data-ttu-id="4ceb9-127">Para usar a recompactação inteligente, execute as etapas a seguir.</span><span class="sxs-lookup"><span data-stu-id="4ceb9-127">To use smart recompression, perform the following steps.</span></span>

1.  <span data-ttu-id="4ceb9-128">Configure um objeto de leitor com o arquivo de origem para leitura.</span><span class="sxs-lookup"><span data-stu-id="4ceb9-128">Set up a reader object with the source file for reading.</span></span> <span data-ttu-id="4ceb9-129">Para obter mais informações, consulte [lendo arquivos ASF](reading-asf-files.md).</span><span class="sxs-lookup"><span data-stu-id="4ceb9-129">For more information, see [Reading ASF Files](reading-asf-files.md).</span></span>
2.  <span data-ttu-id="4ceb9-130">Configure um objeto gravador a ser usado para transcodificar o arquivo.</span><span class="sxs-lookup"><span data-stu-id="4ceb9-130">Set up a writer object to use for transcoding the file.</span></span> <span data-ttu-id="4ceb9-131">Defina o nome do arquivo para o novo arquivo.</span><span class="sxs-lookup"><span data-stu-id="4ceb9-131">Set the file name for the new file.</span></span> <span data-ttu-id="4ceb9-132">Selecione um perfil a ser usado para o novo arquivo.</span><span class="sxs-lookup"><span data-stu-id="4ceb9-132">Select a profile to use for the new file.</span></span> <span data-ttu-id="4ceb9-133">Defina o perfil selecionado no objeto gravador.</span><span class="sxs-lookup"><span data-stu-id="4ceb9-133">Set the selected profile in the writer object.</span></span> <span data-ttu-id="4ceb9-134">Para obter mais informações, consulte [Writing ASF files](writing-asf-files.md).</span><span class="sxs-lookup"><span data-stu-id="4ceb9-134">For more information, see [Writing ASF Files](writing-asf-files.md).</span></span>
3.  <span data-ttu-id="4ceb9-135">Obtenha um ponteiro para a interface [**IWMProfile**](iwmprofile.md) do objeto leitor chamando **IWMReader:: QueryInterface**.</span><span class="sxs-lookup"><span data-stu-id="4ceb9-135">Get a pointer to the [**IWMProfile**](iwmprofile.md) interface of the reader object by calling **IWMReader::QueryInterface**.</span></span>
4.  <span data-ttu-id="4ceb9-136">Recupere a interface [**IWMStreamConfig**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig) para que o fluxo de áudio seja transcodificado chamando [**IWMProfile:: GetStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getstream).</span><span class="sxs-lookup"><span data-stu-id="4ceb9-136">Retrieve the [**IWMStreamConfig**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig) interface for the audio stream to be transcoded by calling [**IWMProfile::GetStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getstream).</span></span>
5.  <span data-ttu-id="4ceb9-137">Obtenha a interface [**IWMMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmediaprops) para o objeto de configuração de fluxo chamando **IWMStreamConfig:: QueryInterface**.</span><span class="sxs-lookup"><span data-stu-id="4ceb9-137">Get the [**IWMMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmediaprops) interface for the stream configuration object by calling **IWMStreamConfig::QueryInterface**.</span></span>
6.  <span data-ttu-id="4ceb9-138">Recupere a estrutura do [**\_ \_ tipo de mídia do WM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) para o fluxo fazendo duas chamadas para [**IWMMediaProps:: GetMediaType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmediaprops-getmediatype).</span><span class="sxs-lookup"><span data-stu-id="4ceb9-138">Retrieve the [**WM\_MEDIA\_TYPE**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) structure for the stream by making two calls to [**IWMMediaProps::GetMediaType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmediaprops-getmediatype).</span></span> <span data-ttu-id="4ceb9-139">Obtenha o tamanho da estrutura na primeira chamada e aloque a memória de um buffer para passar na segunda chamada.</span><span class="sxs-lookup"><span data-stu-id="4ceb9-139">Get the size of the structure on the first call, and allocate memory for a buffer to pass on the second call.</span></span>
7.  <span data-ttu-id="4ceb9-140">Obtenha um ponteiro para a interface [**IWMInputMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwminputmediaprops) para a entrada no gravador chamando [**IWMWriter:: GetInputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-getinputprops).</span><span class="sxs-lookup"><span data-stu-id="4ceb9-140">Get a pointer to the [**IWMInputMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwminputmediaprops) interface for the input in the writer by calling [**IWMWriter::GetInputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-getinputprops).</span></span>
8.  <span data-ttu-id="4ceb9-141">Obtenha a interface [**IWMPropertyVault**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpropertyvault) para o objeto de propriedades de mídia de entrada chamando **IWMInputMediaProps:: QueryInterface**.</span><span class="sxs-lookup"><span data-stu-id="4ceb9-141">Get the [**IWMPropertyVault**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpropertyvault) interface for the input media properties object by calling **IWMInputMediaProps::QueryInterface**.</span></span>
9.  <span data-ttu-id="4ceb9-142">Use o método [**IWMPropertyVault:: SetProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmpropertyvault-setproperty) para definir a \_ Propriedade g wszOriginalWaveFormat.</span><span class="sxs-lookup"><span data-stu-id="4ceb9-142">Use the [**IWMPropertyVault::SetProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmpropertyvault-setproperty) method to set the g\_wszOriginalWaveFormat property.</span></span> <span data-ttu-id="4ceb9-143">Use a estrutura **WAVEFORMATEX** obtida na etapa 6 como o valor da propriedade.</span><span class="sxs-lookup"><span data-stu-id="4ceb9-143">Use the **WAVEFORMATEX** structure obtained in step 6 as the value of the property.</span></span>
10. <span data-ttu-id="4ceb9-144">Inclua alterações feitas nas propriedades de mídia de entrada chamando [**IWMWriter:: SetInputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setinputprops) e passando um ponteiro para a interface **IWMInputMediaProps** .</span><span class="sxs-lookup"><span data-stu-id="4ceb9-144">Include changes made to the input media properties by calling [**IWMWriter::SetInputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setinputprops) and passing it a pointer to the **IWMInputMediaProps** interface.</span></span>
11. <span data-ttu-id="4ceb9-145">Comece a ler exemplos do arquivo original e passá-los para o gravador com chamadas para [**IWMWriter:: WriteSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-writesample).</span><span class="sxs-lookup"><span data-stu-id="4ceb9-145">Begin reading samples from the original file and passing them to the writer with calls to [**IWMWriter::WriteSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-writesample).</span></span>

## <a name="related-topics"></a><span data-ttu-id="4ceb9-146">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="4ceb9-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4ceb9-147">**Tópicos avançados**</span><span class="sxs-lookup"><span data-stu-id="4ceb9-147">**Advanced Topics**</span></span>](advanced-topics.md)
</dt> <dt>

[<span data-ttu-id="4ceb9-148">**Interface IWMInputMediaProps**</span><span class="sxs-lookup"><span data-stu-id="4ceb9-148">**IWMInputMediaProps Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwminputmediaprops)
</dt> <dt>

[<span data-ttu-id="4ceb9-149">**Interface IWMMediaProps**</span><span class="sxs-lookup"><span data-stu-id="4ceb9-149">**IWMMediaProps Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmediaprops)
</dt> <dt>

[<span data-ttu-id="4ceb9-150">**Interface IWMProfile**</span><span class="sxs-lookup"><span data-stu-id="4ceb9-150">**IWMProfile Interface**</span></span>](iwmprofile.md)
</dt> <dt>

[<span data-ttu-id="4ceb9-151">**Interface IWMPropertyVault**</span><span class="sxs-lookup"><span data-stu-id="4ceb9-151">**IWMPropertyVault Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpropertyvault)
</dt> <dt>

[<span data-ttu-id="4ceb9-152">**Interface IWMStreamConfig**</span><span class="sxs-lookup"><span data-stu-id="4ceb9-152">**IWMStreamConfig Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig)
</dt> </dl>

 

 




