---
title: Para desentrelaçar vídeo
description: Para desentrelaçar vídeo
ms.assetid: 60e6af09-fde1-4e4a-b54c-4923c0549b6b
keywords:
- SDK do Windows Media Format, vídeo desentrelaçado
- SDK do Windows Media Format, telecineon inverso
- SDK do Windows Media Format, telecineon
- ASF (Advanced Systems Format), vídeo desentrelaçado
- ASF (formato de sistemas avançados), vídeo desentrelaçado
- Formato de sistema avançado (ASF), inverso
- ASF (formato de sistemas avançados), telecineon inverso
- Formato de sistema avançado (ASF), telecineon
- ASF (formato de sistemas avançados), telecineon
- vídeo desentrelaçado
- inverso, sobre
- telecineon, sobre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 580b8425e5807fefdfa889fcd08deedb4143cf39
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104007126"
---
# <a name="to-deinterlace-video"></a><span data-ttu-id="06249-115">Para desentrelaçar vídeo</span><span class="sxs-lookup"><span data-stu-id="06249-115">To Deinterlace Video</span></span>

<span data-ttu-id="06249-116">Algumas fontes de vídeo, como cartões de captura de vídeo, fornecem dados de vídeo para exibição entrelaçada.</span><span class="sxs-lookup"><span data-stu-id="06249-116">Some sources of video, such as video capture cards, deliver video data for interlaced display.</span></span> <span data-ttu-id="06249-117">Cada quadro de vídeo entrelaçado é composto de dois campos.</span><span class="sxs-lookup"><span data-stu-id="06249-117">Each frame of interlaced video is made up of two fields.</span></span> <span data-ttu-id="06249-118">O campo superior contém a primeira linha de vídeo e todas as outras linhas posteriormente.</span><span class="sxs-lookup"><span data-stu-id="06249-118">The top field contains the first line of video and every other line thereafter.</span></span> <span data-ttu-id="06249-119">O campo inferior contém a segunda linha de vídeo e todas as outras linhas posteriormente.</span><span class="sxs-lookup"><span data-stu-id="06249-119">The bottom field contains the second line of video and every other line thereafter.</span></span> <span data-ttu-id="06249-120">Portanto, um campo contém todas as linhas numeradas pares e a outra contém todas as linhas ímpares.</span><span class="sxs-lookup"><span data-stu-id="06249-120">So one field contains all of the even numbered lines and the other contains all of the odd numbered lines.</span></span> <span data-ttu-id="06249-121">Os campos que compõem um quadro representam tempos de apresentação um pouco diferentes para que, quando intercalados, não formam uma imagem estática.</span><span class="sxs-lookup"><span data-stu-id="06249-121">The fields that make up a frame represent slightly different presentation times so that, when interleaved, they do not form a static image.</span></span>

<span data-ttu-id="06249-122">Quando você deseja exibir vídeo em um monitor de computador, cada quadro do vídeo deve ser exibido como uma imagem (esse método de exibir o vídeo de um quadro inteiro por vez é chamado de vídeo *progressivo* ). Se você exibir vídeo entrelaçado progressivamente, os quadros podem não parecer corretos, devido à diferença de tempo entre os dois campos.</span><span class="sxs-lookup"><span data-stu-id="06249-122">When you want to display video on a computer monitor, each frame of the video should be displayed as one image (this method of displaying video one whole frame at a time is called *progressive* video.) If you display interlaced video progressively, the frames may not look right, because of the time difference between the two fields.</span></span> <span data-ttu-id="06249-123">O codec de vídeo do Windows Media e o codec de perfil avançado do vídeo do Windows Media oferecem suporte a um recurso de pré-processamento que converte conteúdo entrelaçado em quadros progressivos.</span><span class="sxs-lookup"><span data-stu-id="06249-123">The Windows Media Video codec and the Windows Media Video Advanced Profile codec both support a preprocessing feature that converts interlaced content into progressive frames.</span></span>

