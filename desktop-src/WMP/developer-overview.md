---
title: Visão geral do desenvolvedor
description: Visão geral do desenvolvedor
ms.assetid: 72a330b4-5957-4159-b5e8-0c9a4491b589
keywords:
- Plug-ins do Windows Media Player, visualizações
- plug-ins, visualizações
- visualizações, visão geral do desenvolvedor
- visualizações personalizadas, visão geral do desenvolvedor
- visualizações, controles COM
- visualizações personalizadas, controles COM
- visualizações, entrada de áudio
- visualizações personalizadas, entrada de áudio
- visualizações, saída gráfica
- visualizações personalizadas, saída gráfica
- visualizações, ferramentas de desenho
- visualizações personalizadas, ferramentas de desenho
- visualizações, linguagem de programação
- visualizações personalizadas, linguagem de programação
- visualizações, Visual C++
- visualizações personalizadas, Visual C++
- visualizações, assistente de plug-in
- visualizações personalizadas, assistente de plug-in
- Assistente de plug-in
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36ec8632bd5611e081a4a17d1b0390dc99a09703
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292468"
---
# <a name="developer-overview"></a><span data-ttu-id="1d31e-122">Visão geral do desenvolvedor</span><span class="sxs-lookup"><span data-stu-id="1d31e-122">Developer Overview</span></span>

<span data-ttu-id="1d31e-123">Do ponto de vista do desenvolvedor, as visualizações são programas de software que pegam os dados de áudio fornecidos pelo Windows Media Player e convertem esses dados em elementos gráficos que serão o olho do usuário.</span><span class="sxs-lookup"><span data-stu-id="1d31e-123">From the developer's point of view, visualizations are software programs that take audio data provided by Windows Media Player and convert that data to graphics that will please the eye of the user.</span></span> <span data-ttu-id="1d31e-124">Os principais assuntos que um desenvolvedor precisa entender para criar uma nova visualização são os seguintes:</span><span class="sxs-lookup"><span data-stu-id="1d31e-124">The main subjects a developer needs to understand to create a new visualization are the following:</span></span>

## <a name="visualization-packaging"></a><span data-ttu-id="1d31e-125">Empacotamento de visualização</span><span class="sxs-lookup"><span data-stu-id="1d31e-125">Visualization Packaging</span></span>

<span data-ttu-id="1d31e-126">As visualizações são controles COM que o Windows Media Player usa para ativar as ondas de forma de áudio em gráficos animados no Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="1d31e-126">Visualizations are COM controls that Windows Media Player uses to turn audio waveforms into animated graphics in Microsoft Windows.</span></span> <span data-ttu-id="1d31e-127">Os controles COM são empacotados como DLLs (bibliotecas de vínculo dinâmico) do Microsoft Windows e devem ser registrados no registro do Windows.</span><span class="sxs-lookup"><span data-stu-id="1d31e-127">The COM controls are packaged as Microsoft Windows dynamic-link libraries (DLLs) and must be registered in the Windows registry.</span></span> <span data-ttu-id="1d31e-128">Quando o Windows Media Player é executado, as visualizações personalizadas registradas são carregadas e exibidas de acordo com as instruções da capa que o Windows Media Player está usando.</span><span class="sxs-lookup"><span data-stu-id="1d31e-128">When Windows Media Player runs, registered custom visualizations are loaded and viewed in accordance with the instructions of the skin that Windows Media Player is using.</span></span>

## <a name="audio-input"></a><span data-ttu-id="1d31e-129">Entrada de áudio</span><span class="sxs-lookup"><span data-stu-id="1d31e-129">Audio Input</span></span>

<span data-ttu-id="1d31e-130">O Windows Media Player fornece seu código com instantâneos de frequência de áudio e dados de formato de onda em intervalos de tempo medidos em frações de um segundo.</span><span class="sxs-lookup"><span data-stu-id="1d31e-130">Windows Media Player provides your code with snapshots of audio frequency and waveform data at timed intervals measured in fractions of a second.</span></span> <span data-ttu-id="1d31e-131">O intervalo de instantâneos é determinado internamente pelo Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="1d31e-131">The snapshot interval is internally determined by the Windows Media Player.</span></span>

## <a name="graphical-output"></a><span data-ttu-id="1d31e-132">Saída gráfica</span><span class="sxs-lookup"><span data-stu-id="1d31e-132">Graphical Output</span></span>

