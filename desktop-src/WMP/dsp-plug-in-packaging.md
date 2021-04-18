---
title: Empacotamento de plug-in do DSP
description: Empacotamento de plug-in do DSP
ms.assetid: 5d40a39b-0fe8-4f77-9465-8e31d1f2708e
keywords:
- Plug-ins do Windows Media Player, Media Foundation pipeline
- plug-ins, pipeline de Media Foundation
- plug-ins de processamento de sinal digital, Media Foundation pipeline
- Plug-ins do DSP, pipeline de Media Foundation
- Pipeline de Media Foundation
- Plug-ins do Windows Media Player, pipeline do DirectShow
- plug-ins, pipeline do DirectShow
- plug-ins de processamento de sinal digital, pipeline do DirectShow
- Plug-ins do DSP, pipeline do DirectShow
- Pipeline do DirectShow
- plug-ins de processamento de sinal digital, básico
- Plug-ins do DSP, básico
- Plug-ins do Windows Media Player, DSP básico
- plug-ins, DSP básico
- plug-ins básicos do DSP
- Plug-ins do Windows Media Player, DSP de modo duplo
- plug-ins, DSP de modo duplo
- plug-ins de processamento de sinal digital, modo duplo
- Plug-ins do DSP, modo duplo
- plug-ins DSP de modo duplo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62535abe0d82975bf07fef178ac43cf066c6afbd
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105811337"
---
# <a name="dsp-plug-in-packaging"></a><span data-ttu-id="8b98d-123">Empacotamento de plug-in do DSP</span><span class="sxs-lookup"><span data-stu-id="8b98d-123">DSP Plug-in Packaging</span></span>

<span data-ttu-id="8b98d-124">O Windows Media Player renderiza áudio e vídeo usando um dos pipelines a seguir.</span><span class="sxs-lookup"><span data-stu-id="8b98d-124">Windows Media Player renders audio and video by using one of the following pipelines.</span></span>

-   <span data-ttu-id="8b98d-125">DirectShow</span><span class="sxs-lookup"><span data-stu-id="8b98d-125">DirectShow</span></span>
-   <span data-ttu-id="8b98d-126">Media Foundation</span><span class="sxs-lookup"><span data-stu-id="8b98d-126">Media Foundation</span></span>

<span data-ttu-id="8b98d-127">No Microsoft Windows XP e versões anteriores, o Player usa o DirectShow.</span><span class="sxs-lookup"><span data-stu-id="8b98d-127">In Microsoft Windows XP and earlier, the Player uses DirectShow.</span></span> <span data-ttu-id="8b98d-128">No Windows Vista, às vezes o Player usa o DirectShow e, às vezes, usa Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="8b98d-128">In Windows Vista, the Player sometimes uses DirectShow and sometimes uses Media Foundation.</span></span>

<span data-ttu-id="8b98d-129">Um plug-in do DSP projetado para ser executado no pipeline do DirectShow é chamado de *plug-in básico do DSP*.</span><span class="sxs-lookup"><span data-stu-id="8b98d-129">A DSP plug-in that is designed to run in the DirectShow pipeline is called a *basic DSP plug-in*.</span></span> <span data-ttu-id="8b98d-130">Os plug-ins básicos do DSP atuam como um DMO (objeto de mídia do DirectX).</span><span class="sxs-lookup"><span data-stu-id="8b98d-130">A basic DSP plug-ins acts as a DirectX Media Object (DMO).</span></span> <span data-ttu-id="8b98d-131">Um plug-in de DSP básico pode ser executado nativamente no pipeline do DirectShow e também pode ser executado no pipeline de Media Foundation dentro de um wrapper fornecido pelo Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="8b98d-131">A basic DSP plug-in can run natively in the DirectShow pipeline and can also run in the Media Foundation pipeline inside a wrapper provided by Media Foundation.</span></span>

<span data-ttu-id="8b98d-132">Um plug-in do DSP projetado para ser executado nativamente (nenhum wrapper necessário) nos pipelines do DirectShow e do Media Foundation é chamado de *plug-in de DSP de modo duplo*.</span><span class="sxs-lookup"><span data-stu-id="8b98d-132">A DSP plug-in that is designed to run natively (no wrapper required) in both the DirectShow and Media Foundation pipelines is called a *dual-mode DSP plug-in*.</span></span> <span data-ttu-id="8b98d-133">Um plug-in DSP de modo duplo pode atuar como um DMO ou como uma Media Foundation transformação (MFT).</span><span class="sxs-lookup"><span data-stu-id="8b98d-133">A dual-mode DSP plug-in can act as a DMO or as a Media Foundation Transform (MFT).</span></span>

