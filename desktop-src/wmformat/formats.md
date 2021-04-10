---
title: Formatos
description: Formatos
ms.assetid: 7c602643-f1fc-4fbd-a739-4296dc758bc9
keywords:
- SDK do Windows Media Format, entradas
- SDK do Windows Media Format, fluxos
- SDK do Windows Media Format, saídas
- Windows Media Format SDK, formatos
- ASF (Advanced Systems Format), entradas
- ASF (formato de sistemas avançados), entradas
- ASF (Advanced Systems Format), fluxos
- ASF (formato de sistemas avançados), fluxos
- ASF (Advanced Systems Format), saídas
- ASF (formato de sistemas avançados), saídas
- ASF (Advanced Systems Format), formatos
- ASF (formato de sistemas avançados), formatos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8e7895c27af3eb99e96d7009b79ea8df0011208
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292561"
---
# <a name="formats"></a><span data-ttu-id="70938-115">Formatos</span><span class="sxs-lookup"><span data-stu-id="70938-115">Formats</span></span>

<span data-ttu-id="70938-116">As informações em um formato descrevem tudo o que você precisa saber sobre um tipo específico de mídia.</span><span class="sxs-lookup"><span data-stu-id="70938-116">The information in a format describes everything you need to know about a particular type of media.</span></span> <span data-ttu-id="70938-117">Cada formato tem um tipo principal, como áudio ou vídeo, e pode ter um subtipo.</span><span class="sxs-lookup"><span data-stu-id="70938-117">Every format has a major type, like audio or video, and may have a subtype.</span></span> <span data-ttu-id="70938-118">Os formatos contêm informações diferentes com base no tipo principal.</span><span class="sxs-lookup"><span data-stu-id="70938-118">Formats contain different information based on major type.</span></span> <span data-ttu-id="70938-119">Os formatos de áudio e vídeo exigem muito mais informações do que outros tipos.</span><span class="sxs-lookup"><span data-stu-id="70938-119">Audio and video formats require much more information than other types.</span></span>

<span data-ttu-id="70938-120">Assim como os objetos do SDK do Windows Media Format diferenciam os números de entrada, os números de fluxo e os números de saída (consulte [entradas, fluxos e saídas](inputs-streams-and-outputs.md)), há distinções importantes entre formatos de entrada, formatos de fluxo e formatos de saída.</span><span class="sxs-lookup"><span data-stu-id="70938-120">Just as the objects of the Windows Media Format SDK differentiate between input numbers, stream numbers, and output numbers (see [Inputs, Streams and Outputs](inputs-streams-and-outputs.md)), there are important distinctions between input formats, stream formats, and output formats.</span></span> <span data-ttu-id="70938-121">Essas diferenças são descritas aqui:</span><span class="sxs-lookup"><span data-stu-id="70938-121">These differences are described here:</span></span>

## <a name="input-formats"></a><span data-ttu-id="70938-122">Formatos de entrada</span><span class="sxs-lookup"><span data-stu-id="70938-122">Input Formats</span></span>

<span data-ttu-id="70938-123">Um formato de entrada descreve a mídia digital que você passa para o objeto gravador.</span><span class="sxs-lookup"><span data-stu-id="70938-123">An input format describes the digital media that you pass to the writer object.</span></span> <span data-ttu-id="70938-124">Se um fluxo em um arquivo ASF for compactado com um codec, o codec dará suporte a apenas determinados formatos de entrada.</span><span class="sxs-lookup"><span data-stu-id="70938-124">If a stream in an ASF file is compressed with a codec, the codec will support only certain input formats.</span></span> <span data-ttu-id="70938-125">Ao usar os codecs de áudio e vídeo do Windows Media, você pode enumerar os formatos de entrada com suporte usando o objeto Writer.</span><span class="sxs-lookup"><span data-stu-id="70938-125">When using the Windows Media Audio and Video codecs, you can enumerate the supported input formats using the writer object.</span></span> <span data-ttu-id="70938-126">Ao gravar um arquivo, você é responsável por selecionar um formato de entrada que corresponda à mídia de entrada.</span><span class="sxs-lookup"><span data-stu-id="70938-126">When writing a file, you are responsible for selecting an input format that matches your input media.</span></span>

<span data-ttu-id="70938-127">Embora o formato de mídia de entrada tenha suporte do codec que compactará os dados, algumas configurações de formato de entrada não precisam corresponder ao formato de fluxo.</span><span class="sxs-lookup"><span data-stu-id="70938-127">Although the input media format must be supported by the codec that will compress the data, some input format settings need not match the stream format.</span></span> <span data-ttu-id="70938-128">Por exemplo, o formato de entrada para um fluxo de vídeo pode ter um tamanho de quadro diferente daquele definido no formato de fluxo.</span><span class="sxs-lookup"><span data-stu-id="70938-128">For example, the input format for a video stream may have a frame size that is different from that defined in the stream format.</span></span> <span data-ttu-id="70938-129">O codec executará conversões nesses casos.</span><span class="sxs-lookup"><span data-stu-id="70938-129">The codec will perform conversions in these cases.</span></span>

