---
title: Cancelamento
description: A maioria das operações no WWSAPI pode ser cancelada durante a execução.
ms.assetid: d73d76e1-bd78-40ce-9f92-e282b6b127ce
keywords:
- Serviços Web de cancelamento para Windows
- WWSAPI
- Wws
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf75bd8d07d8f78ddf0a5750e6f4f96feb073dc15b8e63ed23ab8ceb061de145
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117841776"
---
# <a name="cancellation"></a>Cancelamento

A maioria das operações no WWSAPI pode ser cancelada durante a execução.

Qual função você usa para cancelar uma operação depende do objeto afetado.

| Função                                           | Descrição                                                                                                            |
|----------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| [**WsAbortChannel**](/windows/desktop/api/WebServices/nf-webservices-wsabortchannel)           | Cancela todas as entradas e saídas pendentes em um canal especificado e define o estado do canal como WS \_ CHANNEL \_ STATE \_ FAULTED. |
| [**WsAbortListener**](/windows/desktop/api/WebServices/nf-webservices-wsabortlistener)         | Cancela todas as entradas e saídas pendentes em um ouvinte especificado.                                                          |
| [**WsAbortServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wsabortserviceproxy) | Cancela todas as entradas e saídas pendentes em um proxy de serviço especificado.                                                     |
| [**WsAbortServiceHost**](/windows/desktop/api/WebServices/nf-webservices-wsabortservicehost)   | Interrompe e descontinua as operações atuais no host de serviço.                                                    |
| [**WsAbandonCall**](/windows/desktop/api/WebServices/nf-webservices-wsabandoncall)             | Abandonar uma chamada, uma chamada especificada em um proxy de serviço especificado.                                                        |



 

Para obter informações sobre cancelamentos que afetam as [operações de serviço do](server-side-service-operations.md) lado do servidor e retornos de chamada do modelo de serviço, consulte Cancelamento de [chamada.](call-cancellation.md)


 

 




