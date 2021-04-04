---
title: Para usar vídeo entrelaçado
description: Para usar vídeo entrelaçado
ms.assetid: cb77bac7-bea8-4f1b-8302-fee9a43d4815
keywords:
- SDK do Windows Media Format, vídeo entrelaçado
- SDK do Windows Media Format, codificação de vídeo entrelaçada
- SDK de formato de mídia do Windows, vídeo entrelaçado de codificação
- SDK do Windows Media Format, decodificando vídeo entrelaçado
- Windows Media Format SDK, ordem de campo
- ASF (Advanced Systems Format), vídeo entrelaçado
- ASF (formato de sistemas avançados), vídeo entrelaçado
- ASF (Advanced Systems Format), codificação de vídeo entrelaçado
- ASF (formato de sistemas avançados), codificação de vídeo entrelaçado
- ASF (Advanced Systems Format), vídeo entrelaçado de codificação
- ASF (formato de sistemas avançados), vídeo entrelaçado de codificação
- Formato de sistema avançado (ASF), decodificação de vídeo entrelaçado
- ASF (formato de sistemas avançados), decodificando vídeo entrelaçado
- Formato de sistema avançado (ASF), ordem de campo
- ASF (formato de sistemas avançados), ordem de campo
- vídeo entrelaçado, sobre
- vídeo entrelaçado, codificação
- vídeo entrelaçado, decodificação
- vídeo entrelaçado, ordem de campo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a093ddd6d9d9487ffcd4b73e1f5c75b849cdcdc1
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "103823568"
---
# <a name="to-use-interlaced-video"></a><span data-ttu-id="b7ac7-122">Para usar vídeo entrelaçado</span><span class="sxs-lookup"><span data-stu-id="b7ac7-122">To Use Interlaced Video</span></span>

<span data-ttu-id="b7ac7-123">Há dois tipos básicos de codificação de vídeo: progressivo e entrelaçado.</span><span class="sxs-lookup"><span data-stu-id="b7ac7-123">There are two basic types of video encoding: progressive and interlaced.</span></span> <span data-ttu-id="b7ac7-124">Na codificação progressiva, cada quadro é uma representação codificada de um quadro de vídeo.</span><span class="sxs-lookup"><span data-stu-id="b7ac7-124">In progressive encoding, each frame is an encoded representation of one frame of video.</span></span> <span data-ttu-id="b7ac7-125">Na codificação entrelaçada, cada quadro é uma representação codificada de todas as linhas pares de pixels no vídeo ou todas as linhas ímpares.</span><span class="sxs-lookup"><span data-stu-id="b7ac7-125">In interlaced encoding, each frame is an encoded representation of either all of the even rows of pixels in the video, or all of the odd rows.</span></span> <span data-ttu-id="b7ac7-126">Cada quadro entrelaçado é chamado de *campo*, portanto, há campos ímpares e até mesmo campos.</span><span class="sxs-lookup"><span data-stu-id="b7ac7-126">Each interlaced frame is called a *field*, so there are odd fields and even fields.</span></span> <span data-ttu-id="b7ac7-127">Uma exibição entrelaçada (como uma televisão) renderiza os campos um de cada vez, alternando campos.</span><span class="sxs-lookup"><span data-stu-id="b7ac7-127">An interlaced display (like a television) renders the fields one at a time, alternating fields.</span></span> <span data-ttu-id="b7ac7-128">Uma exibição progressiva renderiza quadros todos de uma vez.</span><span class="sxs-lookup"><span data-stu-id="b7ac7-128">A progressive display renders frames all at once.</span></span>

<span data-ttu-id="b7ac7-129">O codec de perfil avançado do Windows Media Video 9 fornece suporte para manter o entrelaçamento em fluxos compactados.</span><span class="sxs-lookup"><span data-stu-id="b7ac7-129">The Windows Media Video 9 Advanced Profile codec provides support for maintaining interlacing in compressed streams.</span></span>

## <a name="when-to-use-interlaced-video"></a><span data-ttu-id="b7ac7-130">Quando usar vídeo entrelaçado</span><span class="sxs-lookup"><span data-stu-id="b7ac7-130">When to Use Interlaced Video</span></span>

