---
title: Como funciona o Gerenciador de compactação de áudio
description: Como funciona o Gerenciador de compactação de áudio
ms.assetid: 7f1c3f21-262f-42a1-b9f7-069fb13b9d8f
keywords:
- áudio de multimídia, Gerenciador de compactação de áudio (ACM)
- áudio, Gerenciador de compactação de áudio (ACM)
- Gerenciador de compactação de áudio (ACM), sobre
- ACM (Gerenciador de compactação de áudio), sobre
- Gerenciador de compactação de áudio (ACM), drivers de codec
- ACM (Gerenciador de compactação de áudio), drivers de codec
- Gerenciador de compactação de áudio (ACM), drivers de conversor de formato
- ACM (Gerenciador de compactação de áudio), drivers de conversor de formato
- Gerenciador de compactação de áudio (ACM), filtrar drivers
- ACM (Gerenciador de compactação de áudio), drivers de filtro
- Gerenciador de compactação de áudio (ACM), drivers de compressor
- ACM (Gerenciador de compactação de áudio), drivers de compressor
- Gerenciador de compactação de áudio (ACM), drivers de descompactação
- ACM (Gerenciador de compactação de áudio), drivers de descompactação
- drivers de codec
- drivers do conversor de formato
- drivers de filtro
- drivers de compressor
- drivers de descompactação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14b861d381dfc28307c090dbb71b93db8e58e90a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292339"
---
# <a name="how-the-audio-compression-manager-works"></a><span data-ttu-id="44ec3-122">Como funciona o Gerenciador de compactação de áudio</span><span class="sxs-lookup"><span data-stu-id="44ec3-122">How the Audio Compression Manager Works</span></span>

<span data-ttu-id="44ec3-123">O ACM usa ganchos de interface de driver existentes para substituir o algoritmo de mapeamento padrão para dispositivos de formato de onda-áudio.</span><span class="sxs-lookup"><span data-stu-id="44ec3-123">The ACM uses existing driver interface hooks to override the default mapping algorithm for waveform-audio devices.</span></span> <span data-ttu-id="44ec3-124">Isso permite que o ACM intercepte chamadas de abertura de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="44ec3-124">This allows the ACM to intercept device-open calls.</span></span> <span data-ttu-id="44ec3-125">Depois que uma chamada foi interceptada, o ACM pode executar uma variedade de tarefas para processar os dados de áudio, como inserir um compressor externo ou descompactar na sequência.</span><span class="sxs-lookup"><span data-stu-id="44ec3-125">After a call has been intercepted, the ACM can perform a variety of tasks to process the audio data, such as inserting an external compressor or decompressor into the sequence.</span></span>

<span data-ttu-id="44ec3-126">O ACM gerencia os seguintes tipos de drivers:</span><span class="sxs-lookup"><span data-stu-id="44ec3-126">The ACM manages the following types of drivers:</span></span>

-   <span data-ttu-id="44ec3-127">Drivers de compactador e descompactador (codec)</span><span class="sxs-lookup"><span data-stu-id="44ec3-127">Compressor and decompressor (codec) drivers</span></span>
-   <span data-ttu-id="44ec3-128">Drivers do conversor de formato</span><span class="sxs-lookup"><span data-stu-id="44ec3-128">Format converter drivers</span></span>
-   <span data-ttu-id="44ec3-129">Drivers de filtro</span><span class="sxs-lookup"><span data-stu-id="44ec3-129">Filter drivers</span></span>

