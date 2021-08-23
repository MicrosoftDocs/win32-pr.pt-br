---
description: Depois que uma fila for confirmada chamando SetupCommitFileQueue, ela começará a processar as operações na fila. Em cada etapa, a fila envia uma notificação para a rotina de retorno de chamada especificada na chamada para SetupCommitFileQueue.
ms.assetid: 866e1066-b6e0-43d3-8af4-bd37fbc024e2
title: Notificações de fila
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06858eeb5c6e9abe200792f83edcc83503270ed2706450d35ef36d5dddc80d06
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119665486"
---
# <a name="queue-notifications"></a>Notificações de fila

Depois que uma fila for confirmada chamando [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea), ela começará a processar as operações na fila. Em cada etapa, a fila envia uma notificação para a rotina de retorno de chamada especificada na chamada para **SetupCommitFileQueue.**

A seguir está a sintaxe que [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) usa para enviar uma notificação para a rotina de retorno de chamada.

``` syntax
MsgHandler(          //the specified callback routine
    Context,         //context used by the callback routine
    Notification,    //queue notification code
    Param1,          //additional notification information
    Param2               //additional notification information
);
```

Os valores de *Param1* e *Param2 contêm* informações adicionais relevantes para a notificação que está sendo enviada para a rotina de retorno de chamada. Cada notificação, seus valores *Param1* e *Param2* e como a rotina de retorno de chamada de fila padrão lida com essa notificação, é descrita em detalhes em Notificações da Fila [de Arquivos](file-queue-notifications.md).

 

 



