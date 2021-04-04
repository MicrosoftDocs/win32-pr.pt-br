---
title: Implementando renderização
description: Implementando renderização
ms.assetid: 9b3a64f6-6803-457c-8e63-e8a799089e18
keywords:
- visualizações, eventos cronometrados
- visualizações personalizadas, eventos cronometrados
- visualizações, função render
- visualizações personalizadas, função render
- visualizações, função RenderWindow
- visualizações personalizadas, função RenderWindow
- Processar função, parâmetros
- Função RenderWindow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99db0a96a07c361d18de579fb0235befa11838c8
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104007117"
---
# <a name="implementing-render"></a><span data-ttu-id="4952e-111">Implementando renderização</span><span class="sxs-lookup"><span data-stu-id="4952e-111">Implementing Render</span></span>

<span data-ttu-id="4952e-112">A maneira mais fácil de considerar a programação de visualização é que você está criando um manipulador para um evento cronometrado.</span><span class="sxs-lookup"><span data-stu-id="4952e-112">The easiest way to think of visualization programming is that you are creating a handler for a timed event.</span></span> <span data-ttu-id="4952e-113">Em intervalos específicos, o Windows Media Player tira um instantâneo dos dados de áudio que está jogando e fornece os dados de instantâneo para a visualização atualmente carregada.</span><span class="sxs-lookup"><span data-stu-id="4952e-113">At specific intervals, Windows Media Player takes a snapshot of the audio data it is playing, and provides the snapshot data to the currently loaded visualization.</span></span> <span data-ttu-id="4952e-114">Isso é semelhante à programação orientada a eventos e faz parte do modelo de programação do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="4952e-114">This is similar to event-driven programming and is part of the programming model of Microsoft Windows.</span></span> <span data-ttu-id="4952e-115">Você escreve o código e aguarda que ele seja chamado por um evento específico.</span><span class="sxs-lookup"><span data-stu-id="4952e-115">You write code and wait for it to be called by a particular event.</span></span>

<span data-ttu-id="4952e-116">Se o seu código for uma implementação da função [IWMPEffects:: render](/previous-versions/windows/desktop/api/effects/nf-effects-iwmpeffects-render) para renderização no modo sem janela, ele receberá os seguintes parâmetros:</span><span class="sxs-lookup"><span data-stu-id="4952e-116">If your code is an implementation of the [IWMPEffects::Render](/previous-versions/windows/desktop/api/effects/nf-effects-iwmpeffects-render) function for rendering in windowless mode, it receives the following parameters:</span></span>

<span data-ttu-id="4952e-117">*TimedLevel*</span><span class="sxs-lookup"><span data-stu-id="4952e-117">*TimedLevel*</span></span>

<span data-ttu-id="4952e-118">Essa é uma estrutura que define os dados de áudio que seu código analisará.</span><span class="sxs-lookup"><span data-stu-id="4952e-118">This is a structure that defines the audio data your code will be analyzing.</span></span> <span data-ttu-id="4952e-119">A estrutura é composta de duas matrizes.</span><span class="sxs-lookup"><span data-stu-id="4952e-119">The structure is composed of two arrays.</span></span> <span data-ttu-id="4952e-120">A primeira matriz é baseada em informações de frequência e contém um instantâneo do espectro de áudio dividido em 1024 partes.</span><span class="sxs-lookup"><span data-stu-id="4952e-120">The first array is based on frequency information and contains a snapshot of the audio spectrum divided into 1024 portions.</span></span> <span data-ttu-id="4952e-121">Cada célula da matriz contém um valor de 0 a 255.</span><span class="sxs-lookup"><span data-stu-id="4952e-121">Each cell of the array contains a value from 0 to 255.</span></span> <span data-ttu-id="4952e-122">A primeira célula começa em 20 Hz e a última em 22050 Hz.</span><span class="sxs-lookup"><span data-stu-id="4952e-122">The first cell starts at 20 Hz and the last at 22050 Hz.</span></span> <span data-ttu-id="4952e-123">A matriz é bidimensional para representar áudio estéreo.</span><span class="sxs-lookup"><span data-stu-id="4952e-123">The array is two dimensional to represent stereo audio.</span></span> <span data-ttu-id="4952e-124">A segunda matriz baseia-se nas informações de forma de onda e corresponde à energia de áudio, em que quanto mais forte for a onda, maior será o valor.</span><span class="sxs-lookup"><span data-stu-id="4952e-124">The second array is based on waveform information and corresponds to audio power, where the stronger the wave is, the larger the value.</span></span> <span data-ttu-id="4952e-125">A matriz de forma de onda é um instantâneo granular das últimas 1024 fatias de energia de áudio executadas em intervalos de tempo muito pequenos.</span><span class="sxs-lookup"><span data-stu-id="4952e-125">The waveform array is a granular snapshot of the last 1024 slices of audio power taken at very small time intervals.</span></span> <span data-ttu-id="4952e-126">Essa matriz também é bidimensional para representar áudio estéreo.</span><span class="sxs-lookup"><span data-stu-id="4952e-126">This array also is two dimensional to represent stereo audio.</span></span>

