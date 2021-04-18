---
title: Suporte à marca d' água
description: Suporte à marca d' água
ms.assetid: 1fafb15e-57b8-4dd0-8f0c-ccf460f05157
keywords:
- SDK do Windows Media Format, suporte a marca d' água
- SDK do Windows Media Format, marca d' água digital
- Formato de sistema avançado (ASF), suporte à marca d' água
- ASF (formato de sistemas avançados), suporte à marca d' água
- ASF (Advanced Systems Format), marca d' água digital
- ASF (formato de sistemas avançados), marca d' água digital
- SDK do Windows Media Format, DMO
- ASF (Advanced Systems Format), DMO
- ASF (formato de sistemas avançados), DMO
- SDK do Windows Media Format, interface IWMWatermarkInfo
- Formato de sistema avançado (ASF), interface IWMWatermarkInfo
- ASF (formato de sistemas avançados), interface IWMWatermarkInfo
- marca d' água, sobre
- marca d' água digital
- Objeto de mídia do DirectX (DMO), sobre
- DMO (objeto de mídia DirectX), sobre
- IWMWatermarkInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 417012cb165c0028e71af6f8b50052fdd2fab208
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "105813219"
---
# <a name="watermarking-support"></a><span data-ttu-id="cde04-120">Suporte à marca d' água</span><span class="sxs-lookup"><span data-stu-id="cde04-120">Watermarking Support</span></span>

<span data-ttu-id="cde04-121">A marca d' água digital é uma maneira de inserir direitos autorais ou outras informações nos dados de um fluxo de mídia.</span><span class="sxs-lookup"><span data-stu-id="cde04-121">Digital watermarking is a way to embed copyright or other information in the data of a media stream.</span></span> <span data-ttu-id="cde04-122">As técnicas para a marca d' água variam muito de uma solução para a próxima.</span><span class="sxs-lookup"><span data-stu-id="cde04-122">Techniques for watermarking vary widely from one solution to the next.</span></span> <span data-ttu-id="cde04-123">A forma mais simples de marca d' água é simplesmente adicionar uma imagem de identificação a cada quadro de um fluxo de vídeo.</span><span class="sxs-lookup"><span data-stu-id="cde04-123">The simplest form of watermarking is simply adding an identifying image to each frame of a video stream.</span></span> <span data-ttu-id="cde04-124">Estações de televisão frequentemente usam essa técnica para inserir um logotipo semitransparente em um canto inferior de sua difusão.</span><span class="sxs-lookup"><span data-stu-id="cde04-124">Television stations frequently use this technique to insert a semi-transparent logo in a bottom corner of their broadcast.</span></span> <span data-ttu-id="cde04-125">Formas mais sofisticadas de marca d' água digital são imperceptívels para o usuário assistir ou ouvir o conteúdo.</span><span class="sxs-lookup"><span data-stu-id="cde04-125">More sophisticated forms of digital watermarking are imperceptible to the user watching or listening to the content.</span></span>

<span data-ttu-id="cde04-126">O SDK do Windows Media Format dá suporte ao uso de [*DMOs*](wmformat-glossary.md)de marca d' água digital.</span><span class="sxs-lookup"><span data-stu-id="cde04-126">The Windows Media Format SDK supports the use of digital watermarking [*DMOs*](wmformat-glossary.md).</span></span> <span data-ttu-id="cde04-127">Na prática, um sistema de marca d' água é muito semelhante a um codec: ele usa amostras de mídia, executa algoritmos nos dados e gera os exemplos alterados.</span><span class="sxs-lookup"><span data-stu-id="cde04-127">In practice, a watermarking system is very similar to a codec: it takes media samples, runs algorithms on the data, and outputs the altered samples.</span></span> <span data-ttu-id="cde04-128">Quando um sistema de marca d' água é especificado para um fluxo, o objeto do gravador inclui o DMO em seu processamento de exemplos de entrada.</span><span class="sxs-lookup"><span data-stu-id="cde04-128">When a watermarking system is specified for a stream, the writer object includes the DMO in its processing of input samples.</span></span>

<span data-ttu-id="cde04-129">Você deve especificar informações de configuração de marca d' água ao configurar um fluxo para a marca d' água.</span><span class="sxs-lookup"><span data-stu-id="cde04-129">You must specify watermark configuration information when you configure a stream for watermarking.</span></span> <span data-ttu-id="cde04-130">Os valores de configuração serão diferentes dependendo da marca d' água do DMO.</span><span class="sxs-lookup"><span data-stu-id="cde04-130">The configuration values will be different depending upon the watermarking DMO.</span></span> <span data-ttu-id="cde04-131">O DMO que você usa deve vir com instruções que descrevem os valores de configuração que ele suporta.</span><span class="sxs-lookup"><span data-stu-id="cde04-131">The DMO you use should come with instructions describing the configuration values it supports.</span></span>

<span data-ttu-id="cde04-132">Para obter informações sobre as configurações usadas para especificar um sistema de marca d' água, consulte [ **IWMWriterAdvanced2:: SetInputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-setinputsetting)</span><span class="sxs-lookup"><span data-stu-id="cde04-132">For information about the settings used to specify a watermarking system, see [**IWMWriterAdvanced2::SetInputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-setinputsetting)</span></span>

<span data-ttu-id="cde04-133">Você pode programar seu aplicativo para enumerar o DMOs de marca d' água instalado no computador cliente.</span><span class="sxs-lookup"><span data-stu-id="cde04-133">You can program your application to enumerate the watermarking DMOs installed on the client computer.</span></span> <span data-ttu-id="cde04-134">Para obter mais informações, consulte a interface [**IWMWatermarkInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwatermarkinfo) .</span><span class="sxs-lookup"><span data-stu-id="cde04-134">For more information, see the [**IWMWatermarkInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwatermarkinfo) interface.</span></span>

## <a name="related-topics"></a><span data-ttu-id="cde04-135">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="cde04-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cde04-136">**Recursos de gravação de arquivo**</span><span class="sxs-lookup"><span data-stu-id="cde04-136">**File Writing Features**</span></span>](file-writing-features.md)
</dt> </dl>

 

 