<span data-ttu-id="b7ac7-131">O vídeo entrelaçado de codificação só é útil quando o conteúdo é exibido em um dispositivo entrelaçado.</span><span class="sxs-lookup"><span data-stu-id="b7ac7-131">Encoding interlaced video is useful only when the content is displayed on an interlaced device.</span></span> <span data-ttu-id="b7ac7-132">O conteúdo que deve ser exibido em uma televisão (por meio de um conjunto de decodificador ou outro dispositivo) pode precisar ser entrelaçado.</span><span class="sxs-lookup"><span data-stu-id="b7ac7-132">Content that is intended to be viewed on a television (through a set-top box or other device) may need to be interlaced.</span></span> <span data-ttu-id="b7ac7-133">O conteúdo que se destina a ser exibido exclusivamente em uma exibição do computador não deve ser codificado como entrelaçado.</span><span class="sxs-lookup"><span data-stu-id="b7ac7-133">Content that is intended to be viewed exclusively on a computer display should not be encoded as interlaced.</span></span>

<span data-ttu-id="b7ac7-134">Para codificar vídeo entrelaçado como vídeo progressivo, você deve definir as configurações de entrada.</span><span class="sxs-lookup"><span data-stu-id="b7ac7-134">To encode interlaced video as progressive video, you must configure input settings.</span></span> <span data-ttu-id="b7ac7-135">Para obter mais informações, consulte [para desentrelaçar vídeo](to-deinterlace-video.md).</span><span class="sxs-lookup"><span data-stu-id="b7ac7-135">For more information, see [To Deinterlace Video](to-deinterlace-video.md).</span></span>

## <a name="field-order"></a><span data-ttu-id="b7ac7-136">Ordem de Campos</span><span class="sxs-lookup"><span data-stu-id="b7ac7-136">Field Order</span></span>

<span data-ttu-id="b7ac7-137">A maioria das fontes de vídeo entrelaçado, como cartões de captura de vídeo, fornece amostras de vídeo que incluem ambos os campos intercalados entre si.</span><span class="sxs-lookup"><span data-stu-id="b7ac7-137">Most sources of interlaced video, such as video capture cards, deliver video samples that include both fields interleaved with each other.</span></span> <span data-ttu-id="b7ac7-138">O resultado é como um quadro de vídeo completo, exceto que as linhas ímpares e pares são um pouco deslocadas no tempo.</span><span class="sxs-lookup"><span data-stu-id="b7ac7-138">The result is like a complete frame of video, except that the odd and even lines are shifted slightly in time.</span></span> <span data-ttu-id="b7ac7-139">Não há um padrão universal no qual o campo no exemplo de vídeo intercalado ocorre primeiro no tempo.</span><span class="sxs-lookup"><span data-stu-id="b7ac7-139">There is no universal standard as to which field in the interleaved video sample occurs first in time.</span></span>

<span data-ttu-id="b7ac7-140">Você deve permitir que os usuários especifiquem a ordem dos campos ao passar amostras entrelaçadas para seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="b7ac7-140">You should enable users to specify field order when passing interlaced samples to your application.</span></span>

## <a name="encoding-interlaced-video"></a><span data-ttu-id="b7ac7-141">Vídeo entrelaçado de codificação</span><span class="sxs-lookup"><span data-stu-id="b7ac7-141">Encoding Interlaced Video</span></span>

<span data-ttu-id="b7ac7-142">Para usar a codificação entrelaçada, execute as seguintes etapas:</span><span class="sxs-lookup"><span data-stu-id="b7ac7-142">To use interlaced encoding, perform the following steps:</span></span>

