---
title: O que há de novo nas APIs UPnP
description: As APIs de™ UPnP têm novos recursos e a documentação atualizada do Windows XP SP2. A tabela a seguir identifica a nova documentação.
ms.assetid: ad72d9b8-6db4-4b9b-9b10-ae3980521d7e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e27747c6185b5aecea86e240d388ab10410aa29f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103637185"
---
# <a name="whats-new-in-the-upnp-apis"></a>O que há de novo nas APIs UPnP

As APIs de™ UPnP têm novos recursos e a documentação atualizada do Windows XP SP2. A tabela a seguir identifica a nova documentação.



| Recurso                                                          | Descrição                                                                                                                                                                                                                                                                                                                                                                   |
|------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IUPnPRemoteEndpointInfo**](/windows/desktop/api/Upnphost/nn-upnphost-iupnpremoteendpointinfo)       | Essa nova interface permite que um dispositivo hospedado Obtenha informações sobre um solicitante (isto é, um ponto de controle) e a solicitação. Ele inclui três métodos, cada um dos quais fornece um tipo diferente de informações.                                                                                                                                                              |
| [Implementando o comportamento do dispositivo](implementing-device-behavior.md) | Este tópico inclui uma nova seção que explica como obter informações de ponto de extremidade usando a nova interface [**IUPnPRemoteEndpointInfo**](/windows/desktop/api/Upnphost/nn-upnphost-iupnpremoteendpointinfo) .                                                                                                                                                                                                     |
| [Definições de configuração](configuration-settings.md)             | Este novo tópico fornece informações sobre as configurações do registro que afetam o comportamento das APIs de UPnP.                                                                                                                                                                                                                                                                    |
| [Códigos de erro do dispositivo](device-error-codes.md)                     | Este novo tópico explica como um código de erro de um dispositivo é convertido em um valor HRESULT e vice-versa. Uma compreensão desse processo é necessária para avaliar um valor HRESULT que é retornado pelos métodos [**IUPnPService:: InvokeAction**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-invokeaction) e [**IUPnPService:: QueryStateVariable**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-querystatevariable) . |



 

 

 




