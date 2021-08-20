---
title: Conectando-se ao Windows Media Player
description: Conectando-se ao Windows Media Player
ms.assetid: c6afbd95-bcf8-438a-b854-776c543a5d51
keywords:
- plug-ins Windows Media Player, entradas do registro
- plug-ins, entradas do registro
- plug-ins Windows Media Player, conectando
- plug-ins, conectando
- plug-ins de processamento de sinal digital, conectando
- Plug-ins do DSP, conectando
- plug-ins de processamento de sinal digital, entradas de registro
- Plug-ins do DSP, entradas do registro
- registro, plug-ins do DSP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4d266f1715147d3c7631909e8e23e3e7b1f786337c998d188968a96f6c26b62
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118997626"
---
# <a name="connecting-to-windows-media-player"></a>Conectando-se ao Windows Media Player

Windows Media Player se conecta automaticamente aos plug-ins do DSP que foram instalados e corretamente registrados. plug-ins DSP devem chamar [IWMPMediaPluginRegistrar:: WMPRegisterPlayerPlugin](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpmediapluginregistrar-wmpregisterplayerplugin) para criar as entradas de registro necessárias para permitir que Windows Media Player reconheçam o plug-in e liste-os na guia **plug-ins** da caixa de diálogo opções. Para remover as entradas de registro criadas por **IWMPMediaPluginRegistrar:: WMPRegisterPlayerPlugin**, o plug-in chama [IWMPMediaPluginRegistrar:: WMPUnRegisterPlayerPlugin](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpmediapluginregistrar-wmpunregisterplayerplugin).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Visão geral do desenvolvedor de plug-in do DSP**](dsp-plug-in-developer-overview.md)
</dt> </dl>

 

 




