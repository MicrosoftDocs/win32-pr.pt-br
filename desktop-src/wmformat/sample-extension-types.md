---
title: Tipos de extensão de exemplo
description: Tipos de extensão de exemplo
ms.assetid: 8de2e003-cb21-4be9-bcde-7f5909b6260a
keywords:
- SDK do Windows Media Format, extensões de exemplo
- ASF (Advanced Systems Format), extensões de exemplo
- ASF (formato de sistemas avançados), extensões de exemplo
- SDK do Windows Media Format, extensões de unidade de dados
- ASF (Advanced Systems Format), extensões de unidade de dados
- ASF (formato de sistemas avançados), extensões de unidade de dados
- SDK do Windows Media Format, propriedades do buffer
- Formato de sistema avançado (ASF), propriedades de buffer
- ASF (formato de sistemas avançados), propriedades de buffer
- extensões de exemplo, tipos
- extensões de unidade de dados, tipos
- Propriedades do buffer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 972e3da1ecaad277158bb270cc358436f53db9e2
ms.sourcegitcommit: c2a1c4314550ea9bd202d28adfcc7bfe6180932f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2020
ms.locfileid: "105808235"
---
# <a name="sample-extension-types"></a><span data-ttu-id="ffdb5-115">Tipos de extensão de exemplo</span><span class="sxs-lookup"><span data-stu-id="ffdb5-115">Sample Extension Types</span></span>

<span data-ttu-id="ffdb5-116">As extensões de exemplo, também chamadas de extensões de unidade de dados (dívidas) ou propriedades de buffer, são itens de dados anexados aos exemplos de mídia na seção de dados do arquivo ASF.</span><span class="sxs-lookup"><span data-stu-id="ffdb5-116">Sample extensions, also called data unit extensions (DUEs) or buffer properties, are items of data that are attached to the media samples in the data section of the ASF file.</span></span> <span data-ttu-id="ffdb5-117">Vários tipos de extensões de exemplo são definidos no SDK do Windows Media Format.</span><span class="sxs-lookup"><span data-stu-id="ffdb5-117">Several types of sample extensions are defined in the Windows Media Format SDK.</span></span> <span data-ttu-id="ffdb5-118">Você também pode criar seus próprios tipos de extensão.</span><span class="sxs-lookup"><span data-stu-id="ffdb5-118">You can also create your own extension types.</span></span>

<span data-ttu-id="ffdb5-119">Para usar extensões de exemplo, você deve identificar o tipo de extensão nos dados de configuração de fluxo do perfil.</span><span class="sxs-lookup"><span data-stu-id="ffdb5-119">To use sample extensions, you must identify the extension type in the stream configuration data of the profile.</span></span> <span data-ttu-id="ffdb5-120">Chame o método [**IWMStreamConfig2:: AddDataUnitExtension**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-adddataunitextension) para configurar um fluxo para aceitar amostras com dados estendidos.</span><span class="sxs-lookup"><span data-stu-id="ffdb5-120">Call the [**IWMStreamConfig2::AddDataUnitExtension**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-adddataunitextension) method to configure a stream to accept samples with extended data.</span></span>

<span data-ttu-id="ffdb5-121">Extensões de exemplo individuais devem ser adicionadas aos exemplos de entrada chamando o método [**INSSBuffer3:: SetProperty**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer3-setproperty) .</span><span class="sxs-lookup"><span data-stu-id="ffdb5-121">Individual sample extensions must be added to the input samples by calling the [**INSSBuffer3::SetProperty**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer3-setproperty) method.</span></span> <span data-ttu-id="ffdb5-122">Ao ler exemplos, você pode chamar o método [**INSSBuffer3:: GetProperty**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer3-getproperty) para recuperar os dados de extensão.</span><span class="sxs-lookup"><span data-stu-id="ffdb5-122">When reading samples, you can call the [**INSSBuffer3::GetProperty**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer3-getproperty) method to retrieve the extension data.</span></span> <span data-ttu-id="ffdb5-123">Você também pode usar os métodos da interface [**INSSBuffer4**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer4) para enumerar as extensões de unidade de dados anexadas a um exemplo.</span><span class="sxs-lookup"><span data-stu-id="ffdb5-123">You can also use the methods of the [**INSSBuffer4**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer4) interface to enumerate the data unit extensions attached to a sample.</span></span>

