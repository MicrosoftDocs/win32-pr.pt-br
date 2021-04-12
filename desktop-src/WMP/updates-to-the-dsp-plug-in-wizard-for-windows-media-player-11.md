---
title: Atualizações para o assistente de plug-in do DSP para Windows Media Player 11
description: Atualizações para o assistente de plug-in do DSP para Windows Media Player 11
ms.assetid: 975c18d5-06d7-4db2-a558-bc6557963425
keywords:
- Plug-ins do Windows Media Player, assistente de plug-in
- plug-ins, assistente de plug-in
- plug-ins de processamento de sinal digital, assistente de plug-in
- Plug-ins do DSP, assistente de plug-in
- Assistente de plug-in
- Visual Studio, assistente de plug-in do DSP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a8efe798a3c324f9ecfac0a5b6021db4ea5abdf
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104365572"
---
# <a name="updates-to-the-dsp-plug-in-wizard-for-windows-media-player-11"></a><span data-ttu-id="5fe04-109">Atualizações para o assistente de plug-in do DSP para Windows Media Player 11</span><span class="sxs-lookup"><span data-stu-id="5fe04-109">Updates to the DSP Plug-in Wizard for Windows Media Player 11</span></span>

<span data-ttu-id="5fe04-110">O SDK do Windows Media Player 11 apresenta as seguintes alterações no assistente de plug-in do DSP:</span><span class="sxs-lookup"><span data-stu-id="5fe04-110">The Windows Media Player 11 SDK introduces the following changes to the DSP plug-in wizard:</span></span>

-   <span data-ttu-id="5fe04-111">Os plug-ins registram o modelo de Threading como "ambos".</span><span class="sxs-lookup"><span data-stu-id="5fe04-111">Plug-ins register the threading model as "Both".</span></span> <span data-ttu-id="5fe04-112">Isso permite que o plug-in seja executado no pipeline de Media Foundation no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="5fe04-112">This enables the plug-in to run in the Media Foundation pipeline on Windows Vista.</span></span> <span data-ttu-id="5fe04-113">Consulte o arquivo *ProjectName*. rgs.</span><span class="sxs-lookup"><span data-stu-id="5fe04-113">See the *projectname*.rgs file.</span></span>

    -   <span data-ttu-id="5fe04-114">Os plug-ins do DSP de áudio têm suporte para os dois formatos adicionais a seguir:</span><span class="sxs-lookup"><span data-stu-id="5fe04-114">Audio DSP plug-ins have support for the following two additional formats:</span></span>

    <!-- -->

    -   <span data-ttu-id="5fe04-115">\_formato Wave \_ IEEE \_ float</span><span class="sxs-lookup"><span data-stu-id="5fe04-115">WAVE\_FORMAT\_IEEE\_FLOAT</span></span>
    -   <span data-ttu-id="5fe04-116">\_Formato Wave \_ extensível com SUBformato KSDATAFORMAT \_ subtipo \_ IEEE \_ float.</span><span class="sxs-lookup"><span data-stu-id="5fe04-116">WAVE\_FORMAT\_EXTENSIBLE with subformat KSDATAFORMAT\_SUBTYPE\_IEEE\_FLOAT.</span></span>

    <span data-ttu-id="5fe04-117">Consulte o arquivo *ProjectName*. cpp.</span><span class="sxs-lookup"><span data-stu-id="5fe04-117">See the *projectname*.cpp file.</span></span>

    1.  <span data-ttu-id="5fe04-118">Os plug-ins de DSP de vídeo têm suporte para o formato de vídeo NV12.</span><span class="sxs-lookup"><span data-stu-id="5fe04-118">Video DSP plug-ins have support for the NV12 video format.</span></span>
    2.  <span data-ttu-id="5fe04-119">Plug-ins fazem chamadas adicionais para [IWMPMediaPluginRegistrar:: WMPRegisterPlayerPlugin](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpmediapluginregistrar-wmpregisterplayerplugin) e [IWMPMediaPluginRegistrar:: WMPUnRegisterPlayerPlugin](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpmediapluginregistrar-wmpunregisterplayerplugin) com um novo tipo de plug-in: WMP \_ plugintype \_ DSP \_ OUTOFPROC.</span><span class="sxs-lookup"><span data-stu-id="5fe04-119">Plug-ins make additional calls to [IWMPMediaPluginRegistrar::WMPRegisterPlayerPlugin](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpmediapluginregistrar-wmpregisterplayerplugin) and [IWMPMediaPluginRegistrar::WMPUnRegisterPlayerPlugin](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpmediapluginregistrar-wmpunregisterplayerplugin) with a new plug-in type: WMP\_PLUGINTYPE\_DSP\_OUTOFPROC.</span></span> <span data-ttu-id="5fe04-120">Consulte o arquivo *projectnamedll*. cpp do projeto.</span><span class="sxs-lookup"><span data-stu-id="5fe04-120">See the project's *projectnamedll*.cpp file.</span></span>
    3.  <span data-ttu-id="5fe04-121">Um projeto adicional em cada solução cria uma DLL de proxy/stub para a interface personalizada de configurações da página de propriedades.</span><span class="sxs-lookup"><span data-stu-id="5fe04-121">An additional project in each solution creates a proxy/stub DLL for the property page settings custom interface.</span></span> <span data-ttu-id="5fe04-122">Consulte o projeto *projectnamePS* .</span><span class="sxs-lookup"><span data-stu-id="5fe04-122">See the *projectnamePS* project.</span></span>
    4.  <span data-ttu-id="5fe04-123">As chamadas para métodos preteridos foram alteradas para usar as versões mais recentes.</span><span class="sxs-lookup"><span data-stu-id="5fe04-123">Calls to deprecated methods have been changed to use the newest versions.</span></span>
    5.  <span data-ttu-id="5fe04-124">O assistente pode gerar um plug-in de modo duplo que funciona como DMO, implementando **IMediaObject** e como um MFT, implementando **IMFTransform**.</span><span class="sxs-lookup"><span data-stu-id="5fe04-124">The wizard can generate a dual-mode plug-in that functions both as a DMO, by implementing **IMediaObject**, and as an MFT, by implementing **IMFTransform**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5fe04-125">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="5fe04-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5fe04-126">**Assistente de plug-in do DSP**</span><span class="sxs-lookup"><span data-stu-id="5fe04-126">**DSP Plug-in Wizard**</span></span>](dsp-plug-in-wizard.md)
</dt> </dl>

 

 