<span data-ttu-id="44ec3-130">Os compactadores e os descompactadores alteram um tipo de formato para outro.</span><span class="sxs-lookup"><span data-stu-id="44ec3-130">Compressors and decompressors change one format type to another.</span></span> <span data-ttu-id="44ec3-131">Por exemplo, um compressor ou descompactador pode alterar um arquivo de PCM (modulação de código de pulso) para um arquivo de ADPCM (modulação diferencial de código de pulso).</span><span class="sxs-lookup"><span data-stu-id="44ec3-131">For example, a compressor or decompressor can change a PCM (Pulse Code Modulation) file to an ADPCM (Adaptive Differential Pulse Code Modulation) file.</span></span> <span data-ttu-id="44ec3-132">Os conversores de formato alteram o formato, mas não o tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="44ec3-132">Format converters change the format, but not the data type.</span></span> <span data-ttu-id="44ec3-133">Por exemplo, um conversor pode alterar 44-kHz, dados de 16 bits para 44-kHz, dados de 8 bits.</span><span class="sxs-lookup"><span data-stu-id="44ec3-133">For example, a converter can change 44-kHz, 16-bit data to 44-kHz, 8-bit data.</span></span> <span data-ttu-id="44ec3-134">Os filtros não alteram o formato de dados, mas eles alteram os dados de Wave-audio de alguma maneira.</span><span class="sxs-lookup"><span data-stu-id="44ec3-134">Filters do not change the data format at all, but they change the waveform-audio data in some manner.</span></span> <span data-ttu-id="44ec3-135">Por exemplo, um filtro pode combinar um fluxo de dados e um eco de si mesmo.</span><span class="sxs-lookup"><span data-stu-id="44ec3-135">For example, a filter could combine a data stream and an echo of itself.</span></span> <span data-ttu-id="44ec3-136">Um único driver do ACM ou uma marca de filtro ou de formato em um driver pode também dar suporte a combinações dos tipos anteriores.</span><span class="sxs-lookup"><span data-stu-id="44ec3-136">A single ACM driver, or a filter tag or format tag within a driver, might also support combinations of the preceding types.</span></span>

<span data-ttu-id="44ec3-137">Para saída de Wave-Audio, o ACM passa cada buffer de dados para o conversor conforme ele chega.</span><span class="sxs-lookup"><span data-stu-id="44ec3-137">For waveform-audio output, the ACM passes each buffer of data to the converter as it arrives.</span></span> <span data-ttu-id="44ec3-138">O conversor descompacta os dados e retorna os dados descompactados para o ACM em um buffer de "sombra".</span><span class="sxs-lookup"><span data-stu-id="44ec3-138">The converter decompresses the data and returns the decompressed data to the ACM in a "shadow" buffer.</span></span> <span data-ttu-id="44ec3-139">Em seguida, o ACM passa o buffer de sombra descompactado para o driver de áudio de onda.</span><span class="sxs-lookup"><span data-stu-id="44ec3-139">The ACM then passes the decompressed shadow buffer to the waveform-audio driver.</span></span> <span data-ttu-id="44ec3-140">O ACM aloca os buffers de sombra sempre que recebe uma mensagem de preparação.</span><span class="sxs-lookup"><span data-stu-id="44ec3-140">The ACM allocates the shadow buffers whenever it receives a prepare message.</span></span>

<span data-ttu-id="44ec3-141">Para entrada de formato de onda-áudio, o ACM transmite buffers de sombra vazios para o driver.</span><span class="sxs-lookup"><span data-stu-id="44ec3-141">For waveform-audio input, the ACM passes empty shadow buffers to the driver.</span></span> <span data-ttu-id="44ec3-142">Ele usa uma tarefa em segundo plano para receber uma notificação depois que o driver preencher o buffer de sombra.</span><span class="sxs-lookup"><span data-stu-id="44ec3-142">It uses a background task to receive a notification after the driver has filled the shadow buffer.</span></span> <span data-ttu-id="44ec3-143">Em seguida, o ACM passa os buffers para o driver para a compactação.</span><span class="sxs-lookup"><span data-stu-id="44ec3-143">The ACM then passes the buffers to the driver for compression.</span></span> <span data-ttu-id="44ec3-144">Após a conclusão da compactação, o driver passa os dados para o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="44ec3-144">After compression is finished, the driver passes the data to the application.</span></span>

 

 