## <a name="stream-formats"></a><span data-ttu-id="70938-130">Formatos de fluxo</span><span class="sxs-lookup"><span data-stu-id="70938-130">Stream Formats</span></span>

<span data-ttu-id="70938-131">Um formato de fluxo descreve a forma da mídia como é armazenada no arquivo ASF.</span><span class="sxs-lookup"><span data-stu-id="70938-131">A stream format describes the form of the media as it is stored in the ASF file.</span></span> <span data-ttu-id="70938-132">O formato de fluxo é o formato descrito no perfil e pode ou não ser o mesmo que o formato de entrada e o formato de saída.</span><span class="sxs-lookup"><span data-stu-id="70938-132">The stream format is the format described in the profile, and may or may not be the same as the input format and output format.</span></span> <span data-ttu-id="70938-133">Se um codec for usado para compactar os dados em um fluxo, o formato de fluxo será diferente dos formatos de entrada e saída.</span><span class="sxs-lookup"><span data-stu-id="70938-133">If a codec is used to compress the data in a stream, the stream format will be different than the input and output formats.</span></span>

<span data-ttu-id="70938-134">Ao usar os codecs de áudio e vídeo do Windows Media, você deve obter uma lista de formatos de fluxo com suporte do codec para garantir que não esteja tentando especificar um formato ao qual o código não dá suporte.</span><span class="sxs-lookup"><span data-stu-id="70938-134">When using the Windows Media Audio and Video codecs, you must obtain a list of supported stream formats from the codec to ensure that you are not attempting to specify a format that the code does not support.</span></span> <span data-ttu-id="70938-135">Algumas configurações de formato, como a intensidade de cor e tamanho de um quadro de vídeo, devem ser configuradas manualmente após o formato do codec ser recuperado.</span><span class="sxs-lookup"><span data-stu-id="70938-135">Some format settings, such as the size and color depth of a video frame, must be configured manually after the codec format is retrieved.</span></span>

## <a name="output-formats"></a><span data-ttu-id="70938-136">Formatos de saída</span><span class="sxs-lookup"><span data-stu-id="70938-136">Output Formats</span></span>

<span data-ttu-id="70938-137">Um formato de saída descreve a mídia digital que o leitor (ou leitor síncrono) entrega para seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="70938-137">An output format describes the digital media that the reader (or synchronous reader) delivers to your application.</span></span> <span data-ttu-id="70938-138">Se um fluxo em um arquivo ASF for compactado com um codec, o codec dará suporte apenas a determinados formatos de saída.</span><span class="sxs-lookup"><span data-stu-id="70938-138">If a stream in an ASF file is compressed with a codec, the codec will support only certain output formats.</span></span> <span data-ttu-id="70938-139">Ao usar os codecs de áudio e vídeo do Windows Media, você pode enumerar os formatos de saída com suporte usando o objeto leitor.</span><span class="sxs-lookup"><span data-stu-id="70938-139">When using the Windows Media Audio and Video codecs, you can enumerate the supported output formats by using the reader object.</span></span> <span data-ttu-id="70938-140">Cada um dos codecs de mídia do Windows tem um formato de saída padrão, mas você pode selecionar qualquer formato de saída com suporte para entrega de exemplo.</span><span class="sxs-lookup"><span data-stu-id="70938-140">Each of the Windows Media codecs has a default output format, but you can select any supported output format for sample delivery.</span></span>

<span data-ttu-id="70938-141">Embora o formato de mídia de saída deva ser suportado pelo codec que expactou os dados, algumas configurações de formato de saída não precisam corresponder ao formato de fluxo.</span><span class="sxs-lookup"><span data-stu-id="70938-141">Although the output media format must be supported by the codec that compressed the data, some output format settings need not match the stream format.</span></span> <span data-ttu-id="70938-142">Por exemplo, o formato de saída para um fluxo de vídeo pode ter um tamanho de quadro diferente daquele definido no formato de fluxo.</span><span class="sxs-lookup"><span data-stu-id="70938-142">For example, the output format for a video stream may have a frame size that is different from that defined in the stream format.</span></span> <span data-ttu-id="70938-143">O codec executará conversões nesses casos.</span><span class="sxs-lookup"><span data-stu-id="70938-143">The codec will perform conversions in these cases.</span></span>

## <a name="related-topics"></a><span data-ttu-id="70938-144">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="70938-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="70938-145">**Conceitos**</span><span class="sxs-lookup"><span data-stu-id="70938-145">**Concepts**</span></span>](concepts.md)
</dt> </dl>

 

 