<span data-ttu-id="4952e-127">*HDC*</span><span class="sxs-lookup"><span data-stu-id="4952e-127">*HDC*</span></span>

<span data-ttu-id="4952e-128">Trata-se de um identificador do Microsoft Windows para um contexto de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="4952e-128">This is a Microsoft Windows handle to a device context.</span></span> <span data-ttu-id="4952e-129">Isso oferece uma maneira de identificar a superfície de desenho para o Windows.</span><span class="sxs-lookup"><span data-stu-id="4952e-129">This gives a way to identify the drawing surface to Windows.</span></span> <span data-ttu-id="4952e-130">Você não precisa criá-lo, só precisa usá-lo para chamadas de função de desenho específicas.</span><span class="sxs-lookup"><span data-stu-id="4952e-130">You do not need to create it, you just need to use it for specific drawing function calls.</span></span>

<span data-ttu-id="4952e-131">*RECT*</span><span class="sxs-lookup"><span data-stu-id="4952e-131">*RECT*</span></span>

<span data-ttu-id="4952e-132">Este é um retângulo do Microsoft Windows que define o tamanho de uma superfície de desenho.</span><span class="sxs-lookup"><span data-stu-id="4952e-132">This is a Microsoft Windows rectangle that defines the size of a drawing surface.</span></span> <span data-ttu-id="4952e-133">Este é um retângulo simples com quatro propriedades: **esquerda**, **direita**, **superior** e **inferior**.</span><span class="sxs-lookup"><span data-stu-id="4952e-133">This is a simple rectangle with four properties: **left**, **right**, **top**, and **bottom**.</span></span> <span data-ttu-id="4952e-134">Os valores reais são fornecidos pelo Windows Media Player para que você possa determinar como o usuário ou o desenvolvedor de capa dimensionará a janela que você desenhará.</span><span class="sxs-lookup"><span data-stu-id="4952e-134">The actual values are supplied by Windows Media Player so that you can determine how the user or skin developer has sized the window you will draw on.</span></span> <span data-ttu-id="4952e-135">Ele também determina a posição no HDC em que o efeito deve renderizar.</span><span class="sxs-lookup"><span data-stu-id="4952e-135">It also determines the position on the HDC that the effect is supposed to render on.</span></span>

<span data-ttu-id="4952e-136">Se o seu código for uma implementação da função **IWMPEffects2:: RenderWindowed** para renderização em uma janela, ele receberá os seguintes parâmetros:</span><span class="sxs-lookup"><span data-stu-id="4952e-136">If your code is an implementation of the **IWMPEffects2::RenderWindowed** function for rendering in a window, it receives the following parameters:</span></span>

<span data-ttu-id="4952e-137">*TimedLevel*</span><span class="sxs-lookup"><span data-stu-id="4952e-137">*TimedLevel*</span></span>

