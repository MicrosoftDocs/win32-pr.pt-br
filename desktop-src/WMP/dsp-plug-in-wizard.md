---
title: Assistente de plug-in do DSP
description: Assistente de plug-in do DSP
ms.assetid: 3d1ae5ef-12c4-4db3-815a-2adc73353f20
keywords:
- Plug-ins do Windows Media Player, assistente de plug-in
- plug-ins, assistente de plug-in
- plug-ins de processamento de sinal digital, assistente de plug-in
- Plug-ins do DSP, assistente de plug-in
- Assistente de plug-in
- Visual Studio, assistente de plug-in do DSP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e9a7228056d821d2c2bca258f5c236fe1dce11d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104498679"
---
# <a name="dsp-plug-in-wizard"></a><span data-ttu-id="1f031-109">Assistente de plug-in do DSP</span><span class="sxs-lookup"><span data-stu-id="1f031-109">DSP Plug-in Wizard</span></span>

<span data-ttu-id="1f031-110">O SDK do Windows Media Player fornece um assistente de plug-in que você pode adicionar ao Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="1f031-110">The Windows Media Player SDK provides a plug-in wizard that you can add to Visual Studio.</span></span> <span data-ttu-id="1f031-111">O assistente pode gerar um código de exemplo para uma variedade de plug-ins, incluindo os seguintes tipos de plug-ins do DSP:</span><span class="sxs-lookup"><span data-stu-id="1f031-111">The wizard can generate sample code for a variety of plug-ins, including the following types of DSP plug-ins:</span></span>

-   <span data-ttu-id="1f031-112">Plug-in do DSP de áudio</span><span class="sxs-lookup"><span data-stu-id="1f031-112">Audio DSP plug-in</span></span>
-   <span data-ttu-id="1f031-113">Plug-in do DSP de áudio (modo duplo)</span><span class="sxs-lookup"><span data-stu-id="1f031-113">Audio DSP plug-in (dual mode)</span></span>
-   <span data-ttu-id="1f031-114">Plug-in de DSP de vídeo</span><span class="sxs-lookup"><span data-stu-id="1f031-114">Video DSP plug-in</span></span>
-   <span data-ttu-id="1f031-115">Plug-in de DSP de vídeo (modo dual)</span><span class="sxs-lookup"><span data-stu-id="1f031-115">Video DSP plug-in (dual mode)</span></span>

<span data-ttu-id="1f031-116">Cada um dos dois plug-ins básicos de exemplo, DSP de áudio e DSP de vídeo, funciona como um DMO (objeto de mídia do DirectX).</span><span class="sxs-lookup"><span data-stu-id="1f031-116">Each of the two basic sample plug-ins, Audio DSP and Video DSP, functions as a DirectX Media Object (DMO).</span></span> <span data-ttu-id="1f031-117">Ou seja, cada plug-in de exemplo implementa a interface **IMediaObject** .</span><span class="sxs-lookup"><span data-stu-id="1f031-117">That is, each sample plug-in implements the **IMediaObject** interface.</span></span> <span data-ttu-id="1f031-118">Cada um dos dois plug-ins de exemplo de modo duplo pode funcionar como um DMO ou como uma Media Foundation transformação (MFT).</span><span class="sxs-lookup"><span data-stu-id="1f031-118">Each of the two dual-mode sample plug-ins can function either as a DMO or as a Media Foundation Transform (MFT).</span></span> <span data-ttu-id="1f031-119">Ou seja, cada plug-in de exemplo de modo duplo implementa a interface **IMediaObject** e a interface **IMFTransform** .</span><span class="sxs-lookup"><span data-stu-id="1f031-119">That is, each dual-mode sample plug-in implements both the **IMediaObject** interface and the **IMFTransform** interface.</span></span>

<span data-ttu-id="1f031-120">Você pode compilar, vincular, registrar e testar o código de plug-in de exemplo.</span><span class="sxs-lookup"><span data-stu-id="1f031-120">You can compile, link, register, and test the sample plug-in code.</span></span> <span data-ttu-id="1f031-121">Em seguida, você pode modificar o código de exemplo gerado para criar seu próprio plug-in de DSP.</span><span class="sxs-lookup"><span data-stu-id="1f031-121">Then you can modify the generated sample code to create your own DSP plug-in.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1f031-122">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="1f031-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1f031-123">**Criando um plug-in do DSP**</span><span class="sxs-lookup"><span data-stu-id="1f031-123">**Building a DSP Plug-in**</span></span>](building-a-dsp-plug-in.md)
</dt> <dt>

[<span data-ttu-id="1f031-124">**Visão geral do desenvolvedor de plug-in do DSP**</span><span class="sxs-lookup"><span data-stu-id="1f031-124">**DSP Plug-in Developer Overview**</span></span>](dsp-plug-in-developer-overview.md)
</dt> <dt>

[<span data-ttu-id="1f031-125">**Atualizações para o assistente de plug-in do DSP para Windows Media Player 11**</span><span class="sxs-lookup"><span data-stu-id="1f031-125">**Updates to the DSP Plug-in Wizard for Windows Media Player 11**</span></span>](updates-to-the-dsp-plug-in-wizard-for-windows-media-player-11.md)
</dt> </dl>

 

 




