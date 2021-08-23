---
title: Atualizações para o Assistente de Plug-in do DSP para Windows Media Player 11
description: Atualizações para o Assistente de Plug-in do DSP para Windows Media Player 11
ms.assetid: 975c18d5-06d7-4db2-a558-bc6557963425
keywords:
- Windows Media Player plug-ins, assistente de plug-in
- plug-ins, assistente de plug-in
- plug-ins de processamento de sinal digital, assistente de plug-in
- Plug-ins do DSP, assistente de plug-in
- assistente de plug-in
- Visual Studio,assistente de plug-in DSP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2fb6ffaa9384f46e4630b16310a599de8508d953aabd4a5cdf277e91c130641
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119762166"
---
# <a name="updates-to-the-dsp-plug-in-wizard-for-windows-media-player-11"></a>Atualizações para o Assistente de Plug-in do DSP para Windows Media Player 11

O Windows Media Player SDK 11 apresenta as seguintes alterações ao assistente de plug-in DSP:

-   Os plug-ins registram o modelo de threading como "Ambos". Isso permite que o plug-in seja executado no pipeline Media Foundation no Windows Vista. Consulte o arquivo .rgs *projectname.*

    -   Os plug-ins DSP de áudio têm suporte para os dois formatos adicionais a seguir:

    <!-- -->

    -   WAVE \_ FORMAT \_ IEEE \_ FLOAT
    -   WAVE \_ FORMAT \_ EXTENSIBLE with subformat KSDATAFORMAT \_ SUBTYPE \_ IEEE \_ FLOAT.

    Consulte o arquivo .cpp *projectname.*

    1.  Os plug-ins DSP de vídeo têm suporte para o formato de vídeo NV12.
    2.  Os plug-ins fazem chamadas adicionais para [IWMPMediaPluginRegistrar::WMPRegisterPlayerPlugin](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpmediapluginregistrar-wmpregisterplayerplugin) e [IWMPMediaPluginRegistrar::WMPUnRegisterPlayerPlugin](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpmediapluginregistrar-wmpunregisterplayerplugin) com um novo tipo de plug-in: WMP \_ PLUGINTYPE \_ DSP \_ OUTOFPROC. Consulte o arquivo *.cpp projectnamedll* do projeto.
    3.  Um projeto adicional em cada solução cria uma DLL de proxy/stub para a interface personalizada de configurações da página de propriedades. Consulte o *projeto projectnamePS.*
    4.  As chamadas para métodos preteridas foram alteradas para usar as versões mais recentes.
    5.  O assistente pode gerar um plug-in de modo duplo que funciona como um DMO, implementando **IMediaObject** e como um MFT, implementando **IMFTransform**.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Assistente de Plug-in do DSP**](dsp-plug-in-wizard.md)
</dt> </dl>

 

 




