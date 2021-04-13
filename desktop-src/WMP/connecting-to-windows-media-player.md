---
title: Conectando ao Windows Media Player
description: Conectando ao Windows Media Player
ms.assetid: c6afbd95-bcf8-438a-b854-776c543a5d51
keywords:
- Plug-ins do Windows Media Player, entradas do registro
- plug-ins, entradas do registro
- Plug-ins do Windows Media Player, conectando
- plug-ins, conectando
- plug-ins de processamento de sinal digital, conectando
- Plug-ins do DSP, conectando
- plug-ins de processamento de sinal digital, entradas de registro
- Plug-ins do DSP, entradas do registro
- registro, plug-ins do DSP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8fa0851e271631e2c37bf716c427b5af34ade14
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104365532"
---
# <a name="connecting-to-windows-media-player"></a><span data-ttu-id="ccbdc-112">Conectando ao Windows Media Player</span><span class="sxs-lookup"><span data-stu-id="ccbdc-112">Connecting to Windows Media Player</span></span>

<span data-ttu-id="ccbdc-113">O Windows Media Player se conecta automaticamente aos plug-ins do DSP que foram instalados e corretamente registrados.</span><span class="sxs-lookup"><span data-stu-id="ccbdc-113">Windows Media Player automatically connects to DSP plug-ins that have been installed and properly registered.</span></span> <span data-ttu-id="ccbdc-114">Plug-ins DSP devem chamar [IWMPMediaPluginRegistrar:: WMPRegisterPlayerPlugin](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpmediapluginregistrar-wmpregisterplayerplugin) para criar as entradas de Registro necessárias para permitir que o Windows Media Player reconheça o plug-in e o liste na guia **plug-ins** da caixa de diálogo opções.</span><span class="sxs-lookup"><span data-stu-id="ccbdc-114">DSP plug-ins must call [IWMPMediaPluginRegistrar::WMPRegisterPlayerPlugin](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpmediapluginregistrar-wmpregisterplayerplugin) to create the registry entries necessary to allow Windows Media Player to recognize the plug-in and to list it on the **Plug-ins** tab of the Options dialog box.</span></span> <span data-ttu-id="ccbdc-115">Para remover as entradas de registro criadas por **IWMPMediaPluginRegistrar:: WMPRegisterPlayerPlugin**, o plug-in chama [IWMPMediaPluginRegistrar:: WMPUnRegisterPlayerPlugin](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpmediapluginregistrar-wmpunregisterplayerplugin).</span><span class="sxs-lookup"><span data-stu-id="ccbdc-115">To remove the registry entries created by **IWMPMediaPluginRegistrar::WMPRegisterPlayerPlugin**, the plug-in calls [IWMPMediaPluginRegistrar::WMPUnRegisterPlayerPlugin](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpmediapluginregistrar-wmpunregisterplayerplugin).</span></span>

## <a name="related-topics"></a><span data-ttu-id="ccbdc-116">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ccbdc-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ccbdc-117">**Visão geral do desenvolvedor de plug-in do DSP**</span><span class="sxs-lookup"><span data-stu-id="ccbdc-117">**DSP Plug-in Developer Overview**</span></span>](dsp-plug-in-developer-overview.md)
</dt> </dl>

 

 




