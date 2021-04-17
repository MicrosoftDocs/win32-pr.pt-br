---
description: Se a rotina de retorno de chamada de fila padrão for inicializada e especificada quando SetupCommitFileQueue for chamado, a fila chamará a rotina de retorno de chamada de fila padrão internamente e você não precisará fazer nada mais.
ms.assetid: a976c275-f128-490d-a544-efbfc6fd87f4
title: Chamando a rotina de retorno de chamada de fila padrão
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b24449fc1fcd92d8041de6f104092f45925a495b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105811276"
---
# <a name="calling-the-default-queue-callback-routine"></a>Chamando a rotina de retorno de chamada de fila padrão

Se a rotina de retorno de chamada de fila padrão for inicializada e especificada quando [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) for chamado, a fila chamará a rotina de retorno de chamada de fila padrão internamente e você não precisará fazer nada mais.

Se você criar uma rotina de retorno de chamada de filtro que dependa da rotina de retorno de chamada de fila padrão para manipular um subconjunto das notificações de fila, a rotina de retorno de chamada de filtro deverá chamar [**SetupDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka) explicitamente.

> [!IMPORTANT]
> Ao chamar [**SetupDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka) explicitamente, você deve passar o ponteiro void retornado por [**SetupInitDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallback) ou [**SetupInitDefaultQueueCallbackEx**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallbackex).

 

> [!Note]  
> Uma maneira de fazer isso é criar uma estrutura de contexto para sua rotina de retorno de chamada personalizada que inclua como um de seus membros o ponteiro void retornado por [**SetupInitDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallback) ou [**SetupInitDefaultQueueCallbackEx**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallbackex).

 

 

 