<span data-ttu-id="4952e-138">Essas são as mesmas informações que a função **render** recebe.</span><span class="sxs-lookup"><span data-stu-id="4952e-138">This is the same information that the **Render** function receives.</span></span>

<span data-ttu-id="4952e-139">*fRequiredRender*</span><span class="sxs-lookup"><span data-stu-id="4952e-139">*fRequiredRender*</span></span>

<span data-ttu-id="4952e-140">O parâmetro *fRequiredRender* informa que sua visualização deve redesenhar a si mesma, por exemplo, quando outra janela é arrastada sobre ela.</span><span class="sxs-lookup"><span data-stu-id="4952e-140">The *fRequiredRender* parameter informs you that your visualization must repaint itself—for example, when another window is dragged over it.</span></span> <span data-ttu-id="4952e-141">Quando esse valor for false, você poderá ignorar com segurança o código de renderização se o item de mídia atual for interrompido ou pausado.</span><span class="sxs-lookup"><span data-stu-id="4952e-141">When this value is false, you can safely skip over the rendering code if the current media item is stopped or paused.</span></span> <span data-ttu-id="4952e-142">Isso permite evitar o consumo de ciclos de CPU desnecessariamente.</span><span class="sxs-lookup"><span data-stu-id="4952e-142">This lets you avoid consuming CPU cycles unnecessarily.</span></span>

<span data-ttu-id="4952e-143">O plug-in de exemplo gerado pelo assistente de plug-in não fornece uma implementação personalizada para **RenderWindowed**.</span><span class="sxs-lookup"><span data-stu-id="4952e-143">The sample plug-in generated by the Plug-in Wizard does not provide a custom implementation for **RenderWindowed**.</span></span> <span data-ttu-id="4952e-144">Em vez disso, o código de plug-in de exemplo recupera o contexto do dispositivo da janela pai fornecida pelo Windows Media Player em [IWMPEffects2:: Create](/previous-versions/windows/desktop/api/effects/nf-effects-iwmpeffects2-create), recupera as dimensões da janela pai como uma estrutura RECT e, em seguida, chama para **render** usando o contexto do dispositivo, o Rect e o ponteiro de nível cronometrado de **RenderWindowed**.</span><span class="sxs-lookup"><span data-stu-id="4952e-144">Instead, the sample plug-in code retrieves the device context from the parent window provided by Windows Media Player in [IWMPEffects2::Create](/previous-versions/windows/desktop/api/effects/nf-effects-iwmpeffects2-create), then retrieves the dimensions of the parent window as a RECT structure, and then calls through to **Render** using the device context, the RECT, and the timed level pointer from **RenderWindowed**.</span></span>

<span data-ttu-id="4952e-145">As seções a seguir fornecem mais informações sobre como implementar o **render**:</span><span class="sxs-lookup"><span data-stu-id="4952e-145">The following sections provide more information about implementing **Render**:</span></span>

-   [<span data-ttu-id="4952e-146">Usando níveis de tempo</span><span class="sxs-lookup"><span data-stu-id="4952e-146">Using Timed Levels</span></span>](using-timed-levels.md)
-   [<span data-ttu-id="4952e-147">Usando contextos de dispositivo</span><span class="sxs-lookup"><span data-stu-id="4952e-147">Using Device Contexts</span></span>](using-device-contexts.md)
-   [<span data-ttu-id="4952e-148">Usando retângulos</span><span class="sxs-lookup"><span data-stu-id="4952e-148">Using Rectangles</span></span>](using-rectangles.md)
-   [<span data-ttu-id="4952e-149">Exemplo de código de renderização</span><span class="sxs-lookup"><span data-stu-id="4952e-149">Sample Render Code</span></span>](sample-render-code.md)

## <a name="related-topics"></a><span data-ttu-id="4952e-150">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="4952e-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4952e-151">**Implementando seu código**</span><span class="sxs-lookup"><span data-stu-id="4952e-151">**Implementing Your Code**</span></span>](implementing-your-code.md)
</dt> </dl>

 

 




