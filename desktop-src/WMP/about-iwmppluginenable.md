---
title: Sobre o IWMPPluginEnable
description: Sobre o IWMPPluginEnable
ms.assetid: 7611a197-f404-4cfb-88b0-05348a41ac42
keywords:
- Plug-ins do Windows Media Player, interfaces
- plug-ins, interfaces
- plug-ins de processamento de sinal digital, interfaces
- Plug-ins do DSP, interfaces
- interfaces, plug-ins do DSP
- Plug-ins do Windows Media Player, interface IWMPPluginEnable
- plug-ins, interface IWMPPluginEnable
- plug-ins de processamento de sinal digital, interface IWMPPluginEnable
- Plug-ins do DSP, interface IWMPPluginEnable
- Interface IWMPPluginEnable
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce7bf0f58be1d2623539cc5ac1329838246c8697
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103915997"
---
# <a name="about-iwmppluginenable"></a><span data-ttu-id="29ad0-113">Sobre o IWMPPluginEnable</span><span class="sxs-lookup"><span data-stu-id="29ad0-113">About IWMPPluginEnable</span></span>

<span data-ttu-id="29ad0-114">A interface **IWMPPluginEnable** é necessária para plug-ins do DSP do Windows Media Player. **IWMPPluginEnable** contém dois métodos que armazenam se o Windows Media Player habilitou o plug-in DSP.</span><span class="sxs-lookup"><span data-stu-id="29ad0-114">The **IWMPPluginEnable** interface is required for Windows Media Player DSP plug-ins. **IWMPPluginEnable** contains two methods that store whether Windows Media Player has enabled the DSP plug-in.</span></span> <span data-ttu-id="29ad0-115">O Windows Media Player chama **IWMPPluginEnable:: SetEnable** quando cria uma instância do plug-in do DSP, passando um valor **true** se tiver habilitado o plug-in ou **false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="29ad0-115">Windows Media Player calls **IWMPPluginEnable::SetEnable** when it creates an instance of the DSP plug-in, passing a value of **TRUE** if it has enabled the plug-in or **FALSE** otherwise.</span></span>

<span data-ttu-id="29ad0-116">Plug-ins do DSP podem permanecer carregados mesmo quando o usuário optar por desabilitá-los.</span><span class="sxs-lookup"><span data-stu-id="29ad0-116">DSP plug-ins may remain loaded even when the user chooses to disable them.</span></span> <span data-ttu-id="29ad0-117">Quando desabilitado, um plug-in deve copiar dados do buffer de entrada para o buffer de saída, executando somente o processamento de conversão de formato, se aplicável.</span><span class="sxs-lookup"><span data-stu-id="29ad0-117">When disabled, a plug-in must copy data from the input buffer to the output buffer, performing only format conversion processing, if applicable.</span></span>

<span data-ttu-id="29ad0-118">O Windows Media Player também chama esse método antes de liberar uma instância do plug-in do DSP.</span><span class="sxs-lookup"><span data-stu-id="29ad0-118">Windows Media Player also calls this method before it releases an instance of the DSP plug-in.</span></span> <span data-ttu-id="29ad0-119">Isso é útil para permitir que clientes do plug-in verifiquem se o plug-in está habilitado no momento.</span><span class="sxs-lookup"><span data-stu-id="29ad0-119">This is useful to allow clients of the plug-in to check whether the plug-in is currently enabled.</span></span> <span data-ttu-id="29ad0-120">Por exemplo, um plug-in de interface do usuário pode alterar a aparência de seus controles para alertar o usuário de que o plug-in do DSP não está conectado.</span><span class="sxs-lookup"><span data-stu-id="29ad0-120">For instance, a user interface plug-in might change the appearance of its controls to alert the user that the DSP plug-in is not connected.</span></span>

## <a name="related-topics"></a><span data-ttu-id="29ad0-121">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="29ad0-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="29ad0-122">**Interfaces necessárias**</span><span class="sxs-lookup"><span data-stu-id="29ad0-122">**Required Interfaces**</span></span>](required-interfaces.md)
</dt> </dl>

 

 