1.  <span data-ttu-id="b7ac7-143">Configure o fluxo de vídeo no perfil para usar a extensão de unidade de dados do tipo de conteúdo chamando o método [**IWMStreamConfig2:: AddDataUnitExtension**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-adddataunitextension) .</span><span class="sxs-lookup"><span data-stu-id="b7ac7-143">Configure the video stream in the profile to use the content type data unit extension by calling the [**IWMStreamConfig2::AddDataUnitExtension**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-adddataunitextension) method.</span></span> <span data-ttu-id="b7ac7-144">O GUID de extensão de exemplo para a extensão de tipo de conteúdo é WM \_ SampleExtensionsGUID \_ ContentType.</span><span class="sxs-lookup"><span data-stu-id="b7ac7-144">The sample extension GUID for the content type extension is WM\_SampleExtensionsGUID\_ContentType.</span></span>
2.  <span data-ttu-id="b7ac7-145">Defina o fluxo no perfil e configure o gravador com o perfil como normal.</span><span class="sxs-lookup"><span data-stu-id="b7ac7-145">Set the stream in the profile and configure the writer with the profile as normal.</span></span>
3.  <span data-ttu-id="b7ac7-146">Antes de passar amostras entrelaçadas para o gravador, chame o método [**IWMWriterAdvanced2:: SetInputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-setinputsetting) para definir a \_ configuração de entrada g wszInterlacedCoding como **true**.</span><span class="sxs-lookup"><span data-stu-id="b7ac7-146">Before passing interlaced samples to the writer, call the [**IWMWriterAdvanced2::SetInputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-setinputsetting) method to set the g\_wszInterlacedCoding input setting to **TRUE**.</span></span>
4.  <span data-ttu-id="b7ac7-147">Para cada amostra entrelaçada que você passa para o gravador, chame o método [**INSSBuffer3:: SetProperty**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer3-setproperty) para definir o tipo de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="b7ac7-147">For every interlaced sample that you pass to the writer, call the [**INSSBuffer3::SetProperty**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer3-setproperty) method to set the content type.</span></span> <span data-ttu-id="b7ac7-148">Os valores de tipo de conteúdo são combinações dos sinalizadores na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="b7ac7-148">Content type values are combinations of the flags in the following table.</span></span>



| <span data-ttu-id="b7ac7-149">Sinalizador</span><span class="sxs-lookup"><span data-stu-id="b7ac7-149">Flag</span></span>                         | <span data-ttu-id="b7ac7-150">Descrição</span><span class="sxs-lookup"><span data-stu-id="b7ac7-150">Description</span></span>                                                                                                                                                                                                                                                                                                                                                      |
|------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b7ac7-151">WM \_ CT \_ entrelaçado</span><span class="sxs-lookup"><span data-stu-id="b7ac7-151">WM\_CT\_INTERLACED</span></span>           | <span data-ttu-id="b7ac7-152">Sempre defina esse sinalizador ao codificar conteúdo entrelaçado.</span><span class="sxs-lookup"><span data-stu-id="b7ac7-152">Always set this flag when encoding interlaced content.</span></span> <span data-ttu-id="b7ac7-153">Se você usar esse sinalizador sem definir um sinalizador de ordem de campo ( \_ primeiro, o campo do WM CT \_ \_ na parte \_ \_ superior ou \_ \_ o primeiro campo do WM CT \_ ) o codec assumirá que o campo superior é primeiro.</span><span class="sxs-lookup"><span data-stu-id="b7ac7-153">If you use this flag without setting a field-order flag (WM\_CT\_BOTTOM\_FIELD\_FIRST or WM\_CT\_TOP\_FIELD\_FIRST) the codec will assume that the top field is first.</span></span> <span data-ttu-id="b7ac7-154">Se o codec usar a ordem de campo incorreta, não deverá haver nenhum impacto na qualidade da imagem, mas a eficiência da codificação será afetada.</span><span class="sxs-lookup"><span data-stu-id="b7ac7-154">If the codec uses the wrong field order, there should be no impact on image quality, but the encoding efficiency will be affected.</span></span> |
| <span data-ttu-id="b7ac7-155">\_primeiro campo do WM CT na \_ parte inferior \_ \_</span><span class="sxs-lookup"><span data-stu-id="b7ac7-155">WM\_CT\_BOTTOM\_FIELD\_FIRST</span></span> | <span data-ttu-id="b7ac7-156">Quando combinado com o sinalizador do WM \_ CT \_ entrelaçado, esse sinalizador indica que o campo inferior (o campo que começa com a segunda linha no exemplo) ocorre primeiro no tempo.</span><span class="sxs-lookup"><span data-stu-id="b7ac7-156">When combined with the WM\_CT\_INTERLACED flag, this flag indicates that the bottom field (the field starting with the second line in the sample) occurs first in time.</span></span>                                                                                                                                                                                          |
| <span data-ttu-id="b7ac7-157">primeiro campo do WM \_ CT \_ principal \_ \_</span><span class="sxs-lookup"><span data-stu-id="b7ac7-157">WM\_CT\_TOP\_FIELD\_FIRST</span></span>    | <span data-ttu-id="b7ac7-158">Quando combinado com o sinalizador do WM \_ CT \_ entrelaçado, esse sinalizador indica que o campo superior (o campo que começa com a primeira linha no exemplo) ocorre primeiro no tempo.</span><span class="sxs-lookup"><span data-stu-id="b7ac7-158">When combined with the WM\_CT\_INTERLACED flag, this flag indicates that the top field (the field starting with the first line in the sample) occurs first in time.</span></span>                                                                                                                                                                                              |
| <span data-ttu-id="b7ac7-159">\_ \_ \_ primeiro campo de repetição do WM CT \_</span><span class="sxs-lookup"><span data-stu-id="b7ac7-159">WM\_CT\_REPEAT\_FIRST\_FIELD</span></span> | <span data-ttu-id="b7ac7-160">Indica que o primeiro campo no exemplo deve ser repetido na reprodução.</span><span class="sxs-lookup"><span data-stu-id="b7ac7-160">Indicates that the first field in the sample should be repeated on playback.</span></span> <span data-ttu-id="b7ac7-161">Esse sinalizador é usado para vídeo criado a partir do filme pelo processo de telecineon. Se nenhum sinalizador de ordem de campo for definido em conjunto com esse sinalizador, presume-se que o campo superior ocorra primeiro no tempo.</span><span class="sxs-lookup"><span data-stu-id="b7ac7-161">This flag is used for video that has created from film by the telecine process.If no field-order flag is set in conjunction with this flag, the top field is assumed to occur first in time.</span></span><br/>                                                                             |



 

