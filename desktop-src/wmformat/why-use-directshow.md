---
title: Por que usar o DirectShow
description: Por que usar o DirectShow
ms.assetid: 0ab33526-73d0-425e-a03f-29c74555f578
keywords:
- SDK do Windows Media Format, DirectShow
- SDK do Windows Media Format, hardware
- SDK do Windows Media Format, Windows Driver Model (WDM)
- ASF (Advanced Systems Format), DirectShow
- ASF (formato de sistemas avançados), DirectShow
- ASF (Advanced Systems Format), hardware
- ASF (formato de sistemas avançados), hardware
- ASF (Advanced Systems Format), Windows Driver Model (WDM)
- ASF (formato de sistemas avançados), Windows Driver Model (WDM)
- DirectShow, sobre
- DirectShow, hardware
- DirectShow, Windows Driver Model (WDM)
- Windows Driver Model (WDM)
- WDM (Windows Driver Model)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f90fa1de01a7b136b938f9b09cc7fb2b3c229fad
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103635859"
---
# <a name="why-use-directshow"></a><span data-ttu-id="e0eaf-117">Por que usar o DirectShow?</span><span class="sxs-lookup"><span data-stu-id="e0eaf-117">Why Use DirectShow?</span></span>

<span data-ttu-id="e0eaf-118">Há dois motivos principais pelos quais um aplicativo pode usar o DirectShow em vez do SDK do Windows Media Format diretamente: para a conveniência da arquitetura de streaming do DirectShow e para acesso ao hardware.</span><span class="sxs-lookup"><span data-stu-id="e0eaf-118">There are two main reasons why an application might use DirectShow rather than the Windows Media Format SDK directly: for the convenience of the DirectShow streaming architecture, and for access to hardware.</span></span>

## <a name="convenience"></a><span data-ttu-id="e0eaf-119">Conveniência</span><span class="sxs-lookup"><span data-stu-id="e0eaf-119">Convenience</span></span>

<span data-ttu-id="e0eaf-120">Com a arquitetura de streaming do DirectShow, é necessário apenas algumas chamadas de método para reproduzir arquivos de vídeo do Windows Media Audio ou Windows Media.</span><span class="sxs-lookup"><span data-stu-id="e0eaf-120">With DirectShow streaming architecture, it takes only a few method calls to play Windows Media Audio or Windows Media Video files.</span></span> <span data-ttu-id="e0eaf-121">A criação de arquivos também é simplificada.</span><span class="sxs-lookup"><span data-stu-id="e0eaf-121">Creating files is also simplified.</span></span> <span data-ttu-id="e0eaf-122">Você simplesmente especifica um perfil usando a interface **IConfigAsfWriter** no filtro, e o DirectShow carrega automaticamente os componentes necessários para renderizar ou gravar os fluxos e fornece os mecanismos para transferir e sincronizar o fluxo de dados de mídia.</span><span class="sxs-lookup"><span data-stu-id="e0eaf-122">You simply specify a profile using the **IConfigAsfWriter** interface on the filter, and DirectShow automatically loads the required components for rendering or writing the streams, and provides the mechanisms for transferring and synchronizing the flow of media data.</span></span> <span data-ttu-id="e0eaf-123">O DirectShow é especialmente útil ao converter o conteúdo de formatos variados no formato de mídia do Windows.</span><span class="sxs-lookup"><span data-stu-id="e0eaf-123">DirectShow is especially useful when converting content from varied formats into Windows Media Format.</span></span> <span data-ttu-id="e0eaf-124">Você pode criar gráficos de filtro do DirectShow que decodifiquem uma ampla variedade de tipos de arquivo e compactação e, em seguida, alimentar os fluxos decodificados no filtro de [gravador ASF do WM](wm-asf-writer-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="e0eaf-124">You can create DirectShow filter graphs that decode a wide variety of file and compression types, and then feed the decoded streams into the [WM ASF Writer](wm-asf-writer-filter.md) filter.</span></span> <span data-ttu-id="e0eaf-125">Por comparação, o exemplo de UncompAVItoWMV neste SDK funciona apenas com arquivos AVI não compactados.</span><span class="sxs-lookup"><span data-stu-id="e0eaf-125">By comparison, the UncompAVItoWMV sample in this SDK works only with uncompressed AVI files.</span></span> <span data-ttu-id="e0eaf-126">Fluxos de texto e fluxos de dados arbitrários também podem ser criados e/ou renderizados por meio do DirectShow, mas isso pode exigir que você crie filtros personalizados do DirectShow para processar esses fluxos.</span><span class="sxs-lookup"><span data-stu-id="e0eaf-126">Text streams and arbitrary data streams can also be created and/or rendered through DirectShow, but this might require you to create custom DirectShow filters for processing those streams.</span></span>

## <a name="access-to-hardware"></a><span data-ttu-id="e0eaf-127">Acesso ao hardware</span><span class="sxs-lookup"><span data-stu-id="e0eaf-127">Access to Hardware</span></span>

<span data-ttu-id="e0eaf-128">O DirectShow é a única maneira de o código do aplicativo acessar dispositivos de hardware baseados em Windows Driver Model (WDM), como câmeras de vídeo 1394, sintonizadores de TV e webcams USB.</span><span class="sxs-lookup"><span data-stu-id="e0eaf-128">DirectShow is the only way for application code to access Windows Driver Model (WDM)–based hardware devices such as 1394 DV cameras, TV tuners, and USB webcams.</span></span> <span data-ttu-id="e0eaf-129">Se seu aplicativo precisar capturar dados diretamente de um dispositivo de hardware baseado em WDM e transcodificar para o Windows Media Format, e o SDK do Windows Media Encoder não atender às suas necessidades, o DirectShow será a única alternativa.</span><span class="sxs-lookup"><span data-stu-id="e0eaf-129">If your application must capture data directly from a WDM-based hardware device and transcode it to Windows Media Format, and the Windows Media Encoder SDK does not suit your needs, then DirectShow is the only alternative.</span></span> <span data-ttu-id="e0eaf-130">O DirectShow também pode ser usado para acessar dispositivos herdados com base em vídeo para Windows.</span><span class="sxs-lookup"><span data-stu-id="e0eaf-130">DirectShow can also be used to access legacy devices based on Video for Windows.</span></span>

 

 




