---
title: DSP Plug-in Interfaces
description: DSP Plug-in Interfaces
ms.assetid: 4660f928-2e92-468f-9e2b-b411931dfded
keywords:
- Windows Media Player plug-ins, interfaces DSP
- Windows Media Player plug-ins, interfaces
- plug-ins, interfaces DSP
- plug-ins, interfaces
- plug-ins de processamento de sinal digital, interfaces
- plug-ins de processamento de sinal digital, interface ISpecifyPropertyPage
- Plug-ins do DSP, interfaces
- Plug-ins DSP, interface ISpecifyPropertyPage
- interfaces, plug-ins DSP
- ISpecifyPropertyPage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3bd030b09377adfe965698d6c411f1a39a745979f2db2eae9f0c613cad843d2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119863366"
---
# <a name="dsp-plug-in-interfaces"></a>DSP Plug-in Interfaces

As interfaces de plug-in do DSP (processamento de sinal digital) são usadas para gerenciar a transferência de dados entre Windows Media Player e o plug-in. Todos os plug-ins DSP podem, opcionalmente, implementar a interface **ISpecifyPropertyPage** para fornecer uma implementação de página de propriedade.

As interfaces a seguir são necessárias para criar plug-ins DSP.



| Interface                                                | Descrição                                                                                                                                            |
|----------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Imediaobject**                                         | Gerencia a troca de dados com Windows Media Player e executa tarefas de processamento de sinal digital. A documentação detalhada está incluída no SDK do DirectX. |
| [IWMPMediaPluginRegistrar](/previous-versions/windows/desktop/api/wmpservices/nn-wmpservices-iwmpmediapluginregistrar) | Gerencia o registro de plug-in.                                                                                                                          |
| [IWMPPlugin](/previous-versions/windows/desktop/api/wmpservices/nn-wmpservices-iwmpplugin)                             | Gerencia a conexão com Windows Media Player.                                                                                                        |
| [IWMPPluginEnable](/previous-versions/windows/desktop/api/wmpservices/nn-wmpservices-iwmppluginenable)                 | Armazena se o plug-in está habilitado no momento por Windows Media Player.                                                                               |
| [IWMPServices](/previous-versions/windows/desktop/api/wmpservices/nn-wmpservices-iwmpservices)                         | Recupera informações do Player sobre a hora do fluxo atual e o estado do fluxo.                                                                  |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Referência de programação de plug-ins DSP**](dsp-plug-ins-programming-reference.md)
</dt> </dl>

 

 




