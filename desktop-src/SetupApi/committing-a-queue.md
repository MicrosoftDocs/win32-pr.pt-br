---
description: Depois que todas as operações de arquivo desejadas tiverem sido enfileiradas, a fila deverá ser confirmada. Isso faz com que as operações de arquivo enfileiradas sejam processadas.
ms.assetid: 536f47f5-785e-4a83-a500-c769442e3e68
title: Confirmando uma fila
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d995f6811dbd19bba9e13f29bc119cdf2f471f74
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103663252"
---
# <a name="committing-a-queue"></a>Confirmando uma fila

Depois que todas as operações de arquivo desejadas tiverem sido enfileiradas, a fila deverá ser confirmada. Isso faz com que as operações de arquivo enfileiradas sejam processadas.

Uma fila de arquivos não pode ser reutilizada após ser confirmada. A prática recomendada é coletar todas as operações de arquivo necessárias para a fila de arquivos e confirmar a fila apenas uma vez. Se o processamento adicional da fila for necessário depois que ela tiver sido confirmada, o identificador da fila deverá ser fechado e uma nova fila de arquivos será criada. Para confirmar a fila de arquivos, chame a função [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) , especificando uma rotina de retorno de chamada. A rotina de retorno de chamada receberá notificações de **SetupCommitFileQueue** conforme as operações de arquivo são processadas. Se você quiser usar a rotina de retorno de chamada de fila padrão, primeiro deverá inicializar o contexto necessário chamando [**SetupInitDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallback) ou [**SetupInitDefaultQueueCallbackEx**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitdefaultqueuecallbackex). Para obter mais informações sobre a rotina de retorno de chamada de fila padrão, consulte [rotina de retorno de chamada de fila padrão](default-queue-callback-routine.md).

> [!Note]  
> [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) deve ser chamado antes que a fila seja fechada. Todas as operações que não forem confirmadas quando [**SetupCloseFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupclosefilequeue) for chamado não serão executadas.

 

 

 



