---
description: Depois que uma fila é confirmada chamando SetupCommitFileQueue, ela começará a processar as operações em fila. Em cada etapa, a fila envia uma notificação para a rotina de retorno de chamada especificada na chamada para SetupCommitFileQueue.
ms.assetid: 866e1066-b6e0-43d3-8af4-bd37fbc024e2
title: Notificações de fila
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 842a3ebc82640789fdb6e730e881d6790a0d642b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105756547"
---
# <a name="queue-notifications"></a>Notificações de fila

Depois que uma fila é confirmada chamando [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea), ela começará a processar as operações em fila. Em cada etapa, a fila envia uma notificação para a rotina de retorno de chamada especificada na chamada para **SetupCommitFileQueue**.

Veja a seguir a sintaxe que o [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) usa para enviar uma notificação para a rotina de retorno de chamada.

``` syntax
MsgHandler(          //the specified callback routine
    Context,         //context used by the callback routine
    Notification,    //queue notification code
    Param1,          //additional notification information
    Param2               //additional notification information
);
```

Os valores de *param1* e *param2* contêm informações adicionais relevantes para a notificação que está sendo enviada para a rotina de retorno de chamada. Cada notificação, seus valores *param1* e *param2* e como a rotina de retorno de chamada de fila padrão manipula essa notificação, é descrita em detalhes em notificações de [fila de arquivos](file-queue-notifications.md).

 

 



