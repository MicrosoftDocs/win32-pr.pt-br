---
title: O que há de novo nas APIs UPnP
description: as APIs de™ UPnP têm novos recursos e documentação atualizada para o Windows XP SP2. A tabela a seguir identifica a nova documentação.
ms.assetid: ad72d9b8-6db4-4b9b-9b10-ae3980521d7e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a68ab872eab498e80ec8d30f996f839c73432875d02ec8d32060595ce8d6482b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119057994"
---
# <a name="whats-new-in-the-upnp-apis"></a>O que há de novo nas APIs UPnP

as APIs de™ UPnP têm novos recursos e documentação atualizada para o Windows XP SP2. A tabela a seguir identifica a nova documentação.



| Recurso                                                          | Descrição                                                                                                                                                                                                                                                                                                                                                                   |
|------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IUPnPRemoteEndpointInfo**](/windows/desktop/api/Upnphost/nn-upnphost-iupnpremoteendpointinfo)       | Essa nova interface permite que um dispositivo hospedado Obtenha informações sobre um solicitante (isto é, um ponto de controle) e a solicitação. Ele inclui três métodos, cada um dos quais fornece um tipo diferente de informações.                                                                                                                                                              |
| [Implementando o comportamento do dispositivo](implementing-device-behavior.md) | Este tópico inclui uma nova seção que explica como obter informações de ponto de extremidade usando a nova interface [**IUPnPRemoteEndpointInfo**](/windows/desktop/api/Upnphost/nn-upnphost-iupnpremoteendpointinfo) .                                                                                                                                                                                                     |
| [Configurações de configuração](configuration-settings.md)             | Este novo tópico fornece informações sobre as configurações do registro que afetam o comportamento das APIs de UPnP.                                                                                                                                                                                                                                                                    |
| [Códigos de erro do dispositivo](device-error-codes.md)                     | Este novo tópico explica como um código de erro de um dispositivo é convertido em um valor HRESULT e vice-versa. Uma compreensão desse processo é necessária para avaliar um valor HRESULT que é retornado pelos métodos [**IUPnPService:: InvokeAction**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-invokeaction) e [**IUPnPService:: QueryStateVariable**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-querystatevariable) . |



 

 

 




