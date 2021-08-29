---
title: Autorização de serviço
description: Um aplicativo pode implementar autorização personalizada para mensagens de entrada em um host de serviço .
ms.assetid: 75bcf051-3983-48fc-8121-0984ac9cdcb9
keywords:
- Serviços Web de autorização de serviço para Windows
- WWSAPI
- Wws
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b84b9947d088d5f594ac11f0ee83cc03925f8a3bbc9aeceae0bc7d5cb120477
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120109836"
---
# <a name="service-authorization"></a>Autorização de serviço

Um aplicativo pode implementar autorização personalizada para mensagens de entrada em um host de serviço .


Um host de serviço recebe um retorno de chamada de segurança [**WS \_ SERVICE SECURITY \_ \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_service_security_callback) como parte do PONTO DE EXTREMIDADE DE SERVIÇO do [**WS \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint) que é passado para a [**função WsCreateServiceHost.**](/windows/desktop/api/WebServices/nf-webservices-wscreateservicehost) Esse retorno de chamada é invocado quando [a \_ MENSAGEM WS](ws-message.md) é recebida.

O aplicativo pode contar com esse retorno de chamada para implementar autorização personalizada para mensagens de entrada no host de serviço. Se a autorização falhar, a função de retorno de chamada de segurança retornará um RH de falha e o host do serviço anulará o canal.

Consulte o nome de usuário sobre o exemplo de SSL, [HttpCalculatorWithUserNameOverSslServiceExample](httpcalculatorwithusernameoversslserviceexample.md), para ver um exemplo de implementação.

 

 




