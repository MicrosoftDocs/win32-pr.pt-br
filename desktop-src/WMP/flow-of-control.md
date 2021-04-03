---
title: Fluxo de controle
description: Fluxo de controle
ms.assetid: b91c0191-1908-4d62-96ce-927d09c70f9a
keywords:
- visualizações, fluxo de programa
- visualizações personalizadas, fluxo do programa
- visualizações, fluxo de controle
- visualizações personalizadas, fluxo de controle
- visualizações, eventos cronometrados
- visualizações personalizadas, eventos cronometrados
- visualizações, função render
- visualizações personalizadas, função render
- visualizações, função RenderWindow
- visualizações personalizadas, função RenderWindow
- Função render, fluxo do programa de visualização
- Função RenderWindow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bca09760d958da045c4bbf60ae122a9d0ae4c71c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916032"
---
# <a name="flow-of-control"></a><span data-ttu-id="ffe18-115">Fluxo de controle</span><span class="sxs-lookup"><span data-stu-id="ffe18-115">Flow of Control</span></span>

<span data-ttu-id="ffe18-116">Os dados de áudio entram no Windows Media Player continuamente por meio de um arquivo ou fluxo.</span><span class="sxs-lookup"><span data-stu-id="ffe18-116">Audio data comes into Windows Media Player continuously through a file or a stream.</span></span> <span data-ttu-id="ffe18-117">Esses dados são passados para sua visualização.</span><span class="sxs-lookup"><span data-stu-id="ffe18-117">That data is passed to your visualization.</span></span> <span data-ttu-id="ffe18-118">Você desenha em uma superfície definida e passa essa superfície de volta para o Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="ffe18-118">You draw on a defined surface and pass that surface back to Windows Media Player.</span></span> <span data-ttu-id="ffe18-119">Esse intercâmbio ocorre várias vezes por segundo e, para o usuário, o resultado é uma animação agradável que se move em tempo para a música.</span><span class="sxs-lookup"><span data-stu-id="ffe18-119">This interchange happens several times a second, and to the user, the result is a pleasing animation that moves in time to the music.</span></span>

<span data-ttu-id="ffe18-120">Aqui está a sequência específica do fluxo do programa de visualização:</span><span class="sxs-lookup"><span data-stu-id="ffe18-120">Here is the specific sequence of the visualization program flow:</span></span>

1.  <span data-ttu-id="ffe18-121">Em um intervalo de tempo, o Windows Media Player tira um instantâneo do áudio que está sendo executado.</span><span class="sxs-lookup"><span data-stu-id="ffe18-121">At a timed interval, Windows Media Player takes a snapshot of the audio that is playing.</span></span>
2.  <span data-ttu-id="ffe18-122">O Windows Media Player fornece os dados desse instantâneo para sua visualização por meio da função **render** e da função **RenderWindowed** .</span><span class="sxs-lookup"><span data-stu-id="ffe18-122">Windows Media Player supplies the data from that snapshot to your visualization through the **Render** function and the **RenderWindowed** function.</span></span>
3.  <span data-ttu-id="ffe18-123">Você deve escrever o código que será executado quando **render** e **RenderWindowed** for chamado.</span><span class="sxs-lookup"><span data-stu-id="ffe18-123">You must write code that will run when **Render** and **RenderWindowed** is called.</span></span> <span data-ttu-id="ffe18-124">Seu código desenha usando um contexto de dispositivo definido pelo Windows Media Player ao renderizar sem janela ou usando uma janela que você cria ao renderizar janelas.</span><span class="sxs-lookup"><span data-stu-id="ffe18-124">Your code draws by using a device context defined by Windows Media Player when rendering windowless, or by using a window that you create when rendering windowed.</span></span>
4.  <span data-ttu-id="ffe18-125">Em uma região especificada pela aparência atual, o Windows Media Player exibe o que seu código desenhou.</span><span class="sxs-lookup"><span data-stu-id="ffe18-125">In a region specified by the current skin, Windows Media Player displays what your code drew.</span></span>
5.  <span data-ttu-id="ffe18-126">Esse processo se repete várias vezes por segundo, criando animações gráficas que são cronometradas para a música.</span><span class="sxs-lookup"><span data-stu-id="ffe18-126">This process repeats several times a second, creating graphical animations that are timed to the music.</span></span> <span data-ttu-id="ffe18-127">Quando a música pára de ser reproduzida, a visualização é interrompida.</span><span class="sxs-lookup"><span data-stu-id="ffe18-127">When the music stops playing, the visualization stops.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ffe18-128">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ffe18-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ffe18-129">**Visão geral do desenvolvedor**</span><span class="sxs-lookup"><span data-stu-id="ffe18-129">**Developer Overview**</span></span>](developer-overview.md)
</dt> </dl>

 

 