<span data-ttu-id="ffdb5-124">A tabela a seguir lista os identificadores de extensão de unidade de dados predefinidos e descreve os dados anexados a exemplos para cada um.</span><span class="sxs-lookup"><span data-stu-id="ffdb5-124">The following table lists the predefined data unit extension identifiers, and describes the data that is attached to samples for each.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ffdb5-125">GUID de extensão de exemplo</span><span class="sxs-lookup"><span data-stu-id="ffdb5-125">Sample extension GUID</span></span></th>
<th><span data-ttu-id="ffdb5-126">Descrição</span><span class="sxs-lookup"><span data-stu-id="ffdb5-126">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ffdb5-127">WM_SampleExtensionGUID_OutputCleanPoint</span><span class="sxs-lookup"><span data-stu-id="ffdb5-127">WM_SampleExtensionGUID_OutputCleanPoint</span></span></td>
<td><span data-ttu-id="ffdb5-128">Os dados indicam se o exemplo é um <a href="wmformat-glossary.md"><em>cleanpoint</em></a>.</span><span class="sxs-lookup"><span data-stu-id="ffdb5-128">The data indicates whether the sample is a <a href="wmformat-glossary.md"><em>cleanpoint</em></a>.</span></span> <span data-ttu-id="ffdb5-129">Um valor de zero indica que o exemplo não é um cleanpoint.</span><span class="sxs-lookup"><span data-stu-id="ffdb5-129">A value of zero indicates that the sample is not a cleanpoint.</span></span> <span data-ttu-id="ffdb5-130">Um valor diferente de zero indica que se trata de um cleanpoint.</span><span class="sxs-lookup"><span data-stu-id="ffdb5-130">A non-zero value indicates that it is a cleanpoint.</span></span> <span data-ttu-id="ffdb5-131">Esse tipo de extensão de unidade de dados (devido) de exemplo é usado para controlar o cleanpoints ao gravar fluxos de mídia compactados que foram codificados com codecs de terceiros.</span><span class="sxs-lookup"><span data-stu-id="ffdb5-131">This sample data unit extension (DUE) type is used to keep track of cleanpoints when writing precompressed media streams that were encoded with third-party codecs.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ffdb5-132">WM_SampleExtensionGUID_Timecode</span><span class="sxs-lookup"><span data-stu-id="ffdb5-132">WM_SampleExtensionGUID_Timecode</span></span></td>
<td><span data-ttu-id="ffdb5-133">Os dados são uma estrutura de <a href="/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmt_timecode_extension_data"><strong>WMT_TIMECODE_EXTENSION_DATA</strong></a> que contém dados de código de tempo SMPTE associados ao exemplo. O tamanho para isso devido é sempre WM_SampleExtension_Timecode_Size, que é de 14 bytes.</span><span class="sxs-lookup"><span data-stu-id="ffdb5-133">The data is a <a href="/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmt_timecode_extension_data"><strong>WMT_TIMECODE_EXTENSION_DATA</strong></a> structure containing SMPTE time code data associated with the sample.The size for this DUE is always WM_SampleExtension_Timecode_Size, which is 14 bytes.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ffdb5-134">WM_SampleExtensionGUID_FileName</span><span class="sxs-lookup"><span data-stu-id="ffdb5-134">WM_SampleExtensionGUID_FileName</span></span></td>
<td><span data-ttu-id="ffdb5-135">Esse tipo de extensão de exemplo é usado para fluxos de arquivo.</span><span class="sxs-lookup"><span data-stu-id="ffdb5-135">This type of sample extension is used for file streams.</span></span> <span data-ttu-id="ffdb5-136">Os dados em um exemplo de fluxo de arquivo são uma parte de um arquivo de dados.</span><span class="sxs-lookup"><span data-stu-id="ffdb5-136">The data in a file stream sample is a piece of a data file.</span></span> <span data-ttu-id="ffdb5-137">Os dados na extensão de exemplo especificam o nome do arquivo do qual o conteúdo no exemplo foi tirado. O nome do arquivo é uma cadeia de caracteres largos que contém o nome do arquivo no formato name. Extension sem nenhuma informação de caminho.</span><span class="sxs-lookup"><span data-stu-id="ffdb5-137">The data in the sample extension specifies the name of the file from which the content in the sample was taken.The file name is a wide-character string containing the file name in name.extension format without any path information.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ffdb5-138">WM_SampleExtensionGUID_ContentType</span><span class="sxs-lookup"><span data-stu-id="ffdb5-138">WM_SampleExtensionGUID_ContentType</span></span></td>
<td><span data-ttu-id="ffdb5-139">Os dados identificam o tipo de conteúdo que o exemplo contém.</span><span class="sxs-lookup"><span data-stu-id="ffdb5-139">The data identifies the type of content that the sample contains.</span></span> <span data-ttu-id="ffdb5-140">Esse tipo de extensão de exemplo é usado com fluxos de vídeo entrelaçados. Todo o conteúdo entrelaçado usa o sinalizador de WM_CT_INTERLACED combinado por um OR-bit <strong>ou</strong> com WM_CT_BOTTOM_FIELD_FIRST, WM_CT_TOP_FIELD_FIRST ou WM_CT_REPEAT_FIRST_FIELD.</span><span class="sxs-lookup"><span data-stu-id="ffdb5-140">This type of sample extension is used with interlaced video streams.All interlaced content uses the WM_CT_INTERLACED flag combined by a bitwise <strong>OR</strong> with either WM_CT_BOTTOM_FIELD_FIRST, WM_CT_TOP_FIELD_FIRST, or WM_CT_REPEAT_FIRST_FIELD.</span></span><br/> <span data-ttu-id="ffdb5-141">A ordem de campo não é usada no processo de codificação, mas é mantida com os exemplos compactados para que ele possa ser passado para o hardware de renderização.</span><span class="sxs-lookup"><span data-stu-id="ffdb5-141">The field order is not used in the encoding process, but is maintained with the compressed samples so that it can be passed to the rendering hardware.</span></span> <span data-ttu-id="ffdb5-142">A reprodução de conteúdo entrelaçado com a ordem de campo incorreta apresenta artefatos como a tremulação de movimento no vídeo.</span><span class="sxs-lookup"><span data-stu-id="ffdb5-142">Playing interlaced content with the incorrect field order introduces artifacts such as motion jitter in the video.</span></span><br/> <span data-ttu-id="ffdb5-143">O tamanho para isso devido é sempre WM_SampleExtension_ContentType_Size.</span><span class="sxs-lookup"><span data-stu-id="ffdb5-143">The size for this DUE is always WM_SampleExtension_ContentType_Size.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ffdb5-144">WM_SampleExtensionGUID_PixelAspectRatio</span><span class="sxs-lookup"><span data-stu-id="ffdb5-144">WM_SampleExtensionGUID_PixelAspectRatio</span></span></td>
<td><span data-ttu-id="ffdb5-145">Os dados indicam a taxa de proporção de pixel do conteúdo no exemplo.</span><span class="sxs-lookup"><span data-stu-id="ffdb5-145">The data indicates the pixel aspect ratio of the content in the sample.</span></span> <span data-ttu-id="ffdb5-146">Isso se aplica somente a vídeo. Esse tipo de extensão é usado para identificar a taxa de proporção de pixels não quadrados.</span><span class="sxs-lookup"><span data-stu-id="ffdb5-146">This applies only to video.This extension type is used to identify the aspect ratio of non-square pixels.</span></span> <span data-ttu-id="ffdb5-147">Para obter mais informações, consulte <a href="to-read-and-write-video-streams-with-non-square-pixels.md">para ler e gravar fluxos de vídeo com pixels não quadrados</a>.</span><span class="sxs-lookup"><span data-stu-id="ffdb5-147">For more information, see <a href="to-read-and-write-video-streams-with-non-square-pixels.md">To Read and Write Video Streams with Non-Square Pixels</a>.</span></span><br/> <span data-ttu-id="ffdb5-148">Os valores de taxa de proporção são armazenados como uma palavra cujo byte baixo é o aspecto X e cujo byte alto é o aspecto Y.</span><span class="sxs-lookup"><span data-stu-id="ffdb5-148">Aspect ratio values are stored as a word whose low byte is the X aspect and whose high byte is the Y aspect.</span></span> <span data-ttu-id="ffdb5-149">Por exemplo, 16:9 é armazenado como 0x0910.</span><span class="sxs-lookup"><span data-stu-id="ffdb5-149">For example, 16:9 is stored as 0x0910.</span></span><br/> <span data-ttu-id="ffdb5-150">O tamanho para isso devido é sempre WM_SampleExtension_PixelAspectRatio_Size, que é de 2 bytes.</span><span class="sxs-lookup"><span data-stu-id="ffdb5-150">The size for this DUE is always WM_SampleExtension_PixelAspectRatio_Size, which is 2 bytes.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ffdb5-151">WM_SampleExtensionGUID_SampleDuration</span><span class="sxs-lookup"><span data-stu-id="ffdb5-151">WM_SampleExtensionGUID_SampleDuration</span></span></td>
<td><span data-ttu-id="ffdb5-152">Os dados indicam a duração, em milissegundos, do exemplo contido no objeto de buffer.</span><span class="sxs-lookup"><span data-stu-id="ffdb5-152">The data indicates the duration, in milliseconds, of the sample contained in the buffer object.</span></span> <span data-ttu-id="ffdb5-153">Na reprodução, se isso devido for definido, o objeto de leitor o usará para substituir o valor de duração de exemplo existente. Isso devido é definido automaticamente pelos componentes de tempo de execução do SDK em fluxos de vídeo com taxas de bits de 100 kbps ou mais, em que a sobrecarga das informações de conclusão não é significativa.</span><span class="sxs-lookup"><span data-stu-id="ffdb5-153">On playback, if this DUE is set the reader object will use it to overwrite the existing sample duration value.This DUE is set automatically by the SDK run-time components on video streams with bit rates of 100 kbps or greater, where the overhead of the DUE information is not significant.</span></span> <span data-ttu-id="ffdb5-154">Ele não está definido para fluxos com taxas de bits em 100 kbps.</span><span class="sxs-lookup"><span data-stu-id="ffdb5-154">It is not set for streams with bit rates under 100 kbps.</span></span> <span data-ttu-id="ffdb5-155">Os aplicativos não devem definir isso de forma manual porque o gravador (em fluxos de alta taxa de bits) substituirá o valor por seus próprios dados.</span><span class="sxs-lookup"><span data-stu-id="ffdb5-155">Applications should not set this DUE manually because the writer (on high-bit-rate streams) will overwrite the value with its own data.</span></span><br/> <span data-ttu-id="ffdb5-156">O tamanho para isso devido é sempre WM_SampleExtension_SampleDuration_Size, que é de 2 bytes.</span><span class="sxs-lookup"><span data-stu-id="ffdb5-156">The size for this DUE is always WM_SampleExtension_SampleDuration_Size, which is 2 bytes.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ffdb5-157">WM_SampleExtensionGUID_ChromaLocation</span><span class="sxs-lookup"><span data-stu-id="ffdb5-157">WM_SampleExtensionGUID_ChromaLocation</span></span></td>
<td><span data-ttu-id="ffdb5-158">Os dados indicam o tipo de subamostragem croma usado no formato de vídeo I420. O valor dessa extensão é definido como um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="ffdb5-158">The data indicates the type of chroma subsampling used in the I420 video format.The value of this extension is set to one of the follow values:</span></span><br/>
<ul>
<li><span data-ttu-id="ffdb5-159">WM_CL_INTERLACED420</span><span class="sxs-lookup"><span data-stu-id="ffdb5-159">WM_CL_INTERLACED420</span></span></li>
<li><span data-ttu-id="ffdb5-160">WM_CL_PROGRESSIVE420</span><span class="sxs-lookup"><span data-stu-id="ffdb5-160">WM_CL_PROGRESSIVE420</span></span></li>
</ul>
<span data-ttu-id="ffdb5-161">Esta extensão de unidade de dados não está configurada no perfil.</span><span class="sxs-lookup"><span data-stu-id="ffdb5-161">This data unit extension is not configured in the profile.</span></span> <span data-ttu-id="ffdb5-162">Ele é incluído na saída de exemplos do decodificador.</span><span class="sxs-lookup"><span data-stu-id="ffdb5-162">It is included in samples output from the decoder.</span></span><br/> <span data-ttu-id="ffdb5-163">O tamanho desta conclusão é sempre WM_SampleExtension_ChromaLocation_Size, que é de 1 byte.</span><span class="sxs-lookup"><span data-stu-id="ffdb5-163">The size of this DUE is always WM_SampleExtension_ChromaLocation_Size, which is 1 byte.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ffdb5-164">WM_SampleExtensionGUID_ColorSpaceInfo</span><span class="sxs-lookup"><span data-stu-id="ffdb5-164">WM_SampleExtensionGUID_ColorSpaceInfo</span></span></td>
<td><span data-ttu-id="ffdb5-165">Os dados fornecem informações sobre o espaço de cores usado para o quadro de vídeo atual. O valor dessa extensão é uma estrutura de <a href="/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmt_colorspaceinfo_extension_data"><strong>WMT_COLORSPACEINFO_EXTENSION_DATA</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="ffdb5-165">The data provides information about the color space used for the current video frame.The value of this extension is a <a href="/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmt_colorspaceinfo_extension_data"><strong>WMT_COLORSPACEINFO_EXTENSION_DATA</strong></a> structure.</span></span><br/> <span data-ttu-id="ffdb5-166">Esta extensão de unidade de dados não está configurada no perfil.</span><span class="sxs-lookup"><span data-stu-id="ffdb5-166">This data unit extension is not configured in the profile.</span></span> <span data-ttu-id="ffdb5-167">Ele é incluído na saída de exemplos do decodificador.</span><span class="sxs-lookup"><span data-stu-id="ffdb5-167">It is included in samples output from the decoder.</span></span><br/> <span data-ttu-id="ffdb5-168">O tamanho desta conclusão é sempre WM_SampleExtension_ColorSpaceInfo_Size, que é de 3 bytes.</span><span class="sxs-lookup"><span data-stu-id="ffdb5-168">The size of this DUE is always WM_SampleExtension_ColorSpaceInfo_Size, which is 3 bytes.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ffdb5-169">WM_SampleExtensionGUID_UserDataInfo</span><span class="sxs-lookup"><span data-stu-id="ffdb5-169">WM_SampleExtensionGUID_UserDataInfo</span></span></td>
<td><span data-ttu-id="ffdb5-170">Os dados são dados de usuário personalizados. Os quatro primeiros bytes dos dados contêm o tamanho dos dados personalizados.</span><span class="sxs-lookup"><span data-stu-id="ffdb5-170">The data is custom user data.The first four bytes of the data contain the size of the custom data.</span></span><br/> <span data-ttu-id="ffdb5-171">O próximo byte contém os tipos de dados de usuário fornecidos na extensão de exemplo.</span><span class="sxs-lookup"><span data-stu-id="ffdb5-171">The next byte contains the type of user data provided in the sample extension.</span></span> <span data-ttu-id="ffdb5-172">Os seguintes tipos têm suporte:</span><span class="sxs-lookup"><span data-stu-id="ffdb5-172">The following types are supported:</span></span><br/>
<ul>
<li><span data-ttu-id="ffdb5-173">0x1F-dados de usuário de nível de sequência</span><span class="sxs-lookup"><span data-stu-id="ffdb5-173">0x1F - Sequence level user data</span></span></li>
<li><span data-ttu-id="ffdb5-174">0x1E-dados de usuário do nível de ponto de entrada</span><span class="sxs-lookup"><span data-stu-id="ffdb5-174">0x1E - Entry-point level user data</span></span></li>
<li><span data-ttu-id="ffdb5-175">0x1D-dados de usuário de nível de quadro</span><span class="sxs-lookup"><span data-stu-id="ffdb5-175">0x1D - Frame level user data</span></span></li>
<li><span data-ttu-id="ffdb5-176">0x1C-dados de usuário de nível de campo</span><span class="sxs-lookup"><span data-stu-id="ffdb5-176">0x1C - Field level user data</span></span></li>
<li><span data-ttu-id="ffdb5-177">0x1B-dados de usuário de nível de fatia</span><span class="sxs-lookup"><span data-stu-id="ffdb5-177">0x1B - Slice level user data</span></span></li>
</ul>
<span data-ttu-id="ffdb5-178">O sexto e os bytes subsequentes contêm os dados do usuário.</span><span class="sxs-lookup"><span data-stu-id="ffdb5-178">The sixth and subsequent bytes contain the user data.</span></span> <span data-ttu-id="ffdb5-179">Há quantos bytes de dados de usuário são especificados pelo número nos primeiros quatro bytes.</span><span class="sxs-lookup"><span data-stu-id="ffdb5-179">There are as many bytes of user data as specified by the number in the first four bytes.</span></span><br/> <span data-ttu-id="ffdb5-180">Esta extensão de unidade de dados não está configurada no perfil.</span><span class="sxs-lookup"><span data-stu-id="ffdb5-180">This data unit extension is not configured in the profile.</span></span> <span data-ttu-id="ffdb5-181">Ele é incluído em exemplos que são gerados do decodificador.</span><span class="sxs-lookup"><span data-stu-id="ffdb5-181">It is included in samples that are output from the decoder.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ffdb5-182">WM_SampleExtensionGUID_SampleProtectionSalt</span><span class="sxs-lookup"><span data-stu-id="ffdb5-182">WM_SampleExtensionGUID_SampleProtectionSalt</span></span></td>
<td><span data-ttu-id="ffdb5-183">Os dados são criptografados por exemplo.</span><span class="sxs-lookup"><span data-stu-id="ffdb5-183">The data is encrypted by sample.</span></span> <span data-ttu-id="ffdb5-184">Esse tipo de extensão de exemplo é usado para o conteúdo que é importado de um formato de arquivo não ASF e um esquema de proteção de direitos que não seja o DRM do Windows Media. Ao importar conteúdo protegido, cada amostra deve incluir um Salt exclusivo.</span><span class="sxs-lookup"><span data-stu-id="ffdb5-184">This sample extension type is used for content that is imported from a non-ASF file format and a rights protection scheme other than Windows Media DRM.When importing protected content, each sample must include a unique salt.</span></span> <span data-ttu-id="ffdb5-185">Normalmente, esse valor é um contador que aumenta de forma monotônico.</span><span class="sxs-lookup"><span data-stu-id="ffdb5-185">Typically, this value is a monotonically increasing counter.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="ffdb5-186">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ffdb5-186">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ffdb5-187">**Referência de programação**</span><span class="sxs-lookup"><span data-stu-id="ffdb5-187">**Programming Reference**</span></span>](programming-reference.md)
</dt> </dl>

 

 





