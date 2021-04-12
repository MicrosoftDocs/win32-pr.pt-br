---
title: Interfaces de plug-in do DSP
description: Interfaces de plug-in do DSP
ms.assetid: 4660f928-2e92-468f-9e2b-b411931dfded
keywords:
- Plug-ins do Windows Media Player, interfaces DSP
- Plug-ins do Windows Media Player, interfaces
- plug-ins, interfaces DSP
- plug-ins, interfaces
- plug-ins de processamento de sinal digital, interfaces
- plug-ins de processamento de sinal digital, interface ISpecifyPropertyPage
- Plug-ins do DSP, interfaces
- Plug-ins do DSP, interface ISpecifyPropertyPage
- interfaces, plug-ins do DSP
- ISpecifyPropertyPage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5458ab945b24f8646d986ab7d5d44e12ef3249d
ms.sourcegitcommit: b04e152a7f51618fc174ffa872654623fe088db2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/21/2020
ms.locfileid: "104365733"
---
# <a name="dsp-plug-in-interfaces"></a>Interfaces de plug-in do DSP

As interfaces de plug-in do DSP (processamento de sinal digital) são usadas para gerenciar a transferência de dados entre o Windows Media Player e o plug-in. Todos os plug-ins DSP podem, opcionalmente, implementar a interface **ISpecifyPropertyPage** para fornecer uma implementação de página de propriedades.

As interfaces a seguir são necessárias para a criação de plug-ins DSP.



| Interface                                                | Descrição                                                                                                                                            |
|----------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| **IMediaObject**                                         | Gerencia a troca de dados com o Windows Media Player e executa tarefas de processamento de sinal digital. A documentação detalhada está incluída no SDK do DirectX. |
| [IWMPMediaPluginRegistrar](/previous-versions/windows/desktop/api/wmpservices/nn-wmpservices-iwmpmediapluginregistrar) | Gerencia o registro de plug-in.                                                                                                                          |
| [IWMPPlugin](/previous-versions/windows/desktop/api/wmpservices/nn-wmpservices-iwmpplugin)                             | Gerencia a conexão com o Windows Media Player.                                                                                                        |
| [IWMPPluginEnable](/previous-versions/windows/desktop/api/wmpservices/nn-wmpservices-iwmppluginenable)                 | Armazena se o plug-in está habilitado no momento pelo Windows Media Player.                                                                               |
| [IWMPServices](/previous-versions/windows/desktop/api/wmpservices/nn-wmpservices-iwmpservices)                         | Recupera informações do Player sobre a hora e o estado do fluxo atuais.                                                                  |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Referência de programação de plug-ins do DSP**](dsp-plug-ins-programming-reference.md)
</dt> </dl>

 

 