> [!Note]  
> <span data-ttu-id="b7ac7-162">Se o sinalizador do WM \_ CT \_ entrelaçado não estiver definido, o exemplo será considerado para conter um quadro de vídeo progressivo.</span><span class="sxs-lookup"><span data-stu-id="b7ac7-162">If the WM\_CT\_INTERLACED flag is not set, the sample is assumed to contain a progressive video frame.</span></span>

 

## <a name="decoding-interlaced-video"></a><span data-ttu-id="b7ac7-163">Decodificando vídeo entrelaçado</span><span class="sxs-lookup"><span data-stu-id="b7ac7-163">Decoding Interlaced Video</span></span>

<span data-ttu-id="b7ac7-164">Ao decodificar vídeo entrelaçado, você deve definir a configuração g \_ wszAllowInterlacedOutput como **true** usando o método [**IWMReaderAdvanced2:: SetOutputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setoutputsetting) .</span><span class="sxs-lookup"><span data-stu-id="b7ac7-164">When decoding interlaced video, you must set the g\_wszAllowInterlacedOutput setting to **TRUE** using the [**IWMReaderAdvanced2::SetOutputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setoutputsetting) method.</span></span> <span data-ttu-id="b7ac7-165">Caso contrário, o codec fornecerá quadros progressivos.</span><span class="sxs-lookup"><span data-stu-id="b7ac7-165">Otherwise the codec will deliver progressive frames.</span></span>

<span data-ttu-id="b7ac7-166">A extensão de unidade de dados de tipo de conteúdo é mantida nos exemplos de saída.</span><span class="sxs-lookup"><span data-stu-id="b7ac7-166">The content type data unit extension is maintained on the output samples.</span></span> <span data-ttu-id="b7ac7-167">Você deve passar a orientação do campo para o dispositivo de renderização para garantir a reprodução correta.</span><span class="sxs-lookup"><span data-stu-id="b7ac7-167">You should pass the field orientation to the rendering device to ensure proper playback.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b7ac7-168">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b7ac7-168">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b7ac7-169">**Tópicos avançados**</span><span class="sxs-lookup"><span data-stu-id="b7ac7-169">**Advanced Topics**</span></span>](advanced-topics.md)
</dt> </dl>

 

 