<span data-ttu-id="8b98d-134">Um plug-in do DSP é um objeto COM que é empacotado como um arquivo. dll de registro automático.</span><span class="sxs-lookup"><span data-stu-id="8b98d-134">A DSP plug-in is a COM object that is packaged as a self-registering .dll file.</span></span> <span data-ttu-id="8b98d-135">As interfaces que o plug-in implementa dependem se o plug-in foi projetado como um plug-in de DSP básico ou como um plug-in de DSP de modo duplo.</span><span class="sxs-lookup"><span data-stu-id="8b98d-135">The interfaces that the plug-in implements depend on whether the plug-in is designed as a basic DSP plug-in or as a dual-mode DSP plug-in.</span></span> <span data-ttu-id="8b98d-136">Para obter informações detalhadas sobre as interfaces que os plug-ins do DSP devem implementar, consulte [interfaces necessárias](required-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="8b98d-136">For detailed information about the interfaces that DSP plug-ins must implement, see [Required Interfaces](required-interfaces.md).</span></span>

<span data-ttu-id="8b98d-137">Um plug-in DSP executado no pipeline de Media Foundation (nativamente ou encapsulado) deve registrar seu modelo de Threading como "ambos".</span><span class="sxs-lookup"><span data-stu-id="8b98d-137">A DSP plug-in that runs in the Media Foundation pipeline (either natively or wrapped) must register its threading model as "Both".</span></span> <span data-ttu-id="8b98d-138">Para obter informações detalhadas sobre as subchaves do registro e as entradas associadas aos plug-ins do DSP, consulte [registrando plug-ins do DSP](registering-dsp-plug-ins.md).</span><span class="sxs-lookup"><span data-stu-id="8b98d-138">For detailed information about registry subkeys and entries associated with DSP plug-ins, see [Registering DSP Plug-ins](registering-dsp-plug-ins.md).</span></span>

<span data-ttu-id="8b98d-139">Um plug-in de DSP que implementa interfaces personalizadas e execuções no pipeline de Media Foundation (nativamente ou encapsulado) deve ser emparelhado com um arquivo de stub de proxy. dll que pode realizar marshaling das interfaces personalizadas entre limites de processo.</span><span class="sxs-lookup"><span data-stu-id="8b98d-139">A DSP plug-in that implements custom interfaces and runs in the Media Foundation pipeline (either natively or wrapped) must be paired with a proxy-stub .dll file that can marshal the custom interfaces across process boundaries.</span></span> <span data-ttu-id="8b98d-140">Para obter informações sobre o componente de stub de proxy, consulte [atualizando plug-ins de DSP existentes](updating-existing-dsp-plug-ins.md) e [atualizações para o assistente de plug-in do DSP para Windows Media Player 11](updates-to-the-dsp-plug-in-wizard-for-windows-media-player-11.md).</span><span class="sxs-lookup"><span data-stu-id="8b98d-140">For information about the proxy-stub component, see [Updating Existing DSP Plug-ins](updating-existing-dsp-plug-ins.md) and [Updates to the DSP Plug-in Wizard for Windows Media Player 11](updates-to-the-dsp-plug-in-wizard-for-windows-media-player-11.md).</span></span>

<span data-ttu-id="8b98d-141">Os objetos de plug-in do DSP não devem ser criados como singletons.</span><span class="sxs-lookup"><span data-stu-id="8b98d-141">DSP plug-in objects must not be created as singletons.</span></span> <span data-ttu-id="8b98d-142">O Windows Media Player deve ser capaz de criar várias instâncias separadas de um plug-in de DSP específico.</span><span class="sxs-lookup"><span data-stu-id="8b98d-142">Windows Media Player must be able to create multiple separate instances of a particular DSP plug-in.</span></span>

<span data-ttu-id="8b98d-143">Plug-ins DSP executados no caminho de mídia protegida do Windows Vista (PMP) devem ser assinados.</span><span class="sxs-lookup"><span data-stu-id="8b98d-143">DSP plug-ins that run in the Windows Vista Protected Media Path (PMP) must be signed.</span></span> <span data-ttu-id="8b98d-144">Para obter mais informações, consulte [assinatura de código para componentes de mídia protegidos no Windows Vista](/windows-hardware/test/hlk/).</span><span class="sxs-lookup"><span data-stu-id="8b98d-144">For more information, see [Code Signing for Protected Media Components in Windows Vista](/windows-hardware/test/hlk/).</span></span>

## <a name="related-topics"></a><span data-ttu-id="8b98d-145">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="8b98d-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8b98d-146">**Visão geral do desenvolvedor de plug-in do DSP**</span><span class="sxs-lookup"><span data-stu-id="8b98d-146">**DSP Plug-in Developer Overview**</span></span>](dsp-plug-in-developer-overview.md)
</dt> </dl>

 

 