<span data-ttu-id="1d31e-133">A saída gráfica de sua visualização é um contexto de dispositivo do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="1d31e-133">The graphical output from your visualization is a Microsoft Windows device context.</span></span> <span data-ttu-id="1d31e-134">Essa é uma superfície de desenho padrão do Windows que você pode desenhar sempre que um instantâneo de áudio é fornecido.</span><span class="sxs-lookup"><span data-stu-id="1d31e-134">This is a standard Windows drawing surface that you can draw upon every time an audio snapshot is provided.</span></span> <span data-ttu-id="1d31e-135">Toda a tecnologia Windows em segundo plano é levada em sua atenção.</span><span class="sxs-lookup"><span data-stu-id="1d31e-135">All of the background Windows technology is taken care of for you.</span></span> <span data-ttu-id="1d31e-136">Basta desenhar no contexto do dispositivo com os dados de áudio fornecidos.</span><span class="sxs-lookup"><span data-stu-id="1d31e-136">You just have to draw on the device context with the audio data provided.</span></span>

## <a name="drawing-tools"></a><span data-ttu-id="1d31e-137">Ferramentas de desenho</span><span class="sxs-lookup"><span data-stu-id="1d31e-137">Drawing Tools</span></span>

<span data-ttu-id="1d31e-138">Você pode desenhar no contexto do dispositivo com funções padrão do Microsoft Windows Graphics Device Interface (GDI), usando canetas e pincéis para criar designs que são modificados pelos dados de áudio fornecidos para você pelo Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="1d31e-138">You can draw on the device context with standard Microsoft Windows Graphics Device Interface (GDI) functions, using pens and brushes to create designs that are modified by the audio data supplied to you by Windows Media Player.</span></span> <span data-ttu-id="1d31e-139">O GDI fornece um rico conjunto de ferramentas de desenho que podem criar muitos tipos de efeitos visuais.</span><span class="sxs-lookup"><span data-stu-id="1d31e-139">GDI provides a rich set of drawing tools that can create many kinds of visual effects.</span></span>

## <a name="programming-language"></a><span data-ttu-id="1d31e-140">Linguagem de programação</span><span class="sxs-lookup"><span data-stu-id="1d31e-140">Programming Language</span></span>

<span data-ttu-id="1d31e-141">Microsoft Visual C++ 6,0 e superior é a única linguagem com suporte para a criação de visualizações personalizadas.</span><span class="sxs-lookup"><span data-stu-id="1d31e-141">Microsoft Visual C++ 6.0 and higher is the only supported language for creating custom visualizations.</span></span>

## <a name="plug-in-wizard"></a><span data-ttu-id="1d31e-142">Assistente de plug-in</span><span class="sxs-lookup"><span data-stu-id="1d31e-142">Plug-in Wizard</span></span>

<span data-ttu-id="1d31e-143">O Windows Media Player fornece um assistente COM que você pode adicionar ao Visual C++ que irá gerar o código subjacente necessário para sua visualização.</span><span class="sxs-lookup"><span data-stu-id="1d31e-143">Windows Media Player provides a COM wizard that you can add to Visual C++ that will generate the underlying code needed for your visualization.</span></span> <span data-ttu-id="1d31e-144">Não apenas todos os arquivos de origem são fornecidos, mas uma amostra de aparência é gerada para facilitar o teste da visualização.</span><span class="sxs-lookup"><span data-stu-id="1d31e-144">Not only are all source files provided, but a sample skin is generated to make it easy to test your visualization.</span></span> <span data-ttu-id="1d31e-145">O código gerado cria uma visualização semelhante a barras, com duas predefinições.</span><span class="sxs-lookup"><span data-stu-id="1d31e-145">The generated code creates a visualization similar to Bars, with two presets.</span></span> <span data-ttu-id="1d31e-146">Em seguida, você pode modificar o código para criar sua própria visualização.</span><span class="sxs-lookup"><span data-stu-id="1d31e-146">You can then modify the code to create your own visualization.</span></span> <span data-ttu-id="1d31e-147">Um arquivo de registro também é gerado para registrar sua visualização para que o Windows Media Player possa carregá-lo.</span><span class="sxs-lookup"><span data-stu-id="1d31e-147">A registry file is also generated to register your visualization so that Windows Media Player can load it.</span></span>

<span data-ttu-id="1d31e-148">O tópico a seguir descreve como o código de visualização processa os dados de áudio:</span><span class="sxs-lookup"><span data-stu-id="1d31e-148">The following topic describes how visualization code processes audio data:</span></span>

-   [<span data-ttu-id="1d31e-149">Fluxo de controle</span><span class="sxs-lookup"><span data-stu-id="1d31e-149">Flow of Control</span></span>](flow-of-control.md)

## <a name="related-topics"></a><span data-ttu-id="1d31e-150">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="1d31e-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1d31e-151">**Sobre visualizações personalizadas**</span><span class="sxs-lookup"><span data-stu-id="1d31e-151">**About Custom Visualizations**</span></span>](about-custom-visualizations.md)
</dt> </dl>

 

 




