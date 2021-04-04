---
title: Configurações de entrada
description: Configurações de entrada
ms.assetid: 23adbb64-5733-4198-8f2b-d02052ddb848
keywords:
- SDK do Windows Media Format, constantes globais
- ASF (Advanced Systems Format), constantes globais
- ASF (formato de sistemas avançados), constantes globais
- constantes globais, lista de
- SDK do Windows Media Format, constantes
- ASF (Advanced Systems Format), constantes
- ASF (formato de sistemas avançados), constantes
- constantes, lista de
- SDK do Windows Media Format, configurações de entrada
- ASF (Advanced Systems Format), configurações de entrada
- ASF (formato de sistemas avançados), configurações de entrada
- configurações de entrada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f70ef0db6a3d9371bd1c8e9a20157f5f0ac73b3
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104007079"
---
# <a name="input-settings"></a><span data-ttu-id="641c9-115">Configurações de entrada</span><span class="sxs-lookup"><span data-stu-id="641c9-115">Input Settings</span></span>

<span data-ttu-id="641c9-116">As constantes globais a seguir são usadas para identificar as configurações de entrada para o gravador.</span><span class="sxs-lookup"><span data-stu-id="641c9-116">The following global constants are used to identify input settings for the writer.</span></span>



| <span data-ttu-id="641c9-117">Constante global</span><span class="sxs-lookup"><span data-stu-id="641c9-117">Global constant</span></span>                        | <span data-ttu-id="641c9-118">\_tipo de \_ dados attr WMT</span><span class="sxs-lookup"><span data-stu-id="641c9-118">WMT\_ATTR\_DATATYPE</span></span>                                                                                                                       | <span data-ttu-id="641c9-119">Descrição de *uma* era</span><span class="sxs-lookup"><span data-stu-id="641c9-119">Description of *pValue*</span></span>                                                                                                                                                                                                                                                 |
|----------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="641c9-120">g \_ wszDeinterlaceMode</span><span class="sxs-lookup"><span data-stu-id="641c9-120">g\_wszDeinterlaceMode</span></span>                  | <span data-ttu-id="641c9-121">**WMT \_ Digite \_ DWORD** definido como um dos valores na tabela modo no tópico [como desentrelaçar vídeo](to-deinterlace-video.md).</span><span class="sxs-lookup"><span data-stu-id="641c9-121">**WMT\_TYPE\_DWORD** set to one of the values in the mode table in the topic [To Deinterlace Video](to-deinterlace-video.md).</span></span>            | <span data-ttu-id="641c9-122">Quando definido, especifica o tipo de conteúdo entrelaçado da entrada.</span><span class="sxs-lookup"><span data-stu-id="641c9-122">When set, specifies the type of interlaced content of the input.</span></span> <span data-ttu-id="641c9-123">Para obter mais informações, consulte [para desentrelaçar vídeo](to-deinterlace-video.md).</span><span class="sxs-lookup"><span data-stu-id="641c9-123">For more information, see [To Deinterlace Video](to-deinterlace-video.md).</span></span>                                                                                                                            |
| <span data-ttu-id="641c9-124">g \_ wszFixedFrameRate</span><span class="sxs-lookup"><span data-stu-id="641c9-124">g\_wszFixedFrameRate</span></span>                   | <span data-ttu-id="641c9-125">**WMT \_ tipo \_ bool**</span><span class="sxs-lookup"><span data-stu-id="641c9-125">**WMT\_TYPE\_BOOL**</span></span>                                                                                                                       | <span data-ttu-id="641c9-126">Quando definido como true, instrui o codec para não descartar nenhum quadro durante a codificação.</span><span class="sxs-lookup"><span data-stu-id="641c9-126">When set to True, instructs the codec not to drop any frames during encoding.</span></span> <span data-ttu-id="641c9-127">Isso fará com que a [*taxa de quadros*](wmformat-glossary.md) do fluxo de vídeo de saída seja constante.</span><span class="sxs-lookup"><span data-stu-id="641c9-127">This will cause the [*frame rate*](wmformat-glossary.md) of the output video stream to be constant.</span></span> <span data-ttu-id="641c9-128">A taxa de quadros do fluxo de entrada não precisa ser constante.</span><span class="sxs-lookup"><span data-stu-id="641c9-128">The frame rate of the input stream does not need to be constant.</span></span> |
| <span data-ttu-id="641c9-129">g \_ wszInitialPatternForInverseTelecine</span><span class="sxs-lookup"><span data-stu-id="641c9-129">g\_wszInitialPatternForInverseTelecine</span></span> | <span data-ttu-id="641c9-130">**WMT \_ Digite \_ DWORD** definido como um dos valores na tabela padrão inicial no tópico [para desentrelaçar o vídeo](to-deinterlace-video.md).</span><span class="sxs-lookup"><span data-stu-id="641c9-130">**WMT\_TYPE\_DWORD** set to one of the values in the initial pattern table in the topic [To Deinterlace Video](to-deinterlace-video.md).</span></span> | <span data-ttu-id="641c9-131">Quando o modo de desentrelaçamento é definido como WM \_ DM \_ desentrelaçar \_ INVERSETELECINE, isso pode ser definido para especificar o padrão da entrada de [*telecineon*](wmformat-glossary.md) .</span><span class="sxs-lookup"><span data-stu-id="641c9-131">When the deinterlace mode is set to WM\_DM\_DEINTERLACE\_INVERSETELECINE, this can be set to specify the pattern of the [*telecine*](wmformat-glossary.md) input.</span></span> <span data-ttu-id="641c9-132">Para obter mais informações, consulte [para desentrelaçar vídeo](to-deinterlace-video.md).</span><span class="sxs-lookup"><span data-stu-id="641c9-132">For more information, see [To Deinterlace Video](to-deinterlace-video.md).</span></span>        |
| <span data-ttu-id="641c9-133">g \_ wszInterlacedCoding</span><span class="sxs-lookup"><span data-stu-id="641c9-133">g\_wszInterlacedCoding</span></span>                 | <span data-ttu-id="641c9-134">**WMT \_ tipo \_ bool**</span><span class="sxs-lookup"><span data-stu-id="641c9-134">**WMT\_TYPE\_BOOL**</span></span>                                                                                                                       | <span data-ttu-id="641c9-135">Quando definido como true, especifica que o codec deve codificar o fluxo como conteúdo entrelaçado.</span><span class="sxs-lookup"><span data-stu-id="641c9-135">When set to True, specifies that that the codec should encode the stream as interlaced content.</span></span> <span data-ttu-id="641c9-136">Para obter mais informações, consulte [para usar vídeo entrelaçado](to-use-interlaced-video.md).</span><span class="sxs-lookup"><span data-stu-id="641c9-136">For more information, see [To Use Interlaced Video](to-use-interlaced-video.md).</span></span>                                                                                       |
| <span data-ttu-id="641c9-137">g \_ wszJPEGCompressionQuality</span><span class="sxs-lookup"><span data-stu-id="641c9-137">g\_wszJPEGCompressionQuality</span></span>           | <span data-ttu-id="641c9-138">**WMT \_ tipo \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="641c9-138">**WMT\_TYPE\_DWORD**</span></span>                                                                                                                      | <span data-ttu-id="641c9-139">Especifica o nível de qualidade JPEG (de 1 a 100) a ser usado na entrada.</span><span class="sxs-lookup"><span data-stu-id="641c9-139">Specifies the JPEG quality level (from 1 to 100) to be used on the input.</span></span>                                                                                                                                                                                               |
| <span data-ttu-id="641c9-140">g \_ wszWatermarkCLSID</span><span class="sxs-lookup"><span data-stu-id="641c9-140">g\_wszWatermarkCLSID</span></span>                   | <span data-ttu-id="641c9-141">**\_GUID do tipo WMT \_**</span><span class="sxs-lookup"><span data-stu-id="641c9-141">**WMT\_TYPE\_GUID**</span></span>                                                                                                                       | <span data-ttu-id="641c9-142">O valor é definido como o GUID de marca d' água.</span><span class="sxs-lookup"><span data-stu-id="641c9-142">The value is set to the watermark GUID.</span></span>                                                                                                                                                                                                                                 |
| <span data-ttu-id="641c9-143">g \_ wszWatermarkConfig</span><span class="sxs-lookup"><span data-stu-id="641c9-143">g\_wszWatermarkConfig</span></span>                  | <span data-ttu-id="641c9-144">**Cadeia de caracteres do \_ tipo WMT \_**</span><span class="sxs-lookup"><span data-stu-id="641c9-144">**WMT\_TYPE\_STRING**</span></span>                                                                                                                     | <span data-ttu-id="641c9-145">O valor é definido como a configuração da marca d' água.</span><span class="sxs-lookup"><span data-stu-id="641c9-145">The value is set to the watermark configuration.</span></span> <span data-ttu-id="641c9-146">Esse valor variará dependendo da marca d' água do DMO.</span><span class="sxs-lookup"><span data-stu-id="641c9-146">This value will vary depending upon the watermarking DMO.</span></span> <span data-ttu-id="641c9-147">Consulte a documentação do sistema de marca d' água para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="641c9-147">Consult the documentation of the watermarking system for more information.</span></span>                                                                                   |



 

> [!Note]  
> <span data-ttu-id="641c9-148">As configurações de entrada configuradas para um fluxo não são mantidas no arquivo gravado.</span><span class="sxs-lookup"><span data-stu-id="641c9-148">The input settings configured for a stream are not persisted in the written file.</span></span> <span data-ttu-id="641c9-149">Se desejar que seu leitor personalizado tenha acesso a esses parâmetros de codificação, você deverá criar atributos personalizados para armazená-los no cabeçalho do arquivo.</span><span class="sxs-lookup"><span data-stu-id="641c9-149">If you want your custom reader to have access to these encoding parameters, you must create custom attributes to store them in the file header.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="641c9-150">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="641c9-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="641c9-151">**IWMWriterAdvanced2::GetInputSetting**</span><span class="sxs-lookup"><span data-stu-id="641c9-151">**IWMWriterAdvanced2::GetInputSetting**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-getinputsetting)
</dt> <dt>

[<span data-ttu-id="641c9-152">**IWMWriterAdvanced2::SetInputSetting**</span><span class="sxs-lookup"><span data-stu-id="641c9-152">**IWMWriterAdvanced2::SetInputSetting**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-setinputsetting)
</dt> </dl>

 

 