<span data-ttu-id="06249-124">Para que o codec desentrelaçar o vídeo de entrada, chame o método [**IWMWriterAdvanced2:: SetInputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-setinputsetting) .</span><span class="sxs-lookup"><span data-stu-id="06249-124">To have the codec deinterlace input video, call the [**IWMWriterAdvanced2::SetInputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-setinputsetting) method.</span></span> <span data-ttu-id="06249-125">A configuração a ser usada é g \_ wszDeinterlaceMode.</span><span class="sxs-lookup"><span data-stu-id="06249-125">The setting to use is g\_wszDeinterlaceMode.</span></span> <span data-ttu-id="06249-126">Defina o modo de desentrelaçamento como um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="06249-126">Set the deinterlacing mode to one of the following values.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="06249-127">Valor</span><span class="sxs-lookup"><span data-stu-id="06249-127">Value</span></span></th>
<th><span data-ttu-id="06249-128">Descrição</span><span class="sxs-lookup"><span data-stu-id="06249-128">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="06249-129">WM_DM_NOTINTERLACED</span><span class="sxs-lookup"><span data-stu-id="06249-129">WM_DM_NOTINTERLACED</span></span></td>
<td><span data-ttu-id="06249-130">A entrada é progressiva.</span><span class="sxs-lookup"><span data-stu-id="06249-130">Input is progressive.</span></span> <span data-ttu-id="06249-131">Use essa configuração para parar de desentrelaçar quando você tiver definido anteriormente o modo de desentrelaçamento para outro valor.</span><span class="sxs-lookup"><span data-stu-id="06249-131">Use this setting to stop deinterlacing when you have previously set the deinterlacing mode to another value.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="06249-132">WM_DM_DEINTERLACE_NORMAL</span><span class="sxs-lookup"><span data-stu-id="06249-132">WM_DM_DEINTERLACE_NORMAL</span></span></td>
<td><span data-ttu-id="06249-133">Selecione este modo para misturar os campos pares e ímpares de um quadro entrelaçado (usando um mecanismo de compensação de movimento). Benefícios</span><span class="sxs-lookup"><span data-stu-id="06249-133">Select this mode to blend the even and odd fields of an interlaced frame (using a motion compensation mechanism).Benefits:</span></span><br/>
<ul>
<li><span data-ttu-id="06249-134">Os artefatos entrelaçados da exibição progressiva são reduzidos significativamente.</span><span class="sxs-lookup"><span data-stu-id="06249-134">The interlace artifacts of the progressive display are significantly reduced.</span></span></li>
<li><span data-ttu-id="06249-135">O codec de vídeo do Windows Media produz vídeo compactado de alta qualidade.</span><span class="sxs-lookup"><span data-stu-id="06249-135">The Windows Media Video codec produces higher quality compressed video.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="06249-136">WM_DM_DEINTERLACE_HALFSIZE</span><span class="sxs-lookup"><span data-stu-id="06249-136">WM_DM_DEINTERLACE_HALFSIZE</span></span></td>
<td><span data-ttu-id="06249-137">Selecione esse modo quando a resolução de saída for metade ou menor da resolução de entrada.</span><span class="sxs-lookup"><span data-stu-id="06249-137">Select this mode when the output resolution is half, or less, of the input resolution.</span></span> <span data-ttu-id="06249-138">Por exemplo, use este modo quando a resolução de vídeo de entrada for 640 x 480 pixels e a resolução de vídeo de saída for de 320 x 240 pixels. Benefícios</span><span class="sxs-lookup"><span data-stu-id="06249-138">For example, use this mode when the input video resolution is 640 x 480 pixels and the output video resolution is 320 x 240 pixels.Benefits:</span></span><br/>
<ul>
<li><span data-ttu-id="06249-139">Os artefatos entrelaçados da exibição progressiva são reduzidos significativamente.</span><span class="sxs-lookup"><span data-stu-id="06249-139">The interlace artifacts of the progressive display are significantly reduced.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="06249-140">WM_DM_DEINTERLACE_HALFSIZEDOUBLERATE</span><span class="sxs-lookup"><span data-stu-id="06249-140">WM_DM_DEINTERLACE_HALFSIZEDOUBLERATE</span></span></td>
<td><span data-ttu-id="06249-141">Selecione esse modo quando a resolução de saída for metade, ou menos, da resolução de entrada e a <a href="wmformat-glossary.md"><em>taxa de quadros</em></a> de saída for duas vezes alta.</span><span class="sxs-lookup"><span data-stu-id="06249-141">Select this mode when the output resolution is half, or less, of the input resolution and the output <a href="wmformat-glossary.md"><em>frame rate</em></a> is twice as high.</span></span> <span data-ttu-id="06249-142">Por exemplo, use este modo quando a resolução de vídeo de entrada for 640 x 480 pixels a 30 quadros entrelaçados/s e a resolução de vídeo de saída for 320 x 240 pixels em 60 quadros/s. Benefícios</span><span class="sxs-lookup"><span data-stu-id="06249-142">For example, use this mode when the input video resolution is 640 x 480 pixels at 30 interlaced frames/sec and the output video resolution is 320 x 240 pixels at 60 frames/sec.Benefits:</span></span><br/>
<ul>
<li><span data-ttu-id="06249-143">Isso produz quadros progressivos de alta qualidade, pois cada campo é convertido em um quadro e, portanto, não é necessário misturar nenhuma informação.</span><span class="sxs-lookup"><span data-stu-id="06249-143">This produces progressive frames of high quality, because each field is converted to a frame and so there is no need to blend any information.</span></span></li>
<li><span data-ttu-id="06249-144">O movimento completo dos campos entrelaçados é capturado.</span><span class="sxs-lookup"><span data-stu-id="06249-144">The full motion of the interlaced fields is captured.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="06249-145">WM_DM_DEINTERLACE_INVERSETELECINE</span><span class="sxs-lookup"><span data-stu-id="06249-145">WM_DM_DEINTERLACE_INVERSETELECINE</span></span></td>
<td><span data-ttu-id="06249-146">Selecione este modo para converter o vídeo telecineon de 30 quadros/s nos 24 quadros/s do filme original. Benefícios</span><span class="sxs-lookup"><span data-stu-id="06249-146">Select this mode to convert telecined 30 frames/sec video into the 24 frames/sec of the original film.Benefits:</span></span><br/>
<ul>
<li><span data-ttu-id="06249-147">A qualidade da compactação melhora significativamente porque apenas 24 quadros/s em vez de 30 quadros/s precisam ser codificados.</span><span class="sxs-lookup"><span data-stu-id="06249-147">The compression quality improves significantly because only 24 frames/sec instead of 30 frames/sec need to be encoded.</span></span></li>
<li><span data-ttu-id="06249-148">Como o resultado é progressivo, a mesma compactação e os benefícios de exibição de desentrelaçamento são percebidos.</span><span class="sxs-lookup"><span data-stu-id="06249-148">Because the result is progressive, the same compression and display benefits of deinterlacing are realized.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="06249-149">WM_DM_DEINTERLACE_VERTICALHALFSIZEDOUBLERATE</span><span class="sxs-lookup"><span data-stu-id="06249-149">WM_DM_DEINTERLACE_VERTICALHALFSIZEDOUBLERATE</span></span></td>
<td><span data-ttu-id="06249-150">Selecione esse modo quando a resolução vertical de saída for metade, ou menos, da resolução vertical de entrada e a <a href="wmformat-glossary.md"><em>taxa de quadros</em></a> de saída for duas vezes alta.</span><span class="sxs-lookup"><span data-stu-id="06249-150">Select this mode when the vertical output resolution is half, or less, of the input vertical resolution and the output <a href="wmformat-glossary.md"><em>frame rate</em></a> is twice as high.</span></span> <span data-ttu-id="06249-151">Por exemplo, a resolução de vídeo vertical de entrada é 640 x 480 pixels a 30 quadros entrelaçados/s e a resolução de vídeo vertical de saída é 320 x 240 pixels em 60 quadros/s. Benefícios</span><span class="sxs-lookup"><span data-stu-id="06249-151">For example, the input vertical video resolution is 640 x 480 pixels at 30 interlaced frames/sec and the output vertical video resolution is 320 x 240 pixels at 60 frames/sec.Benefits:</span></span><br/>
<ul>
<li><span data-ttu-id="06249-152">Isso produz quadros progressivos de alta qualidade, pois cada campo é convertido em um quadro e, portanto, não é necessário misturar nenhuma informação.</span><span class="sxs-lookup"><span data-stu-id="06249-152">This produces progressive frames of high quality, because each field is converted to a frame and so there is no need to blend any information.</span></span></li>
<li><span data-ttu-id="06249-153">O movimento completo dos campos entrelaçados é capturado.</span><span class="sxs-lookup"><span data-stu-id="06249-153">The full motion of the interlaced fields is captured.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="06249-154">Para conteúdo misto, defina o modo de desentrelaçamento conforme necessário antes de passar amostras de um novo tipo.</span><span class="sxs-lookup"><span data-stu-id="06249-154">For mixed content, set the deinterlacing mode as needed before passing samples of a new type.</span></span> <span data-ttu-id="06249-155">Por exemplo, para iniciar a codificação com a entrada progressiva, você não precisa definir nenhum modo de desentrelaçamento.</span><span class="sxs-lookup"><span data-stu-id="06249-155">For example, to start encoding with progressive input, you don't need to set any deinterlacing mode.</span></span> <span data-ttu-id="06249-156">Se alguns exemplos exigirem desentrelaçamento normal, você deverá definir o modo de desentrelaçamento para o WM \_ DM \_ desentrelaçar \_ normal.</span><span class="sxs-lookup"><span data-stu-id="06249-156">If some samples then require normal deinterlacing, you must set the deinterlacing mode to WM\_DM\_DEINTERLACE\_NORMAL.</span></span> <span data-ttu-id="06249-157">Para processar amostras progressivas adicionais, você deve definir o modo de desentrelaçamento para o WM \_ DM não \_ entrelaçado.</span><span class="sxs-lookup"><span data-stu-id="06249-157">To then process additional progressive samples you must set the deinterlacing mode to WM\_DM\_NOTINTERLACED.</span></span>

