---
title: Autorização de serviço
description: Um aplicativo pode implementar a autorização personalizada para mensagens de entrada em um host de serviço.
ms.assetid: 75bcf051-3983-48fc-8121-0984ac9cdcb9
keywords:
- Serviços Web de autorização de serviço para Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c296dc6b4900bd20df7d1e70631e758599a0028d
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/04/2020
ms.locfileid: "104085002"
---
# <a name="service-authorization"></a>Autorização de serviço

Um aplicativo pode implementar a autorização personalizada para mensagens de entrada em um host de serviço.


Um host de serviço recebe um [**retorno de \_ \_ \_ chamada**](/windows/desktop/api/WebServices/nc-webservices-ws_service_security_callback) de segurança de serviço WS de retorno de chamada como parte do [**ponto de \_ \_ extremidade do serviço WS**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint) , que é passado para a função [**WsCreateServiceHost**](/windows/desktop/api/WebServices/nf-webservices-wscreateservicehost) . Esse retorno de chamada é invocado quando a [ \_ mensagem WS](ws-message.md) é recebida.

O aplicativo pode contar com esse retorno de chamada para implementar a autorização personalizada para mensagens de entrada no host de serviço. Se a autorização falhar, a função de retorno de chamada de segurança retornará um HR de falha e o host de serviço abortará o canal.

Consulte o nome de usuário sobre SSL example, [HttpCalculatorWithUserNameOverSslServiceExample](httpcalculatorwithusernameoversslserviceexample.md), para obter um exemplo de implementação.

 

 




