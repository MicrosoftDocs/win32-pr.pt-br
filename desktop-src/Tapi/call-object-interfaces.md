---
description: O objeto de chamada é criado quando uma chamada entra em existência. As interfaces associadas obtêm e definem informações relativas à chamada.
ms.assetid: cff131c0-9f4a-418d-b486-155bd71e9316
title: Interfaces de objeto de chamada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57ccb7fb9ed07fad8bd952aff806d39aa2db5e70
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103921831"
---
# <a name="call-object-interfaces"></a>Interfaces de objeto de chamada

O [objeto de chamada](call-object.md) é criado quando uma chamada entra em existência. As interfaces associadas obtêm e definem informações relativas à chamada.

As interfaces de evento e enumerador não são diretamente expostas no objeto de chamada, mas são listadas aqui para conveniência de referência.

As interfaces [**ITCallNotificationEvent**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallnotificationevent), [**ITCallInfoChangeEvent**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfochangeevent), [**ITCallStateEvent**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallstateevent), [**ITCallMediaEvent**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallmediaevent)e [**IEnumTerminalClass**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumterminalclass) não são diretamente expostas no objeto de chamada, mas estão intimamente relacionadas a ela e estão listadas aqui para conveniência de referência.



| Interface                                                      | Descrição                                                                                                                  |
|----------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| [**ITCallInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo)                               | Fornece informações sobre um objeto de chamada, como estado de chamada ou terminais em uso.                                       |
| [**ITCallInfo2**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo2)                             | Estende o [**ITCallInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo) fornecendo métodos para definir a filtragem de eventos em uma base por chamada.                    |
| [**ITBasicCallControl**](/windows/desktop/api/tapi3if/nn-tapi3if-itbasiccallcontrol)               | Usado para conectar, responder e executar operações básicas de telefonia em um objeto de chamada.                                            |
| [**ITBasicCallControl2**](/windows/desktop/api/tapi3if/nn-tapi3if-itbasiccallcontrol2)             | Estende o [**ITBasicCallControl**](/windows/desktop/api/tapi3if/nn-tapi3if-itbasiccallcontrol) fornecendo métodos para selecionar um terminal em uma chamada.              |
| [**ITCallNotificationEvent**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallnotificationevent)     | Interface de notificação para [**ITCallInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo).                                                                 |
| [**ITCallInfoChangeEvent**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfochangeevent)         | Interface de notificação para alterações nas informações de chamada.                                                                      |
| [**ITCallStateEvent**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallstateevent)                   | Obtém informações relacionadas a um evento de chamada.                                                                                    |
| [**ITCallMediaEvent**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallmediaevent)                   | Obtém informações relacionadas a um evento de mídia de chamada.                                                                              |
| [**ITCustomTone**](/windows/desktop/api/Tapi3if/nn-tapi3if-itcustomtone)                           | Fornece métodos para controlar os tons personalizados possíveis com alguns conjuntos de telefone.                                                  |
| [**ITDetectTone**](/windows/desktop/api/Tapi3if/nn-tapi3if-itdetecttone)                           | Fornece métodos para especificar as características de tons e tons que geram eventos de Tom.                                    |
| [**ITLegacyCallMediaControl**](/windows/desktop/api/tapi3if/nn-tapi3if-itlegacycallmediacontrol)   | Dá suporte a aplicativos herdados que devem se comunicar diretamente com um dispositivo.                                                   |
| [**ITLegacyCallMediaControl2**](/windows/desktop/api/Tapi3if/nn-tapi3if-itlegacycallmediacontrol2) | Estende o [**ITLegacyCallMediaControl**](/windows/desktop/api/tapi3if/nn-tapi3if-itlegacycallmediacontrol) fornecendo métodos para detecção e geração de Tom. |
| [**IEnumCall**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumcall)                                 | Enumera [**ITCallInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo).                                                                                 |



 

 

 