## <a name="inverse-telecine-settings"></a><span data-ttu-id="06249-158">Configurações de inversos</span><span class="sxs-lookup"><span data-stu-id="06249-158">Inverse Telecine Settings</span></span>

<span data-ttu-id="06249-159">Para obter uma descrição do telecineon inverso, consulte [para usar o telecineon inverso](to-use-inverse-telecine.md).</span><span class="sxs-lookup"><span data-stu-id="06249-159">For a description of inverse telecine, see [To Use Inverse Telecine](to-use-inverse-telecine.md).</span></span>

<span data-ttu-id="06249-160">Se você definir o modo de desentrelaçamento para o WM \_ DM \_ desentrelaçar \_ INVERSETELECINE, poderá especificar o padrão de telecineon do primeiro quadro de entrada chamando o [**IWMWriterAdvanced2:: SetInputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-setinputsetting).</span><span class="sxs-lookup"><span data-stu-id="06249-160">If you set the deinterlacing mode to WM\_DM\_DEINTERLACE\_INVERSETELECINE, you can specify the telecine pattern of the first input frame by calling the [**IWMWriterAdvanced2::SetInputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-setinputsetting).</span></span> <span data-ttu-id="06249-161">A configuração a ser usada é g \_ wszInitialPatternForInverseTelecine.</span><span class="sxs-lookup"><span data-stu-id="06249-161">The setting to use is g\_wszInitialPatternForInverseTelecine.</span></span> <span data-ttu-id="06249-162">Defina o padrão inicial como um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="06249-162">Set the initial pattern to one of the following values.</span></span>



