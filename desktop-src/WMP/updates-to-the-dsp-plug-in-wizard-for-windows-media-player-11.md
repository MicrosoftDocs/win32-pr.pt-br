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
# <a name="updates-to-the-dsp-plug-in-wizard-for-windows-media-player-11"></a>Atualizações para o assistente de plug-in do DSP para Windows Media Player 11

O SDK do Windows Media Player 11 apresenta as seguintes alterações no assistente de plug-in do DSP:

-   Os plug-ins registram o modelo de Threading como "ambos". Isso permite que o plug-in seja executado no pipeline de Media Foundation no Windows Vista. Consulte o arquivo *ProjectName*. rgs.

    -   Os plug-ins do DSP de áudio têm suporte para os dois formatos adicionais a seguir:

    <!-- -->

    -   \_formato Wave \_ IEEE \_ float
    -   \_Formato Wave \_ extensível com SUBformato KSDATAFORMAT \_ subtipo \_ IEEE \_ float.

    Consulte o arquivo *ProjectName*. cpp.

    1.  Os plug-ins de DSP de vídeo têm suporte para o formato de vídeo NV12.
    2.  Plug-ins fazem chamadas adicionais para [IWMPMediaPluginRegistrar:: WMPRegisterPlayerPlugin](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpmediapluginregistrar-wmpregisterplayerplugin) e [IWMPMediaPluginRegistrar:: WMPUnRegisterPlayerPlugin](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpmediapluginregistrar-wmpunregisterplayerplugin) com um novo tipo de plug-in: WMP \_ plugintype \_ DSP \_ OUTOFPROC. Consulte o arquivo *projectnamedll*. cpp do projeto.
    3.  Um projeto adicional em cada solução cria uma DLL de proxy/stub para a interface personalizada de configurações da página de propriedades. Consulte o projeto *projectnamePS* .
    4.  As chamadas para métodos preteridos foram alteradas para usar as versões mais recentes.
    5.  O assistente pode gerar um plug-in de modo duplo que funciona como DMO, implementando **IMediaObject** e como um MFT, implementando **IMFTransform**.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Assistente de plug-in do DSP**](dsp-plug-in-wizard.md)
</dt> </dl>

 

 




