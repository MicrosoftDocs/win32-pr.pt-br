---
title: Cancelamento
description: A maioria das operações no WWSAPI pode ser cancelada durante a execução.
ms.assetid: d73d76e1-bd78-40ce-9f92-e282b6b127ce
keywords:
- Serviços Web de cancelamento para Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6e979455e898922dfb7c81381c1f1aafd455274
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/04/2020
ms.locfileid: "104294631"
---
# <a name="cancellation"></a>Cancelamento

A maioria das operações no WWSAPI pode ser cancelada durante a execução.

A função que você usa para cancelar uma operação depende do objeto afetado.

| Função                                           | Descrição                                                                                                            |
|----------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| [**WsAbortChannel**](/windows/desktop/api/WebServices/nf-webservices-wsabortchannel)           | Cancela todas as entradas e saídas pendentes em um canal especificado e define o estado do canal para o estado do WS \_ Channel com \_ \_ falha. |
| [**WsAbortListener**](/windows/desktop/api/WebServices/nf-webservices-wsabortlistener)         | Cancela todas as entradas e saídas pendentes em um ouvinte especificado.                                                          |
| [**WsAbortServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wsabortserviceproxy) | Cancela todas as entradas e saídas pendentes em um proxy de serviço especificado.                                                     |
| [**WsAbortServiceHost**](/windows/desktop/api/WebServices/nf-webservices-wsabortservicehost)   | Interrompe e descontinua as operações atuais no host de serviço.                                                    |
| [**WsAbandonCall**](/windows/desktop/api/WebServices/nf-webservices-wsabandoncall)             | Abandona uma chamada, uma chamada especificada em um proxy de serviço especificado.                                                        |



 

Para obter informações sobre cancelamentos que afetam [operações de serviço do servidor](server-side-service-operations.md) e retornos de chamada de modelo de serviço, consulte [cancelamento de chamada](call-cancellation.md).


 

 