| <span data-ttu-id="06249-163">Valor</span><span class="sxs-lookup"><span data-stu-id="06249-163">Value</span></span>                                              | <span data-ttu-id="06249-164">Descrição</span><span class="sxs-lookup"><span data-stu-id="06249-164">Description</span></span>                                                                                                                                                                                                                                                                                                   |
|----------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="06249-165">o WM \_ DM \_ desabilita o \_ \_ \_ modo coerente</span><span class="sxs-lookup"><span data-stu-id="06249-165">WM\_DM\_IT\_DISABLE\_COHERENT\_MODE</span></span>                | <span data-ttu-id="06249-166">Especifica que a mídia de entrada passou pelo processo de telecineon, mas que os quadros não estão mais em um padrão previsível.</span><span class="sxs-lookup"><span data-stu-id="06249-166">Specifies that the input media has gone through the telecine process but that the frames are no longer in a predictable pattern.</span></span> <span data-ttu-id="06249-167">Isso geralmente indica que a mídia foi editada após o processamento de telecineon.</span><span class="sxs-lookup"><span data-stu-id="06249-167">This usually indicates that the media was edited after the telecine processing.</span></span> <span data-ttu-id="06249-168">Quando você usa essa configuração, o codec tenta reconstruir os quadros originais por conta própria.</span><span class="sxs-lookup"><span data-stu-id="06249-168">When you use this setting, the codec attempts to reconstruct the original frames on its own.</span></span> |
| <span data-ttu-id="06249-169">WM \_ DM \_ ele \_ primeiro \_ quadro \_ em \_ clip \_ é \_ AA \_ Top</span><span class="sxs-lookup"><span data-stu-id="06249-169">WM\_DM\_IT\_FIRST\_FRAME\_IN\_CLIP\_IS\_AA\_TOP</span></span>    | <span data-ttu-id="06249-170">Especifica que o campo superior do quadro AA é o primeiro exemplo.</span><span class="sxs-lookup"><span data-stu-id="06249-170">Specifies that the top field of the AA frame is the first sample.</span></span>                                                                                                                                                                                                                                             |
| <span data-ttu-id="06249-171">WM \_ DM \_ ele \_ primeiro \_ quadro \_ no \_ clipe \_ é \_ BB na \_ parte superior</span><span class="sxs-lookup"><span data-stu-id="06249-171">WM\_DM\_IT\_FIRST\_FRAME\_IN\_CLIP\_IS\_BB\_TOP</span></span>    | <span data-ttu-id="06249-172">Especifica que o campo superior do quadro BB é o primeiro exemplo.</span><span class="sxs-lookup"><span data-stu-id="06249-172">Specifies that the top field of the BB frame is the first sample.</span></span>                                                                                                                                                                                                                                             |
| <span data-ttu-id="06249-173">WM \_ DM \_ ele \_ primeiro \_ quadro \_ no \_ clipe \_ é \_ BC \_ superior</span><span class="sxs-lookup"><span data-stu-id="06249-173">WM\_DM\_IT\_FIRST\_FRAME\_IN\_CLIP\_IS\_BC\_TOP</span></span>    | <span data-ttu-id="06249-174">Especifica que o campo superior do quadro BC é o primeiro exemplo.</span><span class="sxs-lookup"><span data-stu-id="06249-174">Specifies that the top field of the BC frame is the first sample.</span></span>                                                                                                                                                                                                                                             |
| <span data-ttu-id="06249-175">WM \_ DM \_ ele \_ primeiro \_ quadro \_ no \_ clipe \_ é \_ CD \_ superior</span><span class="sxs-lookup"><span data-stu-id="06249-175">WM\_DM\_IT\_FIRST\_FRAME\_IN\_CLIP\_IS\_CD\_TOP</span></span>    | <span data-ttu-id="06249-176">Especifica que o campo superior do quadro do CD é o primeiro exemplo.</span><span class="sxs-lookup"><span data-stu-id="06249-176">Specifies that the top field of the CD frame is the first sample.</span></span>                                                                                                                                                                                                                                             |
| <span data-ttu-id="06249-177">WM \_ DM \_ ele \_ primeiro \_ quadro \_ no \_ clipe \_ é \_ DD \_ Top</span><span class="sxs-lookup"><span data-stu-id="06249-177">WM\_DM\_IT\_FIRST\_FRAME\_IN\_CLIP\_IS\_DD\_TOP</span></span>    | <span data-ttu-id="06249-178">Especifica que o campo superior do quadro DD é o primeiro exemplo.</span><span class="sxs-lookup"><span data-stu-id="06249-178">Specifies that the top field of the DD frame is the first sample.</span></span>                                                                                                                                                                                                                                             |
| <span data-ttu-id="06249-179">WM \_ DM \_ ele \_ primeiro \_ quadro \_ em \_ clip \_ é \_ AA \_ Bottom</span><span class="sxs-lookup"><span data-stu-id="06249-179">WM\_DM\_IT\_FIRST\_FRAME\_IN\_CLIP\_IS\_AA\_BOTTOM</span></span> | <span data-ttu-id="06249-180">Especifica que o campo inferior do quadro AA é o primeiro exemplo.</span><span class="sxs-lookup"><span data-stu-id="06249-180">Specifies that the bottom field of the AA frame is the first sample.</span></span>                                                                                                                                                                                                                                          |
| <span data-ttu-id="06249-181">WM \_ DM \_ ele \_ primeiro \_ quadro \_ no \_ clipe \_ é \_ BB \_ inferior</span><span class="sxs-lookup"><span data-stu-id="06249-181">WM\_DM\_IT\_FIRST\_FRAME\_IN\_CLIP\_IS\_BB\_BOTTOM</span></span> | <span data-ttu-id="06249-182">Especifica que o campo inferior do quadro BB é o primeiro exemplo.</span><span class="sxs-lookup"><span data-stu-id="06249-182">Specifies that the bottom field of the BB frame is the first sample.</span></span>                                                                                                                                                                                                                                          |
| <span data-ttu-id="06249-183">WM \_ DM \_ ele \_ primeiro \_ quadro \_ no \_ clipe \_ é \_ BC- \_ Bottom</span><span class="sxs-lookup"><span data-stu-id="06249-183">WM\_DM\_IT\_FIRST\_FRAME\_IN\_CLIP\_IS\_BC\_BOTTOM</span></span> | <span data-ttu-id="06249-184">Especifica que o campo inferior do quadro BC é o primeiro exemplo.</span><span class="sxs-lookup"><span data-stu-id="06249-184">Specifies that the bottom field of the BC frame is the first sample.</span></span>                                                                                                                                                                                                                                          |
| <span data-ttu-id="06249-185">WM \_ DM \_ o \_ primeiro \_ quadro \_ no \_ clipe \_ é o \_ CD \_ inferior</span><span class="sxs-lookup"><span data-stu-id="06249-185">WM\_DM\_IT\_FIRST\_FRAME\_IN\_CLIP\_IS\_CD\_BOTTOM</span></span> | <span data-ttu-id="06249-186">Especifica que o campo inferior do quadro do CD é o primeiro exemplo.</span><span class="sxs-lookup"><span data-stu-id="06249-186">Specifies that the bottom field of the CD frame is the first sample.</span></span>                                                                                                                                                                                                                                          |
| <span data-ttu-id="06249-187">WM \_ DM \_ ele \_ primeiro \_ quadro \_ no \_ clipe \_ é \_ DD \_ Bottom</span><span class="sxs-lookup"><span data-stu-id="06249-187">WM\_DM\_IT\_FIRST\_FRAME\_IN\_CLIP\_IS\_DD\_BOTTOM</span></span> | <span data-ttu-id="06249-188">Especifica que o campo inferior do quadro DD é o primeiro exemplo.</span><span class="sxs-lookup"><span data-stu-id="06249-188">Specifies that the bottom field of the DD frame is the first sample.</span></span>                                                                                                                                                                                                                                          |



 

## <a name="related-topics"></a><span data-ttu-id="06249-189">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="06249-189">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="06249-190">**Tópicos avançados**</span><span class="sxs-lookup"><span data-stu-id="06249-190">**Advanced Topics**</span></span>](advanced-topics.md)
</dt> </dl>

 

 